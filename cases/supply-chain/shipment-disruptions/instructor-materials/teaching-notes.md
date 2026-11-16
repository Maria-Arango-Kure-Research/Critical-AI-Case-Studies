# Teaching notes

## Preparation

Choose an environment using the [computing setup guide](../../../../COMPUTING_SETUP.md). Share the [student notebook](../case-materials/student-notebook.ipynb) and [dataset](../case-materials/final_dataset_supply_chain.csv). The notebook uses Python, NumPy, pandas, scikit-learn, matplotlib, and seaborn. Both models run on a CPU.

Run the notebook from a fresh session before class, including the two **Try me** cells. If you plan to run it on one machine and project it, decide where participants will pause to interpret a result or choose what to try next.

## Session plan

Allocate time for each activity based on your group and session. The discussion times in the table come from the notebook.

| Activity | Facilitation |
|---|---|
| Introduce the case and explore the data | Ask what each row represents and what participants notice about the distribution of delays and recorded actions. The notebook gives groups 10 minutes to discuss their observations. |
| Train and evaluate the delay forecast | Use the first **Try me** cell to compare performance with and without the disruption label. The notebook gives groups 15 minutes to discuss the Task 1 results. |
| Train and evaluate the mitigation model | Have participants trace the delay forecast into the second model and examine the confusion matrix and the second **Try me** comparison. The notebook gives groups 15 minutes to discuss the Task 2 results. |
| Close the lab | Invite groups to share a finding and explain how it would inform their decision about adoption. |

The notebook estimates about 30 seconds for package installation, 30–60 seconds to train the delay model, and a few minutes to train the mitigation model. Check the actual runtime in your chosen environment.

For online delivery, paste the relevant discussion questions into the meeting chat before each breakout. Ask groups to note one result that informed their reasoning so they can refer to it in the closing discussion.

The [take-home reflection](../case-materials/questions.md#reflection-assignment-take-home) asks participants to connect a finding to the course, explain a consequential limitation, and give advice to a supply chain professional.
