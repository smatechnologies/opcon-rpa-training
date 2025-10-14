---
sidebar_label: 'Conditions and Loops'
hide_title: 'true'
---

## Conditions

In OpCon RPA, Conditions are logical checks that determine whether a task or job should proceed, branch, or terminate. They are part of the flow control mechanism and are essential for building intelligent, responsive automation workflows.

### Condition Types

#### If (simple)

![](../static/img/rpa-ifcondition.png)

Check the condition and perform certain actions based on the result of the condition. If the specified condition is true, then execute the left action sequence. Otherwise, execute the right action sequence.

#### Switch

![](../static/img/rpa-switchcondition.png)

Select one choice from a number of activities to execute, based on the value.

## Loops

OpCon RPA supports several loop types to automate repetitive tasks:

### Loop Types

#### For Loop

![](../static/img/rpa-forloop.png)

Executes a task a specific number of times using numeric start and end values (e.g., from 1 to 100).

#### While Loop

![](../static/img/rpa-whileloop.png)

Continues execution as long as a condition is true. Useful for dynamic checks like “while file exists” or “while value < threshold.”

#### Do While Loop

![](../static/img/rpa-dowhileloop.png)

Similar to While, but guarantees at least one execution before checking the condition.

#### For Each Loop

![](../static/img/rpa-foreachloop.png)

Iterates over a list of items—such as rows in a spreadsheet or lines in a string.

#### Flow / Label / Go To

![](../static/img/rpa-flowloop.png)

![](../static/img/rpa-labelloop.png)

![](../static/img/rpa-gotoloop.png)

These allow more advanced control, such as jumping to specific labeled tasks or breaking out of loops based on conditions.

#### End Loop / Continue Loop

![](../static/img/rpa-endloop.png)

![](../static/img/rpa-continueloop.png)

* End Loop stops the loop entirely.
* Continue Loop skips the current iteration and starts the next—ideal for exception handling.

These loop types are configured within the VisualCron Job Task interface, where you define start/end tasks and loop conditions.


### Configuring Loops

#### Defining Loop Boundaries​

Set start and end tasks to encapsulate actions within a loop for clear execution boundaries.​

#### Setting Loop Conditions​

Loop conditions include numeric ranges, booleans, or list iterations to control loop execution flow.​

#### Using Variables and Expressions​

Dynamic loop configuration uses variables and expressions for adaptable and responsive automation workflows.​
#### Loop Settings Interface​

The loop settings interface allows selection of loop types and input of relevant parameters easily.

### Exception Management

#### Error Logging​

OpCon RPA logs errors during loop execution, aiding in troubleshooting and improving reliability.​

#### Conditional Failure Handling​

Using conditional branches allows skipping problematic data or retrying failed tasks gracefully.​

#### Retry Logic Implementation​

Retry logic in loops enables multiple task attempts before exiting, enhancing workflow resilience.

### Best Practices

#### Avoid Infinite Loops​

Set clear exit conditions to prevent loops from running endlessly and causing system issues.​

#### Modularize Loop Logic​

Break loop logic into modules to improve readability and make maintenance easier.​

#### Monitor Nested Loops​

Keep track of performance impact as nested loops can consume significant system resources.​

#### Use Descriptive Naming​

Document loop behavior with clear variable names and comments to enhance understanding.