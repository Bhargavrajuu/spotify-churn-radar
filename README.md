# Spotify Churn Radar

AI solution 02 of 14 · Marketing · built for **Spotify**

Prepared by **K Bhargav Raju**.

## Problem statement

A subscription business is experiencing increasing customer churn despite continued marketing expenditure. Develop an AI system that identifies behavioral patterns associated with churn, segments at-risk customers, determines potential causes, and generates personalized retention strategies.

## Why Spotify

Spotify runs on monthly subscriptions and competes with Apple Music and YouTube Music for the same listeners. This tool scores every subscriber for churn risk, explains why, and assigns a retention play.

## Algorithm

1. **Collect subscriber data**: Listening, skips, logins, billing, plan, support tickets, reviews
2. **Engineer behaviour features**: Change in weekly listening, days since login, failed payments
3. **Train churn classifier**: Logistic regression, 70/30 split, class-weighted
4. **Explain each user**: Per-user feature contributions (SHAP-style) and global drivers
5. **Time to churn**: Monthly hazard turned into expected months until cancel
6. **Segment at-risk users**: Group by each user's top churn driver
7. **Text signals**: Keyword sentiment on reviews and tickets
8. **Retention plays**: Rules + AI analyst pick an action per segment

## Data

3,000 Premium subscribers with 90 days of listening, billing and support history, scaled 2,000x to a 6M-subscriber market (sample data). All figures are illustrative and are not Spotify's actual numbers.

## How to use

Open `index.html` in any web browser. No installation is needed; the whole tool is one self-contained file.

The controls panel lets you change at-risk threshold, expected save rate of plays, and the analysis reruns instantly. "New sample data" generates a fresh dataset.

## AI analyst panel

The "Ask the AI analyst" panel answers questions about the results in plain English through Claude. It works when the page is opened as a Claude artifact on claude.ai. Opened from GitHub, GitHub Pages or a local folder, all the models, charts and controls still run, and the panel shows that it is unavailable.
