---
sidebar_label: 'Exercise: Web Macro Download File'
hide_title: 'true'
---

## Exercise: Create a Web Macro Task to Download a File

### Objective 

Use an OpCon RPA Web Macro to download a file from website

### Instructions 

#### Create the Web Macro Job and Task

1. In the RPA Tray Client, create a **New Web Macro Task**.
2. Name the Job as **Web Macro Download File**.

#### Record the Automation Steps

1. Navigate to **Web Macro > Actions** to view the Action Sequence

*You have two options:*

:::info

In this exercise we will use the **Record Feature**

:::

**Drag and Drop**: Manually drag actions from the left panel to the right sequence panel.

*or* 

**Record Feature** (*Recommended*):

2. Click the Record button.
3. If a new window opens on another screen, drag it into view.
4. Begin recording your actions.

#### Navigate to the Target Website

1. Enter the desired URL at the top and  browse to the page.
2. As you click through the webpage, a blue outline around the selected object will indicate that the step is saved. You will see the steps populate in the right Sequence frame as they are clicked.
    - In this case, we are navigating to `https://github.com/smatechnologies`.
    - Next click on the **opcon-web-installer** link.
    - Scroll to and click the **latest release** link.
    - Click the **OpConWebIntaller.zip** file link.
3. Modify the folder and other parameters if necessary and click **OK**.
4. Click the **Stop** button in the bottom right hand corner of the client to stop the recording.
5. Select **Yes** to save the recorded actions.

#### Test Run and Verify File Download 

1. Click on **Test Run** to test the workflow.
2. Verify that the expected file was downloaded during the worklfow test run.