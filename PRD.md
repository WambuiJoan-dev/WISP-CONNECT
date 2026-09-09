PRODUCT REQUIREMENTS DOCUMENT

**Product Overview**
WISP Connect is a USSD-based, pay-as-you-use internet access platform that gives small-scale individuals in the informal sector affordable, reliable internet — purchased and activated instantly, without a smartphone or a monthly commitment.

**Problem Statement**
Local mwananchi in the informal sector rarely have enough disposable income to commit to standard monthly internet packages. Many who do subscribe end up under-using their data because their days are unpredictable and busy. What they actually need is the ability to buy short, affordable bursts of internet access — an hour, a day exactly when they need it – so their spending matches their actual usage instead of a fixed monthly commitment they may not fully use.
Solution
WISP Connect solves this by letting users dial a USSD code, select a short-duration data package (as little as one hour), pay instantly via M-Pesa, and get connected immediately; no smartphone, app download, or long-term subscription required.

**Target Users**
Primary Users: Small-scale businesspeople in the informal sector, e.g., boda boda riders, market vendors, and kiosk owners.

**MVP Scope**
The MVP will focus on the following core use cases:

Users can register their name and phone number by dialling a USSD code.
Users can view available packages.
Users can select a preferred package (e.g., 1 hour @ Ksh 10).

Users can choose to pay using a different phone number than the one they dialled from.

Users receive a confirmation prompt before payment (e.g., "Confirm: 2 hours @ Ksh 20").

Users receive a prompt to pay.

Users receive a confirmation message once payment succeeds and are connected to the internet.

Users can check their existing/active session.

**Out of Scope**
_The following are not part of the initial MVP:_

* UI/UX web page or app
* Admin real-time dashboard
* Daily/monthly income reports
* Loyalty/rewards points system
* Expansion to a B2B model supporting multiple hotspot ISP partners

**Business Rules**
A user must register with their name and phone number before selecting a package.
A user must select a package before proceeding to payment.
A user must confirm the selected package and price before a payment prompt is sent.
A user may choose to pay from a phone number other than the one they dialled from.
Payment must be confirmed before network access is granted.

**Customer User Journeys**
**_Journey 1: New user, standard purchase_**
User dials the USSD code.
User is presented with the registration menu.
User enters name and phone number to proceed.
User views available packages.
User selects a package.
User confirms the selected package and price.
User pays for the package.
User receives a confirmation message.
User receives a success message and is connected to the internet.
Session ends.
Journey 2: Returning user, checks existing session
User dials the USSD code.
User is presented with the main menu (recognized via phone number).
User selects "check existing session."
User receives a message showing remaining session time.
Session ends.
Journey 3: New user, pays with a different number
User dials the USSD code.
User is presented with the registration menu.
User enters name and phone number to proceed.
User views available packages.
User selects a package.
User selects "pay with a different number."
User enters the alternate M-Pesa number.
User confirms the selected package and price.
User pays for the package.
User receives a confirmation message.
User receives a success message and is connected to the internet.
Session ends.
Product Features
Core features to be built for the MVP, delivered via USSD:
Registration (name + phone number)
Package listing
Package selection and confirmation
Pay with a different number
Payment prompt (M-Pesa STK push)
Payment confirmation handling
Success/connection confirmation message
Existing session check


