# PRODUCT REQUIREMENTS DOCUMENT

### **Product Overview**

WISP Connect is a USSD-based, pay-as-you-use internet access platform that gives small-scale individuals in the informal sector affordable, reliable internet — purchased and activated instantly, without a smartphone or a monthly commitment.

### **Problem Statement**

Local mwananchi in the informal sector rarely have enough disposable income to commit to standard monthly internet packages. Many who do subscribe end up under-using their data because their days are unpredictable and busy. What they actually need is the ability to buy short, affordable bursts of internet access — an hour, a day exactly when they need it – so their spending matches their actual usage instead of a fixed monthly commitment they may not fully use.
Solution
WISP Connect solves this by letting users dial a USSD code, select a short-duration data package (as little as one hour), pay instantly via M-Pesa, and get connected immediately; no smartphone, app download, or long-term subscription required.

### **Target Users**

Primary Users: Small-scale businesspeople in the informal sector, e.g., boda boda riders, market vendors, and kiosk owners.

### **MVP Scope**

_The MVP will focus on the following core use cases:_

1. Users can register their name and phone number by dialling a USSD code.
2. Users can view available packages.
3. Users can select a preferred package (e.g., 1 hour @ Ksh 10).
4. Users can choose to pay using a different phone number than the one they dialled from.
5. Users receive a confirmation prompt before payment (e.g., "Confirm: 2 hours @ Ksh 20").
6. Users receive a prompt to pay.
7. Users receive a confirmation message once payment succeeds and are connected to the internet.
8. Users can check their existing/active session.

### **Out of Scope**

**_The following are not part of the initial MVP:_**

* UI/UX web page or app
* Admin real-time dashboard
* Daily/monthly income reports
* Loyalty/rewards points system
* Expansion to a B2B model supporting multiple hotspot ISP partners

### **Business Rules**
1. A user must register with their name and phone number before selecting a package.
2. A user must select a package before proceeding to payment.
3. A user must confirm the selected package and price before a payment prompt is sent.
4. A user may choose to pay from a phone number other than the one they dialled from.
5. Payment must be confirmed before network access is granted.

### **Customer User Journeys**

**_Journey 1: New user, standard purchase_**

1. User dials the USSD code.
2. User is presented with the registration menu.
3. User enters name and phone number to proceed.
4. User views available packages.
5. User selects a package.
6. User confirms the selected package and price.
7. User pays for the package.
8. User receives a confirmation message.
9. User receives a success message and is connected to the internet.
10. Session ends.

**_Journey 2: Returning user, checks existing session_**
1. User dials the USSD code.
2. User is presented with the main menu (recognized via phone number).
3. User selects "check existing session."
4. User receives a message showing remaining session time.
5. Session ends.

**_Journey 3: New user, pays with a different number_**
1. User dials the USSD code.
2. User is presented with the registration menu.
3. User enters name and phone number to proceed.
4. User views available packages.
5. User selects a package.
6. User selects "pay with a different number."
7. User enters the alternate M-Pesa number.
8. User confirms the selected package and price.
9. User pays for the package.
10. User receives a confirmation message.
11. User receives a success message and is connected to the internet.
12. Session ends.

### **Product Features**
1. Core features to be built for the MVP, delivered via USSD:
2. Registration (name + phone number)
3. Package listing
4. Package selection and confirmation
5. Pay with a different number
6. Payment prompt (M-Pesa STK push)
7. Payment confirmation handling
8. Success/connection confirmation message
9. Existing session check


