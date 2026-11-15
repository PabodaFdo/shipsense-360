# ShipSense 360 Business Requirements

## Problem statement

In the ShipSense 360 business scenario, the fulfilment team needs
a way to see where shipping delays have occurred and identify new
orders that may need attention before shipment.

## Business objectives

- Help the fulfilment team identify where shipping delays occur.
- Help the team prioritize which new orders to review before shipment.

## BR-01 · Compare late fulfilment by shipping mode

The fulfilment manager needs to see the historical late-fulfilment rate
for each shipping mode to decide which modes to investigate first.

### Acceptance criterion

Given four eligible Standard shipping orders, with one shipped late
and one containing multiple items, when the manager views the shipping
mode comparison, then Standard shows 4 orders, 1 late order, and a
late-fulfilment rate of 25%.

## BR-02 · Flag new orders for review

The fulfilment manager needs to see which new orders are at risk of
shipping late so the team can decide which orders to review first.

The prediction must use only information available when the order
is placed.

### Acceptance criterion

Given a new order with valid checkout details, when the manager submits
it for a prediction, then the app shows a late-shipping probability
between 0% and 100% without asking for the actual shipping date.


## Functional requirements

### FR-01 · Display shipping performance by mode

For each shipping mode, the dashboard must display the number of
eligible orders, the number that shipped late, and the percentage
that shipped late.

Supports BR-01.

### FR-02 · Display a late-shipping risk score

The prediction page must let the user submit a new order using
information available when the order is placed. It must display
the predicted probability of late shipping as a percentage.

Supports BR-02.

## Non-functional requirements

### NFR-01 · Protect customer information

Remove sensitive customer fields from dashboard data, prediction
inputs, and public project files. During data profiling, identify
which fields need to be excluded.