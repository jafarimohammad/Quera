# server status: in inputfile:
```
#!/bin/bash

filename="$1"
A="PASS"
B="PASS"
C="PASS"
D="PASS"

if [[ $(cat $filename | awk 'NR==1' | awk {'print $2'}) -le 50 ]]  || [[ $(cat $filename | awk 'NR==1' | awk {'print $3'}) -le 50 ]] ||[[ $(cat $filename | awk 'NR==1' | awk {'print $4'}) -le 50 ]]
then
        A="FAIL"

fi

if [[ $(cat $filename | awk 'NR==2' | awk {'print $2'}) -le 50 ]] || [[ $(cat $filename | awk 'NR==2' | awk {'print $3'}) -le 50 ]] || [[ $(cat $filename | awk 'NR==2' | awk {'print $4'}) -le 50 ]]
then
        B="FAIL"

fi

if [[ $(cat $filename | awk 'NR==3' | awk {'print $2'}) -le 50 ]] || [[ $(cat $filename | awk 'NR==3' | awk {'print $3'}) -le 50 ]] || [[ $(cat $filename | awk 'NR==3' | awk {'print $4'}) -le 50 ]]
then
        c="FAIL"
fi

if [[ $(cat $filename | awk 'NR==4' | awk {'print $2'}) -le 50 ]] || [[ $(cat $filename | awk 'NR==4' | awk {'print $3'}) -le 50 ]] || [[ $(cat $filename | awk 'NR==4' | awk {'print $4'}) -le 50 ]]
then
        D="FAIL"
fi

echo A: $A
echo B: $B
echo C: $C
echo D: $D
```
# sever_input.txt:
```
A 29 23 50
B 33 39 75
C 79 85 80
D 99 88 69
```

# NOTE:
1. Your script MUST read the input from a given file as follows:
2. $ ./count_names.sh input.txt
3. Your script MUST print the result to the stdout.
4. Your script MUST conform to the output format provided in the question.
5. ATTENTION: DON'T change this file name!
