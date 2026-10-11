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

3. Difference between Wget and Curl command
   The Wget command is used to download the files , while curl command is used to transfer data to and from the URL, specially when working with API.
For example:
$wget https://abhishekProject.com/devops.zip
   The File id downloaded to the current directory by default
$curl -O https://abhishekProject.com/file.zip            
   -O here saves the file using its remote filename.
$curl -I https://abhisheksite.com             <--------- To check whether website is rechable
   This requests HTTP response headers, which can include a status such as 200 OK
$curl -X GET https://abhishekproject.site.com/posts/1                 <---- Testing a REST API using curl
$curl -X POST htts://httpbin.org/post \
   -H "content-Type: application/json" \
   -d '{"name":"Abhishek","role":"devops" Engineer"}'

Here , -X POST specifies the HTTP header
       -H adds an HTTP header
       -d supplies the request body
       

