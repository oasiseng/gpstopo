# Stripe Integration Guide

GPSTopo uses Stripe to manage online payments for subscription services and
one-time project fees.

## Goals

- Offer secure, PCI-compliant payment processing.
- Automate invoicing and receipt delivery.
- Sync payment status with project management tools.

## Setup Checklist

1. Create a Stripe account with appropriate business verification.
2. Generate restricted API keys for production and test environments.
3. Configure webhook endpoints for `invoice.payment_succeeded`,
   `invoice.payment_failed`, and `customer.subscription.updated` events.
4. Set up products and pricing plans aligned with service tiers.
5. Enable Stripe Tax if delivering services in multiple jurisdictions.

## Integration Steps

- Use Stripe Checkout or Payment Links for rapid deployment.
- Store customer metadata (project ID, contact email) as key-value pairs on the
  customer object.
- Map successful payments to Trello or CRM records using automation workflows.
- Schedule reconciliation reviews to match Stripe payouts with accounting
  software.

## Security & Compliance

- Rotate API keys periodically and restrict access using environment variables.
- Never store full card details on GPSTopo systems.
- Monitor Stripe Radar alerts and dispute notifications promptly.
- Document incident response procedures for suspected fraud.

Following these practices ensures a reliable billing experience for GPSTopo
clients.
