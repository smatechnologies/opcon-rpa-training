---
sidebar_label: 'Create an Excel Data Robot Task'
hide_title: 'false'
---

# Exercise 2: Create an Excel Data Robot Task

## Objective

Use an OpCon RPA Robot Task to pull Excel Cell data from a workbook and transfer it to a new/different workbook

## Instructions

### Set Up the Excel Source File

1. Create a new Excel Workbook.
2. Name the Excel Workbook **rpasourcebook**.
3. In Cell A1 enter **Bank**.
4. In Cell B1 enter **Rate**.
5. In Cell A2 enter **Amegy**.
6. In Cell B2 enter **6.5**.
7. Save the Workbook.

### Set up the Excel Target File

1. Create a new Excel Workbook.
2. Name the Excel Workbook **rpatargetbook**
3. In Cell A1 enter **Bank**.
4. In Cell B1 enter **Rate**.
5. In Cell A2 enter **Amegy**.
6. Leave Cell B2 blank.
7. Save the Workbook.

### Create a Variable

1. Launch the OpCon RPA Tray Client.
2. Create a new Robot Task and name it **excel-task**
3. Select the **Robot** tab.
4. In the bottom left corner of the tray client, click the **Variables** button.
5. In the RPA Variables screen, click **Add User Variable**.
6. Name the Variable **interest_rate_amegy**.
7. Leave the Variable value blank.
8. Click the **Add** button.

### Create the RPA Task to Read the Cell

1. Select an Excel **Open Workbook** task from the left menu and drag it into the **Sequence** window.
2. In the **File name** box enter the path to your created workbook (**rpasourcebook**).
3. Select an **Excel Cell - Get Cell Value** task from the left menu and drag it into the **Sequence** window below the **Open Workbook** task.
4. Click the **Click to select Excel element** link in the task window.
5. With the source workbook and sheet in focus,click on the cell you wish to retrieve the value from.
6. Hold down the CTRL button and left-click at the same time.
7. Back in the Edit Task Screen - Verify the Cell Address.
8. Select or verify the **Variable type** as **User**.
9. Select or verify the **Variable** as **interest_rate_amegy**.

### Create the RPA Task to Set the Cell 

1. Select an Excel **Open Workbook** task from the left menu and drag it into the **Sequence** window below the **Get Cell Value** task.
2. In the **File name** box enter the path to your created workbook (**rpatargetbook**).
3. Select an **Excel Cell - Set Cell Value** task from the left menu and drag it into the **Sequence** window below the **Open Workbook** task.
4. Click the **Click to select Excel element** link in the task window.
5. With the target workbook and sheet in focus, click on the cell you wish to set cell value on.
6. Hold down the CTRL button and left-click at the same time.
7. Back in the Edit Task Screen - Verify the Cell address.
8. Select or verify the **Value** as the **User Variable** `{USERVAR(interest_rate_amegy)}`.

### Save the Excel File

1. Select an Excel Workbook **Save Workbook** task from the left menu and drag it into the **Sequence** window below the **Set Cell Value** task.
2. Click the **Click to select Excel element** link in the task window.
3. Verify the Workbook name to save is correct.

### Test the Robot

1. Click **Test Run** in the bottom right hand corner of the Robot **Edit Taks** screen.
2. The Robot will run the sequence.
3. Verify that the sequence has completed successfully by checking that the interest rate variable has been set in **rpatargetbook** cell **B2** and that it matches the value in **rpasourcebook** cell **B2**.

### Save the Robot

1. Click **OK** in the bottom right hand corner of the Robot **Edit Task** screen.
2. Choose from **Save and Publish** or **Save as Draft**. In this case, choose **Save and Publish**.
3. Click **OK** to acknowledge that the Robot has been saved and published.
