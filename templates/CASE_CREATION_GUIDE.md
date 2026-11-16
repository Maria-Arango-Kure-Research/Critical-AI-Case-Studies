# Case Creation Guide

This guide walks you through creating a case for Critical AI Case Studies. Each case gives business students hands-on experience with machine learning and asks them to use what they discover to evaluate the model and its outputs.

## Case structure and naming

Organize cases by business discipline. Give each case its own folder inside the discipline folder, even when it is the first case in that discipline. The discipline README lists the cases available in that discipline. Each case README explains how to prepare and teach that case.

Use the scenario to name the case. For example, **Shipment Disruptions** is the scenario for a supply chain case that includes both delay forecasting and mitigation recommendations. Use the scenario title in the discipline README, the case README, and `scenario.md`. Describe the individual modelling tasks in the case README.

Use lowercase letters and hyphens for discipline and case folder names. For **Shipment Disruptions** in **Supply Chain**, the case path is `supply-chain/shipment-disruptions/`. A second supply chain case would get its own folder alongside `shipment-disruptions/`.

Copy the [case template](case-template/) into `<discipline>/<case-name>/`. Add a relative link to the case in the discipline README, for example `[Shipment Disruptions](shipment-disruptions/)`.

Start with five core components:

| Component | Location within the case folder | What it contains |
|---|---|---|
| Scenario | `case-materials/scenario.md` | The context participants need to understand the data and the modelling task |
| Student notebook | `case-materials/student-notebook.ipynb` | The guided workflow, with visible code, explanations, and discussion prompts |
| Dataset | `case-materials/` | The dataset or instructions for obtaining or generating it |
| Questions | `case-materials/questions.md` | The discussion and reflection questions collected in one place |
| Annotations | `instructor-materials/annotations.md` | Expected findings and guidance for discussing the results |

A complete case may be organized like this:

```text
supply-chain/
├── README.md
└── shipment-disruptions/
    ├── README.md
    ├── case-materials/
    │   ├── README.md
    │   ├── scenario.md
    │   ├── student-notebook.ipynb
    │   ├── shipment-disruptions-dataset.csv
    │   └── questions.md
    ├── instructor-materials/
    │   ├── README.md
    │   ├── annotations.md
    │   ├── teaching-notes.md
    │   ├── codebook.md
    │   └── rubric.md
    └── development/
        ├── README.md
        ├── build-dataset.ipynb
        └── design-notes.md
```

Use the template filenames for documents that serve the same purpose in every case, such as `scenario.md` and `teaching-notes.md`. For a new dataset, use a descriptive filename that includes the case name, such as `shipment-disruptions-dataset.csv`. If an existing notebook already expects a specific filename, use that filename consistently in the notebook, setup instructions, and dataset builder. The data and builder filenames in the example are illustrative.

Include a rubric if the case has an assessed component. If the dataset is hosted elsewhere or generated locally, explain how to obtain it in `case-materials/README.md`.

## 1. Plan the case

Choose the discipline and a modelling task that fits it. Decide what participants should be able to explain after working through the case.

- What parts of the machine learning workflow should participants see for themselves?
- What can they investigate by looking at the data, running the model, or changing a setting?
- What will they use as evidence when explaining what they found?
- What subject knowledge do they need to make sense of the case?

Write a scenario that gives participants enough context to interpret the data and results. Decide how they’ll communicate their findings. A group discussion, written reflection, or short presentation can each work, depending on what you want them to practise.

## 2. Prepare the dataset

Choose or build a dataset that supports the modelling task and gives participants something worth investigating. For example, the data could let them examine how missing labels affect predictions, how a model performs on rare cases, or what happens when an input is unavailable at prediction time.

Record the source, its license, and any changes you made. In the codebook, describe the variables the notebook uses, including units and category definitions where relevant. Use the design notes to explain any patterns you introduced and what they let participants explore.

If you generate or augment the dataset, put the script or notebook in `development/`. Explain how to run it and identify the file it produces. Use the same filename in the student notebook and setup instructions.

## 3. Build the student notebook

Assume participants can reason about the case and may be new to Python. Provide the code they need and keep it visible. Use short explanations alongside the code to show what each step does and which choices affect the result.

A typical sequence is:

1. Set up the environment and load the data.
2. Inspect the dataset before preparing it for modelling.
3. Choose the inputs and the outcome the model will learn to predict.
4. Train the model and evaluate it on held-out data.
5. Interpret the results and discuss their implications.

If you include a **Try me** cell, put it immediately after the result it builds on. Point to the setting participants can change and show the original result alongside the new one. For a model comparison, use the same test cases and metrics where possible so participants can see what the change did.

## 4. Write the questions

Place questions near the outputs they refer to and collect them in `questions.md` for reference. Give participants something specific to examine, such as a feature, a group of errors, or a difference between two results.

Ask them to explain what the evidence supports and where they would need more information. You might ask which errors matter for this task, what a simpler approach could achieve, or what would change their judgment about using the model.

## 5. Write the instructor annotations

Use `annotations.md` to explain what an instructor can expect to see and how to guide the discussion. Include relevant design choices, the outputs that show the patterns participants are investigating, and follow-up questions an instructor can use if a group gets stuck or reaches a different conclusion.

## 6. Prepare the teaching notes

Explain how to set up and facilitate the case. Include prerequisites, suggested timing, where to pause for discussion, and ways to adapt the session. If the case includes assessment, explain how the rubric evaluates participants’ reasoning and use of evidence.

When an exercise depends on a chart, provide a text description or a table of the relevant values. Document known accessibility limitations and any workarounds in the case README.

## 7. Test the case

Start a fresh notebook session and follow the setup instructions as written. Check that the data loads, the notebook runs in order, and participants can find the outputs referred to in the questions. If an experiment is included, check that it can be rerun and that the comparison is easy to read.

If you’ve taught or piloted the case, record observations that would help another instructor prepare for it.

## 8. Submit the case

Follow the pull request process in [CONTRIBUTING.md](../CONTRIBUTING.md). Describe what participants are meant to learn, how the case gives them a chance to learn it, and how you checked the materials.
