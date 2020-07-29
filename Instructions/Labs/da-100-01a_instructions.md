

### Lab 01A

Getting Started

# Overview

**The estimated time to complete the lab is 15 minutes**

In this lab, you connect to the classroom virtual machine and setup the environment. Before commencing this lab, you must have received an account and password. It’s important that you complete the labs by using the provided account.

In this lab, you learn how to:

* Sign in to the Power BI service

* Create a workspace

* Open Power BI Desktop

# Exercise 1: Getting Started

In this exercise, you connect to the classroom virtual machine and setup the environment.

### Task 1: Record your account details

In this task, you will open the **MySettings.txt** file, and record your account details.

*An account has been provided to you by your instructor, and it’s important that you use this account to complete all of the labs. If an account was not provided to you, please browse to https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-signing-up-for-power-bi-with-a-new-office-365-trial and follow the steps to create an account before continuing with this lab*.

1. To open File Explorer, on the taskbar, click the File Explorer program shortcut.

    ![Picture 7](Linked_image_Files/PowerBI_Lab01A_image1.png)

2. In File Explorer, navigate to the **D:\DA100\Setup** folder.

3. To open the **MySettings.txt** file, double-click the file.

4. In the **MySettings.txt** file, enter your account name and password next to the labels.

    ![Picture 9](Linked_image_Files/PowerBI_Lab01A_image2.png)

5. To save the **MySettings.txt** file, on the **File** menu, select **Save** (or press **Ctrl+S**).

6. Leave the **MySettings.txt** file open.

7. Leave File Explorer open.

### Task 2: Sign in to the Power BI service

In this task, you will sign in to the Power BI service.

1. To open Edge, on the taskbar, click the Microsoft Edge program shortcut.

    ![Picture 1](Linked_image_Files/PowerBI_Lab01A_image3.png)

9. In Edge, navigate to **http://powerbi.com**.

    *Tip: You can also use the Power BI Service favorite on the Edge favorites bar*.

10. Click **Sign In** (located at the top-right corner).

    ![Picture 5](Linked_image_Files/PowerBI_Lab01A_image4.png)

11. Enter your account details from the **MySettings.txt** file.

12. When prompted to update the password, reenter the provided password, and then enter and confirm a new password. Be sure to update the **MySettings.txt** file with your new password.

13. Complete the sign in process.

14. If prompted by Edge to stay signed in, click **Yes**.

15. In the Power BI service, at the top-right corner, if the “New Look” is not enabled, click the slider control to turn it on.

    ![Picture 13](Linked_image_Files/PowerBI_Lab01A_image5.png)

16. Leave the Edge window open.

  
‎ 

### Task 3: Create a workspace

In this task, you will create a workspace. You will also upgrade your account to Power BI Pro.

*All content you develop in this course will be added to this workspace.*

1. To create a workspace, in the **Navigation** pane (located at the left), click **Workspaces**, and then click **Create a Workspace**.

    ![Picture 14](Linked_image_Files/PowerBI_Lab01A_image6.png)

18. When prompted to upgrade your account to Power BI Pro, click **Try Free**.

    ![Picture 17](Linked_image_Files/PowerBI_Lab01A_image7.png)

    *A Power BI Pro license is required to create and work with workspaces. It’s also required when sharing content. The trial will allow you to work with Pro features for up to 60 days.*

19. When prompted to start the 60-day free Pro trial, click **Start Trial**.

    ![Picture 18](Linked_image_Files/PowerBI_Lab01A_image8.png)

20. When the trial has been extended, click **Close**.

21. Repeat the first step in this task to create the workspace.

22. In the **Create a Workspace** pane (located at the right), in the **Workspace Name** box, enter a name for your workspace.

    *The name you enter must be unique within the tenant. We suggest you name the workspace **Sales Analysis**, and that you also append your initials. For example, the name could be **Sales Analysis AB***.

23. To create the workspace, at the bottom of the pane, click **Save**.

    ![Picture 21](Linked_image_Files/PowerBI_Lab01A_image9.png)

24. In the **Navigation** pane, notice that your workspace is open.

    ![Picture 22](Linked_image_Files/PowerBI_Lab01A_image10.png)

25. You will publish content to the workspace in **Lab 03D**.

  
‎ 

### Task 4: Open Power BI Desktop

In this task, you will open Power BI Desktop, and then sign in using your account.

26. To open the Power BI Desktop, on the taskbar, click the Microsoft Power BI Desktop shortcut.

    ![Picture 2](Linked_image_Files/PowerBI_Lab01A_image11.png)

27. When prompted, click **Sign In**.

    ![Picture 25](Linked_image_Files/PowerBI_Lab01A_image12.png)

28. Complete the sign in process by using the **MySettings.txt** account details.

29. In Power BI Desktop, at the top-right corner, verify that you see your account.

    ![Picture 27](Linked_image_Files/PowerBI_Lab01A_image13.png)

30. Leave Power BI Desktop open.

    *You will commence the development of a data model in **Lab 02A***.

  
‎ 

### Task 5: Update the lab database

In this task, you will run a PowerShell script to update data in the **AdventureWorksDW2020** database.

1. In File Explorer, inside the **D:\DA100\Setup** folder, right-click the **UpdateDatabase-1-UpdateAccount.ps1** file, and then select **Run with PowerShell**.

    ![Picture 28](Linked_image_Files/PowerBI_Lab01A_image14.png)

32. In the **Windows PowerShell** window, when prompted to enter your account, paste in your account name from the **MySettings.txt** file.

    *Tip: To paste into the **Windows PowerShell** window, right-click at the **Account** prompt*.

    ![Picture 29](Linked_image_Files/PowerBI_Lab01A_image15.png)

33. To update the database, press **Enter**.

34. When prompted to press any key to continue, press **Enter** again.

    *The **AdventureWorksDW2020** database has been updated to use your account details. You are now the salesperson Michael Blythe, whose sales performance is measured by the sales of three sales territory regions: US Northeast, US Central, and US Southeast*.

    *These facts will become relevant when implementing row-level security in **Lab 03B***.
