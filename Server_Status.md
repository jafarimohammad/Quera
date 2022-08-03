# بررسی سلامت سرورها
فایلی شامل چهار ستون از اعداد داده شده است. ستون اول شامل یک حرف انگلیسی است که شناسه هر سرور محسوب می شود. سه ستون دیگر هر کدام شامل شاخص‌های مربوط به سرورها هستند که به ترتیب، شاخص استفاده سی پی یو، رم و شبکه است. هر شاخص در بازه ی بسته‌ی ۰ تا ۱۰۰ قرار دارد.

اسکریپتی بنویسید که تشخصی دهید آیا سرورها سلامت هستند یا نه. مبنای سلامتی هر سرور این است که هر شاخص بزرگ‌تر یا مساوی ۵۰ باشد.

# نمونه ورودی:
```
A 29 23 50
B 33 39 75
C 79 85 80
D 99 88 69
```
# status.sh:
```
#!/bin/bash

filename="$1"
A="Pass"
B="Pass"
C="Pass"
D="Pass"

if [[ $(cat $filename | awk 'NR==1' | awk {'print $2'}) -le 50 ]]  || [[ $(cat $filename | awk 'NR==1' | awk {'print $3'}) -le 50 ]] ||[[ $(cat $filename | awk 'NR==1' | awk {'print $4'}) -le 50 ]]
then
        A="Fail"

fi

if [[ $(cat $filename | awk 'NR==2' | awk {'print $2'}) -le 50 ]] || [[ $(cat $filename | awk 'NR==2' | awk {'print $3'}) -le 50 ]] || [[ $(cat $filename | awk 'NR==2' | awk {'print $4'}) -le 50 ]]
then
        B="Fail"

fi

if [[ $(cat $filename | awk 'NR==3' | awk {'print $2'}) -le 50 ]] || [[ $(cat $filename | awk 'NR==3' | awk {'print $3'}) -le 50 ]] || [[ $(cat $filename | awk 'NR==3' | awk {'print $4'}) -le 50 ]]
then
        c="Fail"
fi

if [[ $(cat $filename | awk 'NR==4' | awk {'print $2'}) -le 50 ]] || [[ $(cat $filename | awk 'NR==4' | awk {'print $3'}) -le 50 ]] || [[ $(cat $filename | awk 'NR==4' | awk {'print $4'}) -le 50 ]]
then
        D="Fail"
fi

echo A: $A
echo B: $B
echo C: $C
echo D: $D
```


# NOTE:
1. Your script MUST read the input from a given file as follows:
2. $ ./count_names.sh input.txt
3. Your script MUST print the result to the stdout.
4. Your script MUST conform to the output format provided in the question.
5. ATTENTION: DON'T change this file name!
