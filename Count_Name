#!/bin/bash

filename="$1"    # input filename
c=$( cat $filename | grep -v '^$' | sed  's/,/\n/' | sed  's/!/\n/' | sed  's/|/\n/' | sed  's/    /\n/' | sed  's/ /\n/' | sed  's/\\/\n/' | sed -r '/^\s*$/d' | wc -l )
echo Count: $c

# NOTE:
# * Your script MUST read the input from a given file as follows:
#   $ ./count_names.sh input.txt
# * Your script MUST print the result to the stdout.
# * Your script MUST conform to the output format provided in the question.
#
# ATTENTION: DON'T change this file name!

#/////////////////////////////////////////////////////////////////////////////////////////////////

## names_input.txt:
# ali    behnam salar,javad|ehsan\mohammad!hossein

# hadi

# ali
# mohammadreza
