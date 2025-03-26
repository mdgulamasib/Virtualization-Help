# Fixing VirtualBox 7.1.6 Error: **NtCreateFile(\Device\VBoxDrvStub) Failed**

If you’ve recently encountered an error while trying to start a virtual machine in **Oracle VirtualBox 7.1.6**, you’re not alone.

## Error Message

VirtualBox - Error In supR3HardenedWinReSpawn

NtCreateFile(\Device\VBoxDrvStub) failed: 0xc0000034 STATUS_OBJECT_NAME_NOT_FOUND (0 retries) (rc=-101)

Make sure the kernel module has been loaded successfully.

where: supR3HardenedWinReSpawn what: 3 VERR_OPEN_FAILED (-101) - File/Device open failed. Driver is probably stuck stopping/starting. Try 'sc.exe query vboxsup' to get more information about its state. Rebooting may actually help.


## Cause of the Issue
This error typically occurs when the **VirtualBox driver (`vboxsup`)** is not running properly or has failed to start. The issue can be related to Windows security settings, recent updates, or permission issues.

## **Solution: Restart the VirtualBox Service**
To resolve this issue, follow these steps:

1. **Open Command Prompt as Administrator**  
   - Press `Win + S`, type **CMD**, and select **Run as administrator**.

2. **Restart the VirtualBox support driver**  
   - Run the following command:  
     `net start vboxsup`  
   - If the service is already running, you may need to restart it using:  
     `net stop vboxsup`  
     `net start vboxsup`

3. **Reboot your computer (if necessary)**  
   - If the issue persists, try restarting your machine and then relaunch VirtualBox.

## **Final Thoughts**
This quick fix should help you get your Virtual Machine up and running again. If you’re still facing issues, checking for VirtualBox updates or reinstalling the software might help.

🚀 **Hope this helps!** Let me know if you have any questions.

---

## **Find me on Upwork:**  
[Md Gulam Asib on Upwork](https://www.upwork.com/freelancers/mdgulamasib)

Best,  
**Md Gulam Asib**  
*IT Support Specialist*
