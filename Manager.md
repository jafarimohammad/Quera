# Bonus For Employee ( input file: employee.csv ):
```
#!/bin/bash
file="$cat ./employee.csv"
program="$1"
id="$2"
if [ $program == "bonus" ]
then
        if [ $(cat $file | awk 'NR==1' | awk -F',' {'print $1'}) == "$id" ]
        then
		bonus="$"
                reward="0.05"
                salary=$(cat $file | awk 'NR==1' | awk -F',' {'print $5'})
                bonus+=$(echo $salary $reward | awk '{printf "%4.0f\n",$1*$2}')
                echo $(cat $file | awk 'NR==1' | awk -F',' {'print $3'}) will get $bonus bonus



        elif [ $(cat $file | awk 'NR==2' | awk -F',' {'print $1'}) == "$id" ]
        then
		bonus="$"
                reward="0.05"
                salary=$(cat $file | awk 'NR==2' | awk -F',' {'print $5'})
                bonus+=$(echo $salary $reward | awk '{printf "%4.0f\n",$1*$2}')
                echo $(cat $file | awk 'NR==2' | awk -F',' {'print $3'}) will get $bonus bonus

        elif [ $(cat $file | awk 'NR==3' | awk -F',' {'print $1'}) == "$id" ]
        then
		bonus="$"
                reward="0.05"
                salary=$(cat $file | awk 'NR==3' | awk -F',' {'print $5'})
                bonus+=$(echo $salary $reward | awk '{printf "%4.0f\n",$1*$2}')
                echo $(cat $file | awk 'NR==3' | awk -F',' {'print $3'}) will get $bonus bonus

        elif [ $(cat $file | awk 'NR==4' | awk -F',' {'print $1'}) == "$id" ]
        then
		bonus="$"
                reward="0.05"
                salary=$(cat $file | awk 'NR==4' | awk -F',' {'print $5'})
                bonus+=$(echo $salary $reward | awk '{printf "%4.0f\n",$1*$2}')
                echo $(cat $file | awk 'NR==4' | awk -F',' {'print $3'}) will get $bonus bonus

        fi
fi
```

# employee.csv:
```
10012,Tehran,Seyed Ali Babaei,09121212121,4000,Narmak-Kooche-Aval
20221,Tehran,Mostafa Karimi,09131313131,3900,Kerman-Kooche-Aval
40521,Semnan,Amin Anvari,09123456789,3800,Piroozi-Kooche-Aval
12140,ALborz,Nima Heydari Nasab,09383838383,4100,Fardis-Kooche-Aval
```
