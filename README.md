# SNACKED

A web app where customers reserve lunch snacks before the lunch period and pay at pickup. Admins manage stock and orders from a dashboard.

**Status:** built, working version. The source code is not uploaded yet (it's being cleaned up first). Write-up: https://abhiraajr.github.io/projects/snacked.html

## How it works
- One web address routes people: admins go to the dashboard, customers with an order go to the edit-order page, everyone else sees the storefront.
- Reserving a snack lowers its stock, cancelling puts it back, marking an order as bought finalizes it.
- Each order is tied to the customer's signed-in Google account, limited to one of each snack per order.
- Admins can restock, delete orders and preview the customer view.

## Stack
Google Apps Script (server and HTML pages), Supabase (database), JavaScript.

## What I learned
- Admin access has to be tested with the real admin account after every deploy.
- Stock updates need a lock, or two people can take the last item.
- Secrets belong in script properties, never in code.

Author: Abhiraaj Rampal
