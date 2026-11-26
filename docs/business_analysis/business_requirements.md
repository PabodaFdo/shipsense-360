# Business Requirements

## BR-01 · Compare shipping performance

The fulfilment manager needs to see the total orders, late orders,
and late-shipping rate for each shipping mode.

Late-shipping rate = late orders ÷ eligible orders × 100.

Eligible orders are orders recorded as shipped late, on time, or early.
Cancelled shipments are excluded from this calculation.

Count each order once, even when it contains several item lines.

### Acceptance criterion

Using an example with four eligible orders and one late order,
the dashboard must show four orders, one late order, and a 25% late rate.

## BR-02 · Estimate outcomes for new orders

The fulfilment manager needs estimated probabilities for three outcomes
when a new order is placed:

- Shipping late.
- Shipping on time or early.
- Shipping cancelled.

These estimates help the manager decide which orders to review.

The prediction must use information available when the order is placed.

### Acceptance criterion

When a user submits valid new-order details, the system displays
a probability for each outcome. Each probability is between 0% and 100%,
and the three probabilities total approximately 100%.