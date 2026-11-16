# Discussion and reflection questions

## Initial data exploration

### 1. The On-Time Reality

Look at the first chart showing the distribution of delays.

- What percentage of shipments arrive on time? Is this good or bad for supply chain operations?
- Here's the challenge: Should we build AI to predict all shipments, or focus on the minority that might be delayed?
- If you were managing this supply chain, where would you invest your resources - monitoring everything or focusing on high-risk shipments?

### 2. The Disruptions

The second chart shows different disruption types cause very different delays.

- Which disruption type causes the longest delays? Which causes the shortest? Why might that be?
- Notice the "No Disruption" category - does it have any outliers with significant delays? What could cause delays when there's no official disruption event?
- If we only look at disruption labels, we miss those unlabeled delays. What other signals might predict them?

### 3. The Risk Index Pattern

The bubble chart shows the relationship between risk indices and delays.

- Do you see a pattern? What happens when both geopolitical risk and weather severity are high?
- Are there any high-risk shipments that still arrived on time? What might explain that?
- Do you think the AI can learn this pattern?

### 4. Mitigation Decisions

Look at the chart showing mitigation actions taken.

- Which mitigation action is most common? Why?
- Air freight costs significantly more than sea freight. When is that cost justified?
- If you're choosing between "absorb a delay" vs. "pay premium to expedite," what factors matter?
- Can AI learn to make these cost-benefit decisions? Should it?

### 5. The Class Imbalance Problem

Look back at the delay distribution chart.

- Most shipments are in one category (on-time), fewer in another (delayed). What percentage split do you see?
- If you train an AI on this data, what will it probably learn?
  *(Hint: "Just predict everything is on-time" gives you the majority percentage as accuracy!)*
- This is called **class imbalance** - it's a major challenge in real-world AI
- What if our historical data only logged some disruptions? How would missing data affect what the AI learns?

### 6. Looking Ahead to Tasks 1 & 2

Based on what you've seen in these charts, make predictions:

1. Which features will matter most for predicting delays? (Task 1)
2. Will the AI rely too heavily on disruption labels, or will it learn from risk indices and routes too?
3. For recommending mitigation actions (Task 2), what should the AI optimize for - speed? cost? customer satisfaction?

**Write down your predictions.** We'll test them when we build the models.

## Task 1. Delay forecasting

### 1. Model Performance

Look at your R² score and MAE.

- Is this performance good enough to deploy? What's your threshold?
- Most shipments arrive on time - could the model just be learning "predict near zero most of the time"?
- What would convince you this model is actually useful versus just fitting noise?

### 2. Feature Importance

Look at which features drive predictions.

- Which feature dominates? Is this what you expected?
- What's the split between "what actually happened" (disruption labels) versus "what we could predict beforehand" (risk signals)?
- If one feature accounts for most predictions, is this a robust model or a fragile one?

### 3. Production Reality

Think about when you'd actually use this model.

- When do you need delay predictions? Before shipments leave, or after problems occur?
- When do you get disruption labels? Before delays or after?
- What happens to your model's accuracy if you remove features that aren't available when you need predictions?

### 4. Causation vs. Correlation

The model learned statistical patterns in historical data.

- Does the model understand WHY disruptions cause delays? Or just THAT they correlate?
- What happens when a new type of disruption emerges that wasn't in the training data?
- Can pattern-matching replace domain expertise about supply chain dynamics?

### 5. Deployment Decision

You have accuracy metrics and feature importance. Now what?

- Would you deploy this model in production? Why or why not?
- What questions would you ask before putting this in front of real customers?
- What could go wrong if this model makes bad predictions? Who bears the cost?

## Task 2. Mitigation recommendations

### 1. The Confusion Matrix

Look at where the model makes correct predictions versus mistakes.

- Does the model perform equally well on all three actions, or is it biased?
- If it's biased toward one action, why? (Hint: look at the training data distribution)
- Which type of mistake is more costly: recommending unnecessary action (waste money) or missing urgent action (lose customer)?

### 2. Predicted Delay Dominance

Look at feature importance for Task 2.

- How much does Task 2 rely on Task 1's predictions?
- What happens if Task 1 predicts 3 days but actual delay is 8 days? Will Task 2 recommend the right action?
- This is called error propagation - mistakes cascade through pipelines. How do you prevent this?

### 3. What Else Matters?

Look beyond the top feature.

- After predicted delay, what drives recommendations? Product type? Cost? Risk?
- Why might disruption type have low importance in Task 2 when it had high importance in Task 1?
- Are there critical business factors the model doesn't know about? (Customer relationships, contracts, budget constraints)

### 4. Learning from History

Task 2 learned from past manager decisions.

- What if historical decisions were inconsistent, budget-driven, or biased?
- Can an AI trained on past decisions make BETTER decisions than those past managers?
- If you wanted recommendations better than historical patterns, what would you need?

### 5. Assistive vs. Operational

You have a model that recommends actions. Now what?

- Should managers trust these recommendations blindly? Review all of them? Only review certain types?
- For which action type does the model perform best? Worst? How should that affect trust?
- What would need to change to make this fully Operational instead of assistive?

## Reflection assignment (take-home)

After today's session, take time to process what you experienced. Write a short reflection (1-2 pages) responding to the three prompts below.

This is not a recap of what happened — the discussion already covered the case specifics. This is about what you take away from the experience and how it connects to what you've been learning in this course.

### 1. What Surprised You?

Identify **one specific finding** from today's work that surprised you about how the AI models performed. Don't just say "the model wasn't perfect" — point to something concrete (a metric, a chart, a feature importance ranking, a pattern in the confusion matrix) and explain why it surprised you.

Then connect it to a concept from this course. How does what you found relate to something we've discussed in class?

### 2. What's the Limitation That Matters Most?

Of all the limitations you identified today — across both tasks — which one would matter most if this system were deployed in an actual supply chain operation?

Explain why with reference to specific evidence from your analysis. Think about: Who gets affected? What decisions go wrong? What's the cost of the failure?

### 3. What Would a Supply Chain Professional Need to Know?

Imagine your company is considering deploying AI tools like the ones you built today. A supply chain manager — smart, experienced, but not technical — asks you: "What do I need to understand about AI to use it well?"

What would you tell them? Be specific. Go beyond "AI isn't perfect" or "always verify the outputs." What concrete understanding would help them make better decisions about when to trust AI, when to question it, and when to override it?
