# pay-with-blik-code

An [Agent Skill](https://agentskills.io/) for paying with BLIK — a Polish mobile payment system.

## What is BLIK?

BLIK lets you pay by generating a 6-digit one-time code in your banking app. The code is entered into a payment form (online store, browser, app) and then confirmed in the banking app. The code expires in ~2 minutes and can only be used once, making it safe to share in a chat with an AI agent.

## What does this skill do?

It guides an AI agent through the process of completing a BLIK payment collaboratively with a human user:

1. The agent summarizes the order (products, merchant, exact amount)
2. The agent asks the user for a BLIK code
3. The agent enters the code and submits the payment
4. The user confirms the transaction in their banking app and lets the agent know
5. The agent verifies the result

## Usage

Follow the [Agent Skills installation instructions](https://agentskills.io/) for your agent platform to add this skill.
