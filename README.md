# cintel-02-static-anomalies

[![Python 3.14+](https://img.shields.io/badge/python-3.14%2B-blue?logo=python)](#)
[![MIT](https://img.shields.io/badge/license-see%20LICENSE-yellow.svg)](./LICENSE)

> Professional Python project for continuous intelligence.

Continuous intelligence systems monitor data streams, detect change, and respond in real time.
This course builds those capabilities through working projects.

In the age of generative AI, durable skills are grounded in real work:
setting up a professional environment,
reading and running code,
understanding the logic,
and pushing work to a shared repository.
Each project follows the structure of professional Python projects.
We learn by doing.

## This Project

This project introduces **static anomaly detection**.

The goal is to copy this repository,
set up your environment,
run the example analysis,
and explore how anomalies are identified in static data.

You will run the example pipeline, read the code,
and make small modifications to understand how
the detection logic works.

## Data

The example pipeline reads **pediatric clinic** age and height
data from: `data/clinic_data_case.csv`.
It creates reasonable thresholds and outputs
**anomalies** (data outside the expected threshold).

You'll copy the Python file and make it your own (see docs/your-files.md),
and perform a similar analysis on `data/clinic_data_yourname.csv`
given **adult clinic** age and height data.

## Working Files

You'll work with just these areas:

- **data/** - it starts with the data
- **docs/** - tell the story
- **src/cintel/** - where the magic happens
- **pyproject.toml** - update authorship & links
- **zensical.toml** - update authorship & links

## Instructions

Follow the [step-by-step workflow guide](https://denisecase.github.io/pro-analytics-02/workflow-b-apply-example-project/) to complete:

1. Phase 1. **Start & Run**
2. Phase 2. **Change Authorship**
3. Phase 3. **Read & Understand**
4. Phase 4. **Modify**
5. Phase 5. **Apply**

## Challenges

Challenges are expected.
Sometimes instructions may not quite match your operating system.
When issues occur, share screenshots, error messages, and details about what you tried.
Working through issues is part of implementing professional projects.

## Success

After completing Phase 1. **Start & Run**, you'll have your own GitHub project,
running on your machine, and running the example will print out:

```shell
========================
Pipeline executed successfully!
========================
```

And a new file named `project.log` will appear in the project folder.

## Command Reference

The commands below are used in the workflow guide above.
They are provided here for convenience.

Follow the guide for the **full instructions**.

<details>
<summary>Show command reference</summary>

### In a machine terminal (open in your `Repos` folder)

After you get a copy of this repo in your own GitHub account,
open a machine terminal in your `Repos` folder:

```shell
git clone https://github.com/kehummel/cintel-02-static-anomalies

cd cintel-02-static-anomalies
code .
```

### In a VS Code terminal

```shell
uv self update
uv python pin 3.14
uv sync --extra dev --extra docs --upgrade

uvx pre-commit install
git add -A
uvx pre-commit run --all-files

uv run python -m cintel.anomaly_detector_case

uv run ruff format .
uv run ruff check . --fix
uv run zensical build

git add -A
git commit -m "update"
git push -u origin main
```

</details>

## Notes

- Use the **UP ARROW** and **DOWN ARROW** in the terminal to scroll through past commands.
- Use `CTRL+f` to find (and replace) text within a file.


## Phase 4 Implementation

Since the data was focused on adults, I decided to focus on middle age and late aged adult. I set a minimum age limit of 40 and a maximum age limit of 99, since anyone older than 99 would be an outlier. I set a minimum height of 5 feet (60 inches) as well but there were no anomalies for the height.

There were a total of 8 anomalies; two were above the maximum and 6 were below the minimum.


## Phase 5 Implementation

I found a data set looking at data on adults and their screen time and how it affected their sleep and stress. I marked anomalies as anyone under 21 years old. I marked as an anomaly anyone that spent over 2 hours before bed on their phone. Because if they are spending over two hours on it, it is not before bed. It may be the activity that precedes sleeping, but it is its own activity at that point. I also marked sleeping over 10 hours as an anomaly, because most adults don't sleep 10 hours.

This produced 1,048 anomalies.
