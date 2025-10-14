---
sidebar_label: 'Create a Self Service Button for RPA'
hide_title: 'true'
---

## Create a Self Service Button for an OpCon RPA Job

### Build the RPA Schedule and Job

Before linking it to the button, ensure the RPA job is fully configured.

Define the RPA Job in the Schedule

Use OpCon Studio to create the RPA job.
Include all necessary parameters, dependencies, and scripts (e.g., VisualCron macros, REST API calls).

Test the Job Independently

Run the job manually to confirm it executes correctly.


### Create a “KeepScheduleOpen” Job

This job ensures the schedule remains open so that the Self Service button can dynamically add jobs.

1. Create a Null Job
2. In OpCon Studio, create a new job within the target schedule.
Name it something like **KeepScheduleOpen**.
3. Set Frequency

Assign a frequency to the job (e.g., every 5 minutes or hourly).
This keeps the schedule active and ready to accept new jobs.

4. Set Start Offset

Configure a start offset to ensure the job runs slightly after the schedule opens.
This prevents premature closure of the schedule.


### Create the Self Service Button

This button will trigger the RPA job dynamically.

1. Open OpCon Self Service Portal
2. Navigate to the Self Service configuration panel.
3. Create a New Button
4. Name it clearly (e.g., “Run RPA Job”).
5. Configure the Button Action

Use the Add Job Event:

Specify the Schedule Name (where the RPA job resides).
Specify the Job Name (the RPA job you created).
Specify the Frequency Name (same as used in the job setup).

Set Permissions and Visibility

Assign the button to appropriate user roles.
Ensure only authorized users can trigger the job.


### Validate the Workflow

1. Run the Button

Click the button to test the job addition.
Confirm that the job is added to the open schedule and executes as expected.

### Monitor Execution

Use the OpCon dashboard to track job status and logs.