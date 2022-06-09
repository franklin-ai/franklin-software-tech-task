# Technical Assessment task for franklin.ai

This is a technical assessment task for [Software Engineering roles](
https://jobs.lever.co/harrison/4f10d488-9417-4128-bc5c-846d75304dae) at [franklin.ai](https://franklin.ai/).

Your task is to develop a command-line tool that processes a stream of events and outputs
a summary of the event data. You may implement the tool using your choice of:

* Rust
* Python
* JavaScript/TypeScript

You are welcome to use external open-source libraries if desired.

Your solution to this task will form the starting point for a 60-minute technical interview,
during which we'll collaboratively review the code, discuss your design choices, and investigate
potential future enhancements and refactorings.

## Task Expectations

You should take a copy of this repo, implement the requirements described below, and push them to GitHub
for discussion in the scheduled technical interview. You're welcome to use a private repository, as
long as it is visible to `@doc-E-brown`, `@rickfoxcroft`, `@rfk` and `@timleslie`.

You will be given the email address of a member of the team, and should email this person with a link to your
solution at least 24 hours before the scheduled technical interview. You're also encouraged to email them with
questions at any time while working on this task.

**Please don't spend more than a few hours on this task**.

It's not a trick question and we're not expecting anything too elaborate. It's a small self-contained exercise to
help us get to know you through your code - how you break down a problem, how you structure your code, and how you
communicate about it with your potential future team-mates.

We'll be looking for well-structured, clear, maintainable code with reasonable performance characteristics.
We will *not* be looking for micro-optimisations or for every single detail to be carefully polished.

## Task Requirements

Given a file containing events like the following:

```json
[
    {
        "EventType": "PatientCreated",
        "Payload": {
            "PatientID": "a30bb29d",
            "Name": "Olivia"
        }
    },
    {
        "EventType": "PatientCaseSlideAttached",
        "Payload": {
            "PatientID": "a30bb29d",
            "File": "d9392a98.tiff"
        }
    },
    {
        "EventType": "PatientCaseSlideAttached",
        "Payload": {
            "PatientID": "a30bb29d",
            "File": "f796f432.tiff"
        }
    },
    {
        "EventType": "PatientCreated",
        "Payload": {
            "PatientID": "e36ff8f4",
            "Name": "Sophie"
        }
    },
    {
        "EventType": "PatientCaseSlideAttached",
        "Payload": {
            "PatientID": "e36ff8f4",
            "File": "ccd803fd.tiff"
        }
    }
]
```

Write a command-line tool that displays the following output:

```
Olivia: d9392a98.tiff, f796f432.tiff
Sophie: ccd803fd.tiff
```

This functionality may be implemented using your choice of **Go**, **Rust**, **Python**, or **JavaScript/TypeScript**, and may use external
open-source libraries if desired.
