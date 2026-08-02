# Nutrition AI Agent — Dietify tech

**Domain:** Nutrition & Diet Assistant
**Team:** Om Choudhari (Lead), Atharva Dhanraj Gawande, Vaishnavi Komalwar, Ojaswi Chakole, Nakul Gopal Dwivedi

## Problem
Generic diet advice ignores individual goals, allergies, budget, and local food availability, so people abandon manual calorie/macro tracking within weeks. Dietitians are expensive (₹500–₹2,000/session) and unavailable at the moment a food choice is actually made.

## What this agent does
The user describes a meal in plain language (e.g. *"grabbed a peanut butter toast for breakfast"*). The agent:
1. **Perceives** — matches the description to a food/nutrition database
2. **Decides** — checks the food against the user's allergies, diet type (vegan/vegetarian), budget tier, and daily calorie goal
3. **Acts** — returns an instant ✅ / ⚠️ verdict, and if something's a bad fit, suggests a real alternative from the database with a similar calorie count

This directly answers the "conversational meal logging + budget- and availability-aware recommendations" differentiator from our pitch.

## Run it
```bash
pip install -r requirements.txt
jupyter notebook agent.ipynb
```
Or open `agent.ipynb` in Google Colab and run all cells — no API key required for the base demo (rule-based responses). To enable Claude-generated natural-language replies, set the `ANTHROPIC_API_KEY` environment variable before running.

## Project structure
```
AI-Agent-Project/
├── README.md
├── agent.ipynb
├── requirements.txt
├── data/
│   └── sample_food_data.csv
└── screenshots/
```

## Status & next steps
This is an MVP built for Day 2 of the hackathon. Known limitations and planned next steps are documented in the final cell of `agent.ipynb` (better food matching via NLP/embeddings, a full USDA/Edamam database, persistence, and photo-based meal logging).
