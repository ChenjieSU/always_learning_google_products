# always_learning_google_assistant/GLOSSARY.md

This file contains paraphrased definitions of key terms learned in the google code labs.

# Glossary

## 1. From the Build Actions for the Google Assistant (Level 1) Code Lab

For more information, see `02-build_actions-code_lab-level_1`

### 1.1: Overview: None

### 1.2: Understand how it works

- Action: entry point into an interaction
- Intent: underlying goal or task the user wants to accomplish
- Fulfillment: logic that handles an intent and executes the appropriate Action

### 1.3: Setup

- Actions project: allows managing, testing, and publishing a set of Actions
- Actions Console: a web-based console allowing developers to create, maintain, test, and publish a set of Actions
- Dialogflow: web-based service containing an agent that processes input spoken by the user
- NLU: Natural Language Understanding, the ability to understand and parse input spoken by the user

### 1.4: Starting a conversation: None

### 1.5: Create conversational responses

- Parameters (Dialogflow): values that Dialogflow parses from user input
- Dialogflow intent: maps user input to the agent's static or dynamic response
- Dialogflow webhook (fulfillment): code for handling intents and returning a dynamic response to the user
- Training phrase (Dialogflow): examples of user input used to train the model and match future inputs
- Entities (Dialogflow): a category of things, such as colors or dates

### 1.6: Implement a webhook: None

### 1.7: Next steps: None

## 2. From the Build Actions for the Google Assistant (Level 2) Code Lab

For more information, see `03-build_actions-code_lab-level_2`

### 2.1: Overview: None

### 2.2. Install the Firebase command-line interface: None

### 2.3. Set up for local development

- Cloud Functions for Firebase: develop actions locally, use Firebase CLI to run them in a managed environment

### 2.4. Add a deep link to your Action

- Explicit invocation: users speak the Action name to invoke the app; may specify a deep link (specific task)
- Implicit invocation: users invoke the app 'based on various signals' and google gives them a choice of Actions

### 2.5: Personalize your responses with helper intents

- Helper intents: can return information that might be requested frequently, e.g., user's name, location, permissions, etc.

### 2.6: Add audio effects with SSML

- Speech Synthesis Markup Language (SSML): markup language giving additional control over how speech is generated




