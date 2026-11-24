---
name: get-started
description: Set up Seayora after connecting it. Finds out what kind of account is connected (landlord, property manager, renter, contractor or guest), says what this connection can and cannot do, and offers a first task that fits.
---

# Get started with Seayora

Use this right after the user connects Seayora, or when they ask what Seayora can do for them. Keep it to one short message.

## 1. Find out who is connected

Call `whoami`. It returns the kind of account, the permissions this connection holds and the ones it was not given. Never ask the user for an account id, an email address or a company id: everything is already scoped to the connected account.

## 2. Say what this connection can do, in one or two sentences

- **Guest** (connected without a Seayora account): search homes advertised on Seayora, read a listing in full, check what an area asks in rent, and see when a home can be viewed. Nothing can be changed, and booking a viewing needs a Seayora account.
- **Renter**: what they owe and when it was due, their lease, their repairs, and viewings of advertised homes.
- **Landlord or property manager**: rent owed and paid across their buildings, open repairs, leases and renewals, applications, listings and their books.
- **Contractor**: their jobs, estimates priced from their own past work, sales tax on a job line by line, and how the business is doing.

## 3. Explain once how changes work

Most changes are proposals. Seayora saves them for the account holder to approve, and a result with `staged: true` means nothing has changed yet. Say so plainly and never report a staged change as done. No Seayora tool moves money: rent is paid inside Seayora itself.

## 4. Offer one first task that fits the account

- Landlord or manager: "Which of my units are behind on rent, and what repairs are still open?" (`delinquency_report`, `list_work_orders`)
- Renter: "How much rent do I owe right now?" (`my_home`)
- Contractor: "What sales tax do I charge on a $6,000 boiler replacement in Brooklyn?" (`quote_sales_tax`)
- Guest: "Find me a one-bedroom in Brooklyn under $3,000." (`search_listings`)

Ask which one they want, or let them ask their own question. Do not run every tool during setup.
