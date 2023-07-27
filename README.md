
# Lockd 

Abbreviation For `Lock Daemon`. 

Unix-Style Lock Written In Bash. Best Suitable For Termux. 

## Features :- 

1. Open Source. 

2. Single-File Daemon. 

3. Embeddable. 

4. Robust. 

5. Complex Architecture. 

6. 3 Factor Authentication (3FA) ( `Hostname -> Username -> Password` ). 

7. Uses Different Hostnames, Usernames, And Passwords, Than Actual System Hostnames, Usernames, And Passwords. No Need To Expose Confidential Details! 

8. Multi-Level Classification Possible For Multi-User Systems. 

9. Built-In Enabling/Disabling Feature For Entire Lock, By Setting Value Of `loggedin` Variable To Any Number Greater Than `0`, And For Specific Authentication Factors, By Commenting Out Specific Factor Checking Conditional Statements Using `#`. 

10. Custom Commands Can Be Embedded For Each Hostname And/Or User And/Or Password For Internal Mechanism Customization, As Well As User Desired Customization. 

11. Highly Compatible With Termux. 

12. Cannot Interrupt With `CTRL+C` Or Any Type Of Interrupt Signal. 

13. Can Be Customized To Greet Individual Users With Individual Welcome Messages, And Run Various Commands Specifically As Per Individual User's Choice, As Desired. 

14. Easy To Understand, For `Features -> 9.`. 

15. Can Increase And/Or Decrease The Number Of Attempts Of Failed Authentication Factors, By Changing The Values Of `failhnamecount` And/Or `failunamecount` And/Or `failpwordcount` To Desired Number Of Attempts. 

## Drawbacks :- 

1. Doesn't Uses Real Hostnames, Usernames, And Real Passwords For Classification. 

2. Can Bypass If :- 

	1. External Access To Daemon File Is Possible. 

	2. If Any Time-Consuming Process Is Running Before LockD, And That Process Is Interrupted Manually. E.g. :- `Time-Consuming_Process && lockd` Or `Time-Consuming_Process ; lockd`. 

3. Malicious Actors Can Create Backdoors, If, External Access To Daemon File Is Possible. 

4. Doesn't Natively Work On Shells Other Than Bash ( Might Work On Shells Based On Bash ). For Making It Work On Other Shells, Entire Code Of The `LockD` Mechanism Needs To Be Re-Written Using The Target Shell Scripting Language. 

## Install :- ( For On Termux Start, Or, When `.bashrc` Is Called.) 

1. Download The LockD File `lockd`. 

	1. Using `git clone`. 

	2. Using `Download File` Feature Of This Repository. 

2. Move The Downloaded `lockd` File In The Same Directory Where `.bashrc` Is Stored. 

3. Provide `Execute` Permission Using `chmod +x lockd`. 

4. Append This New Line In `.bashrc` :- 

	`./lockd`

5. Change Hostname(s), Usernames(s) From Conditional Statements, And Password From Predefined Variable Of `lockd` File, As You Desire. 

Note :- You Can Add More Hostnames, Usernames Per Single Hostname, Password Variables Per Single Username, As You Desire. 

## Security :- 

### To Avoid Drawback -> 2 -> 2 :- 

	1. Make Sure That The `lockd` File Is Starting First, Before Any Time-Consuming Process Or Any Process That Cannot Be Interrupted ( E.g. :- Neofetch, Which Takes Time To Print System Information ). 

	2. If `.bashrc` Contains Important System Commands, Give Them First Priority, Then Second Priority To `lockd`, Then To Any Other Non-System Interruptable Process. 

### To Avoid Drawback -> 2 -> 2 After Embedding LockD Inside An Application Software :- 

	1. Make Sure That The `lockd` File Is Starting First, Before Any Time-Consuming Process Or Any Process That Cannot Be Interrupted. 

### Code-Level Security Is Provided, For System-Level Security, You Are On Your Own! 

### If Any Issue/Defect/Bug/Error/Exception/Etc. Occurs And/Or Found, Leaving Your Device(s)/Computer(s)/Machine(s)/System(s) Vulnerable, STOP USING LockD AS SOON AS POSSIBLE! 

## Responsibility And Liability :- 

1. If Any Loss ( Data/System/Etc. ) Occurs, I, The Creator Of This `LockD` Mechanism, Am Neither Responsible, Nor Liable. 

2. If Any Issue/Defect/Bug/Error/Exception/Etc. Occured And/Or Found In This `LockD` Mechanism, And Can Be Avoided By Modifying The Code Of This `LockD` Mechanism, :- 

	1. If The Issue/Defect/Bug/Error/Exception/Etc. Is Locally Occured And/Or Found On A Single Device/Computer/Machine/System, Feel Free To Modify The Code Of This `LockD` Mechanism Locally In The Device/Computer/Machine/System, To Avoid The Occured And/Or Found Issue/Defect/Bug/Error/Exception/Etc, BUT, Then That Modifier/Person Who Modified The Code Of This `LockD` Mechanism Locally, And/Or The Organization/Company/Group Of Companies/Etc. Under Which The Modifier/Person Who Modified The Code Of This `LockD` Mechanism Locally, Is Working And/Or Contributing For, Is Entirely Responsible For Any Loss ( Data/System/Etc. ) Caused By The Locally Modified Code Of This `LockD` Mechanism. 

	2. If The Issue/Defect/Bug/Error/Exception/Etc. Is Globally Occured And/Or Found On Multiple Devices/Computers/Machines/Systems, Feel Free To Raise Issue(s) Or Pull Request(s) On This Repository, BUT, If Any Loss ( Data/System/Etc. ) Occurs Before And/Or After The Issue/Defect/Bug/Error/Exception/Etc. Is Occured And/Or Found, I, The Creator Of This `LockD` Mechanism, Am ( STILL ) Neither Responsible, Nor Liable. 

# Made In Nano On Termux. 

Heck! Even This README Is Made in Nano On Termux. 

# `Thanks!`

