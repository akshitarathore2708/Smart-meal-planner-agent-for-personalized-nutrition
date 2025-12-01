# Smart-meal-planner-agent-for-personalized-nutrition
The Smart Meal Planner Agent is an AI-powered nutrition and diet-planning assistant designed to help users create personalized daily and weekly meal plans based on their goals, dietary preferences, and nutritional needs. The purpose of this capstone project is to demonstrate how a generative, tool-augmented, multi-turn AI agent can solve a problem.
Problem Statement

Planning healthy meals every day is difficult for most people. The biggest challenges users face include:

Not knowing what to cook or eat based on their health goals

Difficulty balancing macronutrients (protein, carbs, fats)

Time wasted searching recipes

Managing allergies and dietary restrictions

Lack of clear portion guidance

Difficulty staying consistent with a fitness or weight-loss plan


These challenges make nutrition planning overwhelming, especially for beginners. Traditional diet apps rely on static templates and do not adapt dynamically to users’ goals or changing needs.

The Smart Meal Planner Agent solves this by using generative AI to create fully personalized meal plans, adjusting portion sizes, calories, and ingredients based on user inputs.


---

🔹 Why Agents?

AI agents are the right solution because they provide:

1. Multi-turn conversation

The agent can remember the user’s preferences across turns:

“I am vegetarian.”

“I want 2000 calories per day.”

“Avoid peanuts, I’m allergic.”


2. Tool-based reasoning

Instead of free-text hallucination, the agent uses:

A nutrition lookup tool

A recipe generation tool

A calorie calculation tool

A grocery list generator


3. Real-time dynamic updates

If the user changes a requirement:

> “Reduce the carbs and increase protein.”



The agent recalculates the whole meal plan instantly.

4. Personalization at scale

Using user history, preferences, and context, agents create unique diet plans for each individual.

This adaptability and intelligence make LLM-based agents ideal for building a smart concierge-style meal planner.


---

🔹 What I Created — Architecture Overview

The Smart Meal Planner Agent follows a clean, modular architecture built on Google Cloud:


---

1. User Interface

A simple chat-based frontend where users can:

Ask for meal plans

Modify diet goals

Request recipes or grocery lists


The demo in the YouTube video shows this interface clearly.


---

2. Vertex AI Agent Builder (Core Brain)

This is the heart of the system.

The LLM handles:

Understanding user intent

Multi-turn context

Calling tools

Summarizing nutrition information

Generating recipes and meal plans

Ensuring personalization


The agent is grounded in structured data to avoid hallucinations.


---

3. Tools / Functions (Python Cloud Functions)

The agent uses multiple tools:

✔ Nutrition Data Tool

Fetches calories, macros, and micronutrients for ingredients.

✔ Recipe Generator Tool

Creates healthy recipes based on:

Calories

Diet type (Veg, Non-veg, Vegan)

Cooking difficulty

Ingredients available


✔ Calorie Calculator Tool

Calculates:

Total daily calories

Per-meal distribution

Protein, carbs, fat breakdowns


✔ Grocery List Tool

Compiles:

Ingredients

Quantities

Weekly shopping list


Each tool returns structured JSON that the agent uses to produce the final output.


---

4. Nutrition Database

A curated dataset containing:

Common foods and Indian recipes

Macros and calories

Healthy replacements for each ingredient


The agent queries this to maintain accuracy.


---

5. Logging + Monitoring

All conversations and tool interactions are logged in:

BigQuery (structured logs)

Cloud Monitoring (latency + error detection)


This ensures the agent works reliably and can be improved over time.
