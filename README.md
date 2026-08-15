# Contentsquare Website Analytics

## Overview

This portfolio project analyses e-commerce website behaviour using exports from Contentsquare. It combines engagement metrics, page-view data and funnel stages to identify where users progress and where they may encounter friction.

**Workflow:** Contentsquare exports → Python/Pandas → funnel analysis and visualisation → UX recommendations

## Objectives

- Measure overall engagement using sessions, page views and bounce rate.
- Trace progression from the homepage to the cart.
- Calculate stage-level conversion and drop-off.
- Identify a focused UX investigation opportunity.
- Communicate findings with clear visuals and appropriately cautious recommendations.

## Key findings

| Metric | Result |
|---|---:|
| Total sessions | 7 |
| Total page views | 120 |
| Bounce rate | 28.57% |
| Average page views per session | 17.14 |
| Homepage-to-cart conversion | 28.57% |
| Largest funnel drop-off | 3 sessions (60%) at Cart |

Seven sessions began on the homepage; five reached product listing pages, five reached product detail pages, and two reached the cart. The largest observed loss was between product detail pages and the cart. This makes the cart stage the clearest area for follow-up investigation, including cart and checkout usability, navigation and product-information clarity.

Because the dataset contains only seven sessions, these results are **directional rather than statistically representative**. They are intended to guide further investigation, not to make claims about the wider customer population.

## Repository contents

```text
ContentsquareProject/
├── ContentsquareAnalysis.ipynb     # Final analysis, calculations and charts
├── README.md                       # Project context and findings
├── data/                           # Original Contentsquare exports used by the notebook
│   ├── key-performance-metrics.xlsx
│   ├── funnel-dashboard.xlsx
│   └── page-view-segment.xlsx
└── assets/
    └── journey-analysis.png        # Supporting Contentsquare journey export
```

## Data and method

The notebook reads three Contentsquare dashboard exports:

- **Key performance metrics:** sessions and bounce rate.
- **Funnel dashboard:** homepage, product listing, product detail and cart stages.
- **Page-view segment:** total page views.

It uses Python with Pandas for extraction and calculation, and Matplotlib for the funnel charts. Run the notebook from the repository root so its relative `data/` paths resolve correctly.

## Tools

- Contentsquare
- Python
- Pandas
- Matplotlib
- Jupyter Notebook

## AI assistance disclosure

AI was used as an **assistance and validation tool** during this project: to help explain concepts, check the analysis approach and improve the clarity of written documentation. The Contentsquare exports, calculations, analysis decisions and final interpretation were reviewed and completed by the project author. AI was not used to generate the project wholesale or replace understanding of the work.

## Limitations and next steps

The small sample means that a single session materially affects the reported percentages. A useful next step would be to collect more sessions, then investigate the product-detail-to-cart journey and review the cart/checkout experience for possible friction.
