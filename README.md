# application-packaging

EXE to MSI Repackaging
Repackaging means converting a normal installer file (EXE) into an enterprise deployable MSI package

What is Repackaging?
Repackaging is a process where we:

Take a snapshot of the system before installation

Install the EXE application

Take another snapshot after installation

The tool compares both snapshots

Generates an MSI based on the changes

Why do we convert EXE to MSI?

We convert EXE to MSI because MSI is the standard Windows Installer format used in enterprise deployments. It supports silent installation, centralized deployment through SCCM/Intune, better logging, repair, rollback, and clean uninstall, which makes software management easier in large organizations.

Using centralized deployment tools like SCCM or Intune. The admin uploads the MSI package, targets device groups, and the tool pushes silent installation to all machines automatically.

IRP --> ISM
----------------------------------------------------------------------------

Steps:

Step 1: Download the Application Installer
Open Browser (Microsoft Edge)
Search for the application
Download the EXE installer

Step 2: Create Repackager Folder on Desktop
Go to Desktop
Create a new folder

\\Step 3: Open Command Prompt (CMD)
\\Right-click → Paste the folder path
\\Example:
\\cd "C:\Users\Admin\Desktop\Repackager"

step3: Start the Repackaging Tool
repackaging 1:
repackager folder on the desktop 
go to repack -> right click -> shift -> copy as path
on cmd -> right click enter
next-> multiple steps -> Analyze Initial System Status
This scan is called:
Before Installation Snapshot

step 4: 
Install winzip via Desktop -> click on winzip

step 5:

repackaging 2:

run the repackager command again by upparrow ->key enter
Multiple steps -> Analayze System Status Changes 
give product name and company name 
you must get error popups do yes yes yes

step 6:
windowsC:\user\repackgeruotput\win10\
Copy win10 folder and paste in quick access -> select ipadress
rutuja -> /newfolder/paste

------------------------
 Go to cloud 
 ----------
 open repackager folder -> winzip repackager -> winzip open in admin studio -> exclude unneccesary files 
 save and build 

step 7:
open installshield in cloud lab
click on Open ->winzip.exe
C:\user\administrator\desktop\rutuja\repackaging2\winzip\msi_package\winzip\installshield project
change:
package\product\upgrade code
authur: Rutuja {repackagers name}
version: check in appwiz.cpl

property manager ->add-> new
ALLUSER -1
REBOOT-ReallySuppress
ARPCOMMENTS- Rutuja

save->release wizard
select
compress all files
uncheck to setup launcher next next and finish 

Result ---
C;\User\administrator\desktop\rutuja\repackging2\winzip\msi_package\winzip\product confi\release2
diskimage and logfiles

SUCCESFULLY Got the logfile 
go to win10 --> Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Windows\CurrentVersion\Uninstall
check for newly installed appliction (we have to check if the application is in uninstalled registry)

RESULT
---------------------------------
MSI is properly registered in Windows
Your package is enterprise-ready
Application installation is captured correctly
 delete every thing you did at last
 
