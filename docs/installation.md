---
sidebar_label: 'Exercise: Installation'
hide_title: 'true'
---

## Exercise: Install RPA Agent

## Objective

Install and configure the RPA Agent
 
## Summary

Install the files needed to run the RPA Agent. Create a special RPA User to run the RPA Jobs and configure the RPA Tray Client so that RPA Tasks can be defined.

## Instructions

### Download Files

1. Open a File Explorer window and navigate to ``C:\Users\smauser\Downloads\OpConWebInstaller``

2. Launch the **OpCon Web Installer.exe**

3. Click **Next**

4. Select **Download** from the drop-down for the following items:

  * SMA OpCon RPA Agent

  * RPA Integration

5. Click **Next**

6. Click **Next**

7. Select **Finish** after the download is complete.


### Install the DLL

8. In the File Explorer, navigate to ``C:\Users\smauser\Downloads\OpCon Releases\Integrations\RPA\1.0.0``

9. Unzip the **rpa.zip** file

10. Copy the file and paste it into the ``C:\ProgramData\OpConxps\SAM\plugins`` directory


### Configure the User

11. Launch Solution Manger, use the **Log In With Windows** button to log in

12. Navigate to **Library**, **Access Manager**, **Users**

13. Click the **+** to add a new user with the following settings:

  * In the **First Name** field, enter ``RPA``

  * In the **Last Name** field, enter ``User``

  * In the **Username** field, enter ``RPAUser``

  * In the **Password** field, enter ``password1``

14. Click **Save**

15. Select the **Roles** section, while viewing the User information.

16. Select **Role_ocadm** and click **Save**

17. Select **Settings**

18. Select **Enable external tokens** and click **Save**

19. Log out of Solution Manager as the current user

20. Log in as the **RPAUser**


### Start Defining the Agent

21. In Solution Manger, click the **Heartbeat Icon** in the lower right corner

22. Click **Add** to configure the Agent with the following settings:

  * In the **Name** field, enter **RPAAgent**

  * In the **Type** field, select **RPA**

23. Expand **General Settings**

24. In the**NetCom Name** field, enter ``<Default>``

25. Expand the **RPA Settings** and keep open until the Agent is installed and the RPA Tray Client has launched

 
### Install Agent

26. In the File Explorer, navigate to ``C:\Downloads\OpCon Releases\Agents\RPA\1.0.0``

27. Double click on the **RPAAgent1.0.0.msi**

28. Once the Tray Client has launched, click **Settings** in the Navigation area on the left hand side


### Finish Defining the Agent

29. In the **RPA Tray Client**, copy the **Https UrI** value

30. Paste the value in the **RPA Server URI** field in **Solution Manager**

31. In the **RPA Tray Client**, click **Generate Token**

32. Click **Yes**

33. Click **Ok**

34. Paste the value in the **API Token**field, in **Solution Manager**

  * _This should be saved automatically and the field will appear to be blank_

35. Click **Save** in the **Agent Details** screen.

36. Click the **Change Communication Status** button, select **Enable Full Comm. (Job Start Enabled)


### Define the OpConAPI Connection

37. In the **RPA Tray Client**, while still in **Settings**, click **OpConAPI**

38. Configure the **OpCon API Connection** with the following settings:

  * In the **OpCon API URL field, enter ``https://smatraining``

  * In the **OpCon API User** field, enter ``RPAUser``

  * In the **OpCon API Password** field, enter ``password1``

  * In the **OpCon Agent Name** field, enter ``RPAAgent``

39. Click **Get OpCon API Token**

40. Click **Ok**

  * _These fields will become empty and the **Agent has a registered API Token** will become checked_

:::info

On the Agent screen in Solution Manager, the RPAAgent should show as Communicating along with the SMATraining agent.

:::