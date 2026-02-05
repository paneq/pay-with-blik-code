---
name: pay-with-blik-code
description: >
  Pay for products or services using BLIK, a Polish mobile payment system.
  Use when the agent needs to complete a payment via BLIK in a browser or mobile app.
  The agent summarizes the order, asks the user for a BLIK code, enters it, and confirms the result.
compatibility: Requires browser or mobile app automation to enter the BLIK code into a payment form.
---

# Pay with BLIK code

## What is BLIK?

BLIK is a Polish mobile payment system. The user opens their banking app and generates a 6-digit one-time code. That code is then entered into a payment form (online store, browser, mobile app) to initiate a transaction. The user then confirms the payment in their banking app via a push notification.

The BLIK code is a **one-time code** — it can only be used for a single transaction and expires in approximately 2 minutes. It is safe for the user to share it in the chat. Even if someone else saw the code, they could not use it without also having access to the user's banking app to approve the transaction.

## Process

### Step 1: Summarize the order

Before asking for the BLIK code, you MUST present ALL of the following to the user:

1. **Products/items** — a clear list of every item being purchased, including quantities
2. **Merchant/platform** — the name of the store, service, or platform where the purchase is being made
3. **Exact total amount** — the precise amount that will be charged, including currency (typically PLN)

Do NOT proceed without all three. If any of them is unclear, investigate first (check the checkout page, cart, etc.).

Example:

```
I'm ready to complete the payment. Here is a summary:

- Merchant: Allegro
- Items:
  - 1x USB-C Cable (29.99 PLN)
  - 2x Screen Protector (15.00 PLN each)
- Total: 59.99 PLN

To proceed, I need your BLIK code.
```

### Step 2: Ask for the BLIK code

Ask the user to open their banking app and generate a fresh BLIK code. Remind them:

- The code is 6 digits
- It expires in about 2 minutes, so they should generate it only when they are ready
- It is a one-time code — safe to share in the chat
- After you submit the code, they will need to confirm the transaction in their banking app

### Step 3: Enter the code and submit

Once the user provides the 6-digit code:

1. Enter the code into the BLIK payment field in the browser or app
2. Submit the payment form
3. Tell the user to **check their banking app now** — they will receive a push notification to approve the transaction

### Step 4: Wait for the user to confirm

You cannot check the user's banking app yourself. After telling them to approve the transaction, you must **wait for the user to respond in the chat**. Ask them to let you know once they have approved (or declined) the payment in their banking app.

Example:

```
I've entered your BLIK code and submitted the payment.
Please open your banking app now — you should see a notification to confirm the payment of 59.99 PLN to Allegro.

Let me know here once you've approved it, and I'll verify the result.
```

Do not proceed until the user replies.

### Step 5: Verify the result

Once the user confirms they approved the payment:

1. Check the payment page for a success message, confirmation screen, or order confirmation
2. Report the result to the user (success or failure)
3. If the payment failed (e.g. code expired, wrong code, user declined), explain what happened and offer to retry from Step 2 with a new code

## Important rules

- NEVER ask for the BLIK code before presenting the full order summary with the exact amount
- If the code expires or payment fails, always ask for a NEW code — never reuse an old one
- Always remind the user to confirm in their banking app after submitting the code
- Be mindful of the ~2 minute expiry window — move quickly between receiving the code and entering it
