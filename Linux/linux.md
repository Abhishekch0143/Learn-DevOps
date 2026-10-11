1. The Concept of Wheel or sudo group

If you want to give a user with privileged command access we can add that user in the wheel or sudo group

For Example:
$useradd abhishek
$sudo usermod -aG sudo abhishek 

2. Difference between Sed vs Awk command
   sed command is used to find, replace , delete and modify text from the file , While Awk command is used to process the field , extract the column and do the calculations.

For example:
$vi file.txt
  abhishek 1234 active
  rahul 5678 active
  pankaj 9012 stopped
$sed '/s/active/running/g' file.txt
  This will give the output stream as
  -----------------------------------
  abhishek 1234 running
  rahul 5678 running
  pankaj 9012 stopped

$awk '$3 == "running" {print $1}' file.txt
  This will give the output stream as
  -----------------------------------
  abhishek
  rahul

