# Devops-Learning---Bash-Course-Coderco

this was the first time i truelly learnt how important scripting was and how much it was used, in this module i looked into if statements, variables, parameters and more.

1.SHEBANG

this is the title of every script you write, it could be said different ways but the most common is 
#!/bin/bash

2.Comments
also known as "echo" just like in linux we used this to detail what the script was about so anyone could understand it 

3.Running scripts from anywhere 
this was simple it was to add the script to a folder thats in $PATH.

4.Variables

this lesson i learnt how i can add data to a script

heres my example:
greeting="ronaldo is the best player in the world"
echo $greeting
5.Parameters

i learnt that you can give a script inputs when you run it, the script then knows them as $1, $2 and so on.

example:

echo "first: $1 second: $2"


6.Arithmetic Expansion

this lets you do maths inside your script.

example:

num1=5
num2=10
echo $((num1 + num2))


7.Arithmetic Expansion (with parameters)

instead of hardcoding numbers i can use parameters.

example:

echo $(( $1 + $2 ))


8.if Statements

if statements check if something is true before running.

example:

age=20
if [ $age -gt 18 ]; then
  echo "you are an adult"
fi


9.else and elif

i learnt how to add extra checks with elif and what to do if none match with else.

example:

age=15
if [ $age -gt 18 ]; then
  echo "adult"
elif [ $age -ge 13 ]; then
  echo "teenager"
else
  echo "child"
fi


10.Nested if Statements

i can put if statements inside other ifs to check multiple things.

example:

age=18
score=85
if [ $age -ge 18 ]; then
  if [ $score -ge 80 ]; then
    echo "eligible"
  fi
fi


11.while Loops

i learnt that while loops keep going until the condition is false.

example:

count=1
while [ $count -le 3 ]; do
  echo "count: $count"
  ((count++))
done


12.for Loops

a for loop goes through items one by one.

example:

for i in 1 2 3; do
  echo "number $i"
done


13.break and continue

break stops a loop early, continue skips one turn.

example:

for i in 1 2 3 4 5; do
  if [ $i -eq 3 ]; then
    continue
  fi
  if [ $i -eq 5 ]; then
    break
  fi
  echo "number $i"
done
