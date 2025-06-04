# SmartMood Tracker for Project Management

Final project for the Building AI course

![Project Status: Prototype](https://img.shields.io/badge/status-prototype-orange)

## Summary

SmartMood Tracker is an AI system that automatically analyzes the tone of work emails and messages to provide insights on the stress level and well-being of project teams.

<img src="immagini/smartmood_tracker_dashboard.png" width="600">

## Background

Problem:
Project management is a high-stress job. Project Managers (PMs) receive and handle hundreds of messages, emails, and requests — often in fast-paced and complex environments.
Chronic stress within teams can lead to:
1) burnout
2) mistakes
3) decreased productivity
4) high employee turnover

Personal motivation:
I am very interested in project management and see stressed colleagues every day. Often the problem becomes visible only when it’s already too late.

Importance:
An AI system that can detect early signs of stress would help managers and HR teams to take proactive actions and improve the overall work climate.

## How is it used?

Context:
For corporate project teams (PM + team members + HR).

Users:
1) Project Managers → can view team stress trends
2) HR → can monitor overall company well-being
3) Team members → can receive personal feedback (if they choose to opt-in)

Affected people:
All team members → special care must be taken regarding consent and privacy.


## Example Code

from transformers import pipeline

sentiment_pipeline = pipeline("sentiment-analysis")

email_text = "I'm very concerned about the project deadlines. We're falling behind."

result = sentiment_pipeline(email_text)

print(result)


## Data sources and AI methods
Data sources:
- Internal emails (anonymized)
- Slack / Teams / work chat messages
- Interaction logs (response times, message frequency)

Data quality:
Privacy must be a top priority → all data must be used ethically and anonymized.

AI techniques:
- NLP (Natural Language Processing)
- Sentiment analysis → positive / negative tone
- Emotion detection (anxiety, frustration, etc.)
- Pre-trained models: BERT, spaCy, HuggingFace Transformers
- Simple classification: stable / attention needed / high risk

Simple demo:
I can implement a basic sentiment analysis demo using sample/mockup email data.

## Challenges

Limitations:
- The tone of messages does not always perfectly reflect the actual emotional state.
- Privacy → data must be handled ethically.
- This does not replace human communication → it is only a support tool.

## What next?

How it could grow:
- Interactive dashboard for HR / PMs
- Analysis of trends over time
- Integration with team feedback systems
- More accurate and personalized models

## Acknowledgments

Use of open-source models (spaCy, HuggingFace Transformers, scikit-learn)

Inspiration from HR Analytics articles and corporate well-being tools

Potential impact: If properly implemented, SmartMood Tracker could provide valuable insights on team well-being and help foster a more positive work environment.
