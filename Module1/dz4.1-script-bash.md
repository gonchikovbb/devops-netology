1.
echo /c/Users/Администратор/bash_completion.d/*.bash будет выводить a+b, потому что перед a и b нет знака $, и bash будет обращаться не к переменным a и b.

echo  будет выводить 1+2, перед a и b стоят $, значит Bash обращается к переменным a и b, а они а=1 и=2.

echo  будет выводить 3, так как выражение с переменными $a+$b под общей скобкой с $

2.

```bash
while ((1==1)
do
curl https://localhost:4757
if (($? != 0))
then
date > curl.log
elif (($? = 0))
then
break
fi
done
```

3.
```bash
array_int=(192.168.0.1 173.194.222.113 87.250.250.242)
while ((1==1))
do
for a in ${array_int[@]}
  do
  for (( b=1; b<=5; b++ ))
     do
     nc –zv $a 80
     done
  done
if (($? !=0))
then
$? > log.log
fi
done
```
4.
```bash
array_int=(192.168.0.1 173.194.222.113 87.250.250.242)
while ((1==1))
do
for a in ${array_int[@]}
  do
  for (( b=1; b<=5; b++ ))         
    do   
    nc –zv $a 80
      if (($? !=0))
      then
      $a > error_log
      fi
    done
  done
if (($? !=0))
then
$? > log.log
fi
done
```