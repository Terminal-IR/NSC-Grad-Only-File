# NSC Graduates Only File Creation

As part of GE - FVT reporting, we found that the college had many thousands of students in the graduate reconciliation file.  There are two main contributors to this:
1: Community College students tend to swirl their enrollments, completing programs and then enrolling again in the future.
2: While we submit Degree Verify files and Enrollment Verification files to NSC we have not provided Graduate Only EV files in the past.

Using the NSC web interface to complete the graduate reconciliation list was untenable given the number of records.

We utilize Colleague as our SIS. The Colleague process for creating a Graduates Only file didn't yield usable results.

This R-Markdown document creates a Graduates Only File and provides some instruction for prepping the file for upload to the NSC FTP service.

## Program Basics
R Markdown is used to build an Excel file that is used as the basis for the NSC Graduates Only File submission This package uses R, but most of the heavy lifting is done in SQL which mirrors my status as an R newbie. **You will need to alter the code to fit your institution’s needs**. If you come up with a better way to do something, please share!  I’m new to R and would appreciate the guidance. 

## Pre-requisites
<ul>
  <li>R and an R IDE such as R-Studio</li>
  <li>A database to get program data from</li>
  <li>R Markdown Package</li>
  <li>Required R libraries are listed at the top of the code</li>
  <li>A little R knowledge</li>
  <li>Some amount of SQL knowledge</li>
 </ul>

## The Files
Sample_Excel_1 is an image inserted in the instructions.</br>
NSC Grads Only File is the R Markdown file.</br>


## What You Will Have To Do (knowledge that you need to bring to the party)
At minimum, you will need to do the following to make these files work for you.
<ol>
  <li>Alter openDBConnection function to connect to your database.
  <li>Alter NSC_GRADS function so the SQL code works with your data source.
</ol>

### How to Make this Work
After your environment is set-up 
Step 1: Create a new R Project
Step 2: Copy the Sample_Excel_1 image file into the project folder 
Step 3: Create a new R Markdown File
Step 4: Copy and paste the code from NSC Grads Only File.RMD into that document
Step 5: Edit the database connection and SQL Code
Step 6: Make sure you are connected to your database via your VPN or whatever processes you use
Step 7: Knit the document and follow the guidance in the created document.

## Debts of Gratitude
Wim McSpadden for his cajoling, dry wit, and Colleauge know-how.
Thanks to everyone involved in making the R libraries I used. 
Love to my wife and kids and thanks for letting burn the midnight oil to develop this package.

## I'm a Newb
If you have any suggestions for improvement, I'm all ears!
Brian Murphy
murphybr@butte.edu
