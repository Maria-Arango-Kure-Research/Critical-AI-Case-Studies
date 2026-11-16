# Contributing to Critical AI Case Studies

You can contribute a case in another business discipline, adapt an existing case for a different cohort, or improve the notebooks and teaching materials. Use a GitHub issue to share an idea or report a problem. If you have a change ready to review, open a pull request.

## Develop a case

Start with the [case creation guide](templates/CASE_CREATION_GUIDE.md) and the [case template](templates/case-template/). Use the folder for the relevant business discipline. If the discipline is new to the collection, give it a folder and a README that tells instructors where to start.

Explain what critical AI skills the case teaches and what participants will see or do in the notebook that helps them develop those skills. A case might let participants examine what happens when they change a feature, compare a model with a simpler approach, or investigate which errors an overall score hides. Choose an exercise that fits what you want participants to discover.

## Prepare the materials

- `case-materials/` contains the scenario, guided student notebook, discussion questions, and the dataset or instructions for obtaining it. Explain how to set up and run the notebook. Keep the code visible and explain what participants should look for in the outputs.
- `instructor-materials/` contains the teaching notes and annotations. Explain the design choices behind the case, what instructors should look for in the outputs, and how they can use those outputs to guide the discussion.
- `development/` contains the design notes and any scripts or notebooks used to create or adapt the dataset. Record the data source, what you changed, and how another instructor can reproduce the dataset. Include source attribution and licensing with the case.

## Accessibility

Use descriptive headings and link text, and explain what participants need to notice in charts and other visual outputs. When an exercise depends on a chart, provide a short text description or a table of the relevant values. Use labels or patterns as well as colour to distinguish groups.

Document any known accessibility limitations in the case README. If you have a workaround, include it in the setup instructions.

## Submit your contribution

1. Fork this repository to your GitHub account. If you already have write access, you can work directly in this repository.
2. Create a branch from `main` and make your changes on that branch.
3. For a new case or a notebook change, run the notebook from a fresh session using the setup instructions you provide. Check that the instructions lead to the expected data and that the discussion questions refer to outputs participants can see.
4. Commit your changes and push your branch to GitHub.
5. Open a pull request from your branch into `main` in Critical AI Case Studies.

In your pull request, describe what you added or changed and how you checked it. For a new case, describe what participants are meant to learn and include any observations from teaching it, if available.

## How contributions are reviewed

Maria Arango-Kure maintains this repository and decides what to merge. Review takes place in the pull request. The maintainer may ask questions or request changes there. If revisions are requested, push them to the same branch to update the pull request. Once the changes are approved, the maintainer merges them into `main`.

For a new case, review considers whether:

- The activities teach critical AI skills and give participants a way to examine the model's behaviour or evaluate its outputs.
- Another instructor can obtain the data, run the notebook from a fresh session, and understand the teaching choices.
- The discussion questions connect to results participants can investigate in the notebook.
- The materials document data sources, licensing, and known accessibility limitations.

For smaller changes, review focuses on what the pull request changes and how it affects the existing materials.

## Ongoing collaboration

Anyone can propose a contribution through an issue or a pull request. If you’d like to help maintain a case, review contributions, or work on the repository regularly, contact the maintainer and describe what you’d like to take on. The maintainer can invite ongoing collaborators and grant write access where it helps with that work. Collaborators with write access can create branches directly in the repository and submit their changes for review through a pull request.
