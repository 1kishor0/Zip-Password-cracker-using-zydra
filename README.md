Zydra is an exciting utility that cracks password protected files. We often face a situation that requires us to crack password protected files such as rar, zip or pdf during pentests sometimes. First, we have to demonstrate how weak the password is. Zydra is a fantastic program that can crack or recover the protected files as well as cracks the linux shadow file. One thing is that zip has upgraded its structure and now they are using a robust encryption algorithm but still zydra crack the legacy zip files, zydra utilizes the standard password attacks such as dictionary and brute force attacks.



So, Lets install the zydra.First of all I should check my python version.


Then install some  prerequisites first . command is: $pip3 install rarfile pyfiglet py-term

 ![image](https://user-images.githubusercontent.com/57821690/209801303-06fa3d9f-5ca1-4280-b8d1-e45e1631efca.png)

Fig 1: prerequisites
After this I have to git clone https://github.com/hamedA2/Zydra.git after the cross checks dictionary. let's get into this directory zydra and let's see there you can see the Python already available that you need to execute.
 ![image](https://user-images.githubusercontent.com/57821690/209801342-61bac272-93b2-4ee4-874d-076499bcb98b.png)
 
 Fig 2: Attacking mode
After executing Zydra in fig 2 we see that there are two mode available one is dictionary attack mode next one is brute force mode. And the following command we can do these attacks. 

![image](https://user-images.githubusercontent.com/57821690/209801353-6592ab9f-d10b-47e7-b5b2-3fa9ef6de160.png) 

Fig 3: Wordlist Tools
In Kali linux there has a built in password cracker wordlist tools where I can use those attack mode by use these lots of possible string combination and find the actual output. But we use a list from a lot of combinations of string downloaded from git hub and push into the zydra.
 ![image](https://user-images.githubusercontent.com/57821690/209801379-6efb6518-fc57-4cb9-983e-3b023a5970e7.png)
Fig 4: Encryption Command
Now In fig 4 shows that encrypted command of an file called README.md . By using this command I protected this file into zip and set password:123.

 ![image](https://user-images.githubusercontent.com/57821690/209801389-e38d82e0-f6c4-48d7-b169-75f05a6692ee.png)

Fig 5: encrypted file
Fig 5 shows that the file being proteceted after run this command.

 ![image](https://user-images.githubusercontent.com/57821690/209801420-c53ea366-e4fb-45aa-bb5b-9b7958e4d67f.png)

Fig 6: Password required
We can’t open these file without password.

 ![image](https://user-images.githubusercontent.com/57821690/209801432-697705af-c3b2-489a-a217-1346593b97bc.png)

Fig 7: All possible passwords on protected.zip


These command extracts all possible strings.

 ![image](https://user-images.githubusercontent.com/57821690/209801457-3e0ded67-3363-4990-910c-074c153261f2.png)

Fig 8: Passwords Combination





For this protected.zip file there are lot of combination password. After that wget function assures all the possible password into the protected files.
 ![image](https://user-images.githubusercontent.com/57821690/209801481-da465e2e-6658-4bc2-93a7-dff915e4050a.png)

Fig 9: Dictionary Attack

Then apply dictionary attack on this zip file.
![image](https://user-images.githubusercontent.com/57821690/209801495-83fe56ef-676d-4090-bc64-41b43818dac3.png) 

Fig 10: Password shown

And get the actual password which I set up in starting.
 ![image](https://user-images.githubusercontent.com/57821690/209801509-8b2bb37c-3ebf-4e94-8ee6-6cb465f06b8f.png)

Fig 11: cracked file

After that I open the README.md file by using this password.

 ![image](https://user-images.githubusercontent.com/57821690/209801524-3215f7ed-ce60-4d4e-8000-1370a3eca4ea.png)

Fig 12: Recover Linux password

python3zydra.py-f/home/kali/Desktop/shadow-d/usr/share/seclists/ Passwords/Common-Credentials/10k-most-common.txt 
Zydra can automatically crack the password or hashes of users found in Linux shadow files but it will totally depends on your dictionary.
