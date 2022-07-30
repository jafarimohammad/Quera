# count name in input file

```
#!/bin/bash

filename="$1"    # input filename
count=$( cat $filename | grep -v '^$' | sed  's/,/\n/' | sed  's/!/\n/' | sed  's/|/\n/' | sed  's/    /\n/' | sed  's/ /\n/' | sed  's/\\/\n/' | sed -r '/^\s*$/d' | wc -l )
echo Count: $count
```
# NOTE:
1. Your script MUST read the input from a given file as follows:
2. $ ./count_names.sh input.txt
3. Your script MUST print the result to the stdout.
4. Your script MUST conform to the output format provided in the question.
5. ATTENTION: DON'T change this file name!


# names_input.txt:
```
ali    behnam salar,javad|ehsan\mohammad!hossein

hadi

ali
mohammadreza
```
