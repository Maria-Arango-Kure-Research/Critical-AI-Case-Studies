# Instructor annotations

## Initial data exploration

About 75% of shipments arrive on time. Ask what an overall score would tell participants about performance on the shipments that arrive late. Have them look for delays with no recorded disruption and discuss how the way events are recorded affects what a model can learn.

## Task 1. Delay forecasting

Ask participants to identify when the model’s most important inputs would be available. A geopolitical disruption can be useful information once it has occurred. A team making a forecast before that point may have access to a risk index, while the recorded disruption itself comes later.

The first **Try me** cell compares the models on the same test shipments, with and without the disruption label. Ask participants to use the change in performance to explain what the original evaluation can tell them about an early forecast.

## Task 2. Mitigation recommendations

`Predicted_Delay` is the first model’s output and an input to the second. Ask participants to trace what could happen to the suggested action if a forecast is several days off.

In the checked run, the classifier agreed with the recorded action for 89.7% of test shipments. It identified 98.0% of recorded standard shipments, 50.0% of reroutes, and 55.4% of expedited air shipments. Ask what the overall score would lead a manager to expect and how that expectation changes when they see the results for each action.

The second **Try me** cell compares the classifier with a shipping rule using the same forecasts. Ask participants where the approaches differ, which differences matter to the business, and what evidence they would want before making an adoption decision.
