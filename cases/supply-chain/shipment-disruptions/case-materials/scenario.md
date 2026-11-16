# Shipment Disruptions

## Context

You are a supply chain analyst at a mid-sized consumer goods company that ships goods along several international routes:

- Shanghai to Rotterdam via the Suez Canal
- Hamburg to New York across the Atlantic
- Singapore to Los Angeles across the Pacific

Geopolitical conflicts, severe weather, port congestion, and strikes can disrupt shipments. When a delay is likely, the team has to decide how to respond.

| Option | Trade-off |
|---|---|
| Keep the original shipping plan | Avoids the cost of changing the plan, but the shipment may arrive late. |
| Reroute the shipment | Can avoid a disruption, with a change in transit time or cost. |
| Expedite by air | Can shorten transit time at a higher shipping cost. |
| Negotiate with the carrier | May lead to a different arrangement, depending on what the carrier can offer. |

## Task

The company wants to explore what machine learning could contribute to managing disruptions. You’ll train one model on shipment records to forecast delivery delays. You’ll then use those forecasts and examples of past shipping decisions to train a second model that suggests how to respond.

As you work through the notebook, consider how useful the model is, what it misses and what it gets wrong, the data’s limitations, and what business value adopting the models could offer.

## Data

Each row represents one shipment. The records include routes and transport modes, scheduled and actual lead times, recorded disruptions, geopolitical and weather risk indices, shipping costs, and mitigation actions.

The case dataset combines 10,000 rows from Bernardo Mario Uskono’s [Global Supply Chain Disruption & Resilience dataset](https://www.kaggle.com/datasets/bertnardomariouskono/global-supply-chain-disruption-and-resilience) with 40,000 rows generated for the exercise. The source dataset is licensed under [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0).

## Start the case

Follow the [setup instructions](README.md) to open the notebook and load the data.
