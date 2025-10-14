---
sidebar_label: 'Exercise: Create a Self Service Button for RPA'
hide_title: 'true'
---

## Exercise: Create a Self Service Button for an OpCon RPA Job

### Build the RPA Schedule and Job

Before linking it to the button, ensure the RPA job is fully configured. For this exercise, use the Schedule and Job created in the **Build an OpCon RPA Job** exercise. Verify that the Schedule has built and is open in the daily.

### Create a Null Job

1. Create a new **Null Job** within the same schedule as the RPA Job (**RPARateSched**).
    - Name: **KeepScheduleOpen**.
    - *This job ensures the schedule remains open so that the Self Service button can dynamically add jobs*
2. Assign a Frequency to the job.
    - Give the Job a Frequency of **OnRequest**.
    - *This keeps the schedule active and ready to accept new jobs*
3. Configure a start offset to ensure the job runs slightly after the schedule opens.
    - *This prevents premature closure of the schedule*

### Create the Self Service Button

This button will trigger the RPA job dynamically.

1. Open OpCon Self Service Portal
2. Navigate to the Self Service configuration panel.
3. Create a New Button and name it **RPA Rate Button**.
4. Create a **$JOB:ADD Event**
    - Schedule Name: **RPARateSched**.
    - Job Name: **RPARateJob**.
    - Frequency Name: **Mon-Fri-N** *(The Frequency for the Event and the OpCon Job must match)*.

:::info Note

When builing a Self Service button in your environment, remember to set Permissions and Visibility
- Assign the button to appropriate user roles
- Ensure only authorized users can trigger the job

:::

### Validate the Workflow

#### Run the Button

1. Click the button to test the Job addition.
2. Confirm that the Job is added to the open Schedule and executes as expected.

### Monitor Execution

Use the OpCon dashboard to track job status and logs if necessary.