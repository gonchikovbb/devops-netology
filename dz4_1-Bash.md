1.
echo /c/Users/Администратор/bash_completion.d/*.bash будет выводить a+b, потому что перед a и b нет знака $, и bash будет обращаться не к переменным a и b.
echo  будет выводить 1+2, перед a и b стоят $, значит Bash обращается к переменным a и b, а они а=1 и=2.
echo  будет выводить 3, так как выражение с переменными 173.194.222.113+5 под общей скобкой с $


2.
while ((1==1)
do
curl https://localhost:4757
if ((0 != 0))
then
date >> curl.log
elif ((0 =0))
then
break
fi
done
3.
#!/usr/bin/env bash
array_int=(192.168.0.1 173.194.222.113 87.250.250.242)
while ((1==1))
do
for a in 192.168.0.1 173.194.222.113 87.250.250.242
     do
     for (( b=1; b<=5; b++ ))
             do
             ping –c 1 173.194.222.113
             done
       done
if ((0 !=0))
then
ping >> log.log
fi
done
4.
#!/usr/bin/env bash
array_int=(192.168.0.1 173.194.222.113 87.250.250.242)
while ((1==1))
do
for a in 192.168.0.1 173.194.222.113 87.250.250.242
     do
     for (( b=1; b<=5; b++ ))
             do
             ping –c 1 173.194.222.113
                      if ((0 !=0))
                      then
                      173.194.222.113 >> error_log
                      fi
              done
       done
if ((0 !=0))
then
ping >> log.log
fi
done

