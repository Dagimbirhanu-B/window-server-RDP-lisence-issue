# window-server-RDP-lisence-issue



how to remove RDP lisence issue on window server
====================================================================================
# got to registry edit
wind+R
regedit
#go to the following path
Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Terminal Server\RCM\GracePeriod
# right click on GracePeriod and then permission 
give a full control for administrator 
#if you get 'access denaid' error 
under permission go to advanced and click on change button infront of  owner : SYSTEM
then applay and ok 
# under lisence core on the right side delete the key 
# restart the server to make the chagetake effect 

this method is worked for us on one of our window server 



# How to Remove RDP License Issue on Windows Server

This method helped resolve the **Remote Desktop licensing issue** on one of our Windows Server machines. Follow the steps below carefully.

---

### 🛠 Steps

1. **Open Registry Editor**  
   Press `Win + R`, type `regedit`, and press `Enter`.

2. **Navigate to the following path**:
Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Terminal Server\RCM\GracePeriod

3. **Modify Permissions on `GracePeriod`**:
- Right-click on the `GracePeriod` folder.
- Select **Permissions**.
- Click **Advanced**.
- Click the **Change** button next to the **Owner: SYSTEM**.
- Set the owner to **Administrators**, apply, and OK.

4. **Grant Full Control**:
- Back in the Permissions window, give **Administrators** **Full Control**.

5. **Delete the Key**:
- On the right side of the `GracePeriod` folder, delete the key shown (usually a binary key).
- If you encounter **"Access Denied"**, repeat the steps above to ensure proper permissions.

6. **Restart the Server**:
- Restart the Windows Server to apply the changes.

---

✅ This method resolved the RDP license issue for us on one of our servers.

> **Disclaimer**: Editing the registry can be risky. Always back up the registry before making changes.

