# Platform Flows (v1.0)

This document describes the core user and seller flows for the MVP.

---

## 1. User Flow (Participant)

### 1.1 Entry
- User arrives via Telegram (bot or link)
- User sees short explanation of the platform concept
- User must accept platform rules to continue

---

### 1.2 Browse Listings
- User sees active listings with:
  - item description
  - images
  - token price
  - progress indicator (without revealing target amount)
  - time remaining
  - "Buy Now" option (if available)

---

### 1.3 Buy Participation Tokens
- User selects number of tokens
- User sees:
  - total token cost
  - non-refundable condition after target is reached
  - token-based refund condition if target is not reached
- User confirms purchase
- Crypto payment is made
- Tokens are credited to user's internal balance
- Tokens are locked for the selected listing

---

### 1.4 Waiting State
User status while deal is active:
- tokens are locked
- user cannot cancel or withdraw tokens
- user can track deal progress
- user may purchase additional tokens

---

### 1.5 Deal Outcome — Target NOT Reached
- Sale period ends
- Target amount is not reached
- Locked tokens are returned to user's internal balance
- User can:
  - reuse tokens in another listing
  - withdraw tokens with applicable fees

---

### 1.6 Deal Outcome — Target Reached
- Target amount is reached
- One participant is selected as the item recipient
- All other participants:
  - lose locked tokens
  - receive no refund
- Funds remain locked until delivery confirmation

---

### 1.7 Recipient Flow
If user is selected as recipient:
- User is notified
- User provides delivery details
- User waits for shipment
- User confirms item delivery

---

### 1.8 Funds Release
- After delivery confirmation:
  - seller receives funds
  - platform fee is deducted
- Deal is marked as completed
- No refunds are possible

---

## 2. Seller Flow (Creator)

### 2.1 Seller Registration
- Seller connects via Telegram
- Seller provides:
  - identity details
  - proof of item ownership (if required)
- Seller accepts platform rules

---

### 2.2 Create Listing
Seller creates a new listing by specifying:
- item title and description
- images
- target amount (including all delivery costs)
- token price
- sale duration
- delivery regions
- Buy Now price (optional)

---

### 2.3 Listing Review
- Platform performs basic review
- Listing is published

---

### 2.4 Active Sale
- Seller can:
  - track progress
  - promote listing externally
- Seller cannot:
  - modify target amount
  - cancel sale early

---

### 2.5 Sale Failed
- Target amount not reached
- Listing is closed
- Seller receives no funds

---

### 2.6 Sale Successful
- Target amount reached
- Recipient selected
- Seller ships item
- Seller provides tracking info

---

### 2.7 Payout
- After delivery confirmation:
  - seller receives funds
  - payout is made in cryptocurrency
- Seller can withdraw funds to external wallet

---

## 3. Token & Funds States

### Token States
- Available (user balance)
- Locked (active deal)
- Returned (after failed deal)
- Spent (after successful deal)

---

### Funds States
- Incoming (payment received)
- Locked (escrow)
- Released to seller
- Platform fee collected

---

## 4. Platform Responsibilities
- maintain transaction logic
- lock and unlock tokens
- perform recipient selection
- provide transaction logs
- handle escrow fund flow

---

Draft version. Subject to updates.
