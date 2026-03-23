# Continuous Intelligence

This site provides documentation for this project.
Use the navigation to explore module-specific materials.

## How-To Guide

Many instructions are common to all our projects.

See
[⭐ **Workflow: Apply Example**](https://denisecase.github.io/pro-analytics-02/workflow-b-apply-example-project/)
to get these projects running on your machine.

## Project Documentation Pages (docs/)

- **Home** - this documentation landing page
- **Project Instructions** - instructions specific to this module
- **Your Files** - how to copy the example and create your version
- **Glossary** - project terms and concepts

## Additional Resources

- [Suggested Datasets](https://denisecase.github.io/pro-analytics-02/reference/datasets/cintel/)


## Custom Project

### Dataset
The data set I used focused on adults and their screen time and its effect on sleep and stress level.

### Signals
-I decided to focus on people aged 21 and older, making anyone under 21 an anomaly.
-One of the data points was the number of minutes spent on a screen before bed. I chose to make anything more than 2 hours an anomaly as spending more than 2 hours before bed on a task does not make it a before bed task. It may be the activity you do prior to sleeping, but to me that is too long to qualify as before bed. It is its own action then.
-The third point was if someone slept longer than 10 hours. If an adult is sleeping longer than 10 hours there is usually a distinct cause, like sickness.

### Experiments
Originally, I set the phone usage before bed to 1.5 hours, or 90 minutes. When I did that I got over 4,800 anomalies. I rejected this metric because it would be almost a third of my data, and a third of my data should not be marked as an anomaly as that is too large of a percentage.

### Results
-All of the anomalies were due to age. It found every participate between the ages of 18 and 21. There were no data entires with over 10 hours of sleep nor was there anyone with 120 minutes of time on their phone before bed.

### Interpretation
Even though the original data was 18 and above, the majority were over 21 as well, meaning the data has a nice range of adults.
