<center>
# Blockchain Fraud Network Analysis
</center>

## Project Overview
This repository contains a comprehensive data-driven investigation into a blockchain transaction network. The primary objective of this analysis is to uncover money laundering typologies, specifically layering and fan-out structures, and to map the structural hubs utilized by bad actors to obfuscate illicit funds.

By employing advanced network graph analytics, composite risk scoring, and pattern detection algorithms, this project translates raw blockchain transaction data into actionable intelligence for Anti-Money Laundering (AML) and compliance teams.

## Dataset
The data utilized for this network analysis can be accessed here: [https://www.kaggle.com/datasets/ellipticco/elliptic-data-set]

## Repository Contents
This repository contains the following key deliverables:

1. **Jupyter Notebook (PDF)**
   - Contains the complete, fully executed Python workflow.
   - Details the subgraph extraction process (utilizing a 3-hop radius around sampled central nodes to bridge fragmented communities).
   - Includes the programmatic logic used to calculate PageRank and Betweenness Centrality, establish composite risk scores, and detect specific fraud typologies.

2. **Executive Compliance Report**
   - A business-facing summary detailing the highest-risk transaction nodes.
   - Outlines the structural discoveries regarding unlabelled accomplice wallets and provides immediate, actionable recommendations for the transaction monitoring team.

3. **Interactive Dashboard (HTML)**
   - A standalone, full-screen interactive visualization built with Plotly.
   - Features a dynamic network graph highlighting the top 10 central hubs, a time-based transaction volume chart, and a dynamically updating risk ranking table.
   - Includes massive, intuitive side-panel slicers to filter the network by transaction class (Illicit, Licit, Unknown).

## Analytical Methodology
- **Network Mapping:** Constructed a directed graph of transactions, identifying central hubs using exact centrality calculations on a statistically significant structural sample.
- **Typology Detection:** - *Fan-out Patterns:* Flagged nodes receiving from minimal sources but rapidly dispersing funds to a high volume of distinct destinations within a single time step (Placement).
  - *Layering Behavior:* Flagged high-throughput intermediary nodes exhibiting simultaneously high in-degree and out-degree centrality within a condensed timeframe.
- **Risk Scoring:** Developed a normalized composite risk metric weighting PageRank and Betweenness Centrality equally to rank the most structurally critical nodes.

## Usage Instructions
To view the interactive dashboard:
1. Download the `compliance_dashboard.html` file.
2. Open the file in any modern web browser (Google Chrome, Firefox, Edge, Safari). No server or local Python environment is required.
3. Use the toggle buttons on the right-hand panel to filter the network topology, transaction timelines, and risk table by specific entity classes.
