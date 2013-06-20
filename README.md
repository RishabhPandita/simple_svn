simple_svn
==========

A Simple Subversion Control System

Implemented using Shell Scripting
Shell used is GNU bash, version 4.2.8(1)-release (x86_64-pc-linux-gnu)


Following are the features of the program:

1)The program is implemented with help of popular tools diff and patch.

2)The program suffices to the specified details in the assignment details,morever
  it doesn't has restrictions as specified in assignment details like number of 
  lines,position where the file can be edited,etc.


3)Metadata files are maintained in hidden directory(.version) to protect from direct manipulations
  by the user.

4)File vN in directory .version holds metadata of Nth version.

5)System is automatically initialised on first commit.

6)Exception Handling implemented:
    
    1)Number of arguments
	2)Check if file exists
	3)Check if version exists

7)Optimisations:
	
	Rather than saving each individual version diff from base versions are saved to 
	reduce memory utilisations.
	A version is selected to be base if the newest commit differs from previous by a 
	predefined threshhold (10 here).
	A base version is registered in key_log file in .version directory.

