---
title: Gift Card Refund System
description: A full-stack feature that lets Customer Service Advisors issue refunds to gift cards instead of the original payment method — built across the React microfrontend, .NET backend, and two integrated services.
date: 2025-06-01
tags: [React, TypeScript, .NET, C#, Microfrontend, REST APIs]
employer: Mountain Warehouse
featured: true
---

## What it does

When a customer returns an item at Mountain Warehouse, advisors previously had only one option: refund to the original payment method. This feature adds a second path — refunding to a Mountain Warehouse gift card instead.

On the surface it's a simple UI choice. Behind it is a chain of integrations: the Customer Service tool (a React microfrontend) needs to call the Order Management System, which needs to call a separate Gift Card Service owned by a different team, and everything needs to be resilient if any part of that chain fails.

## My role

I designed and built the feature end to end:

- **React microfrontend** — added the gift card option to the refund flow in the CS tool, including state management for the new refund type and loading/error states
- **.NET API** — wrote the backend endpoint that handles the refund request, validates the order, and orchestrates the call to the Gift Card Service
- **Cross-team integration** — worked directly with the Gift Card team to understand their API contract and built the integration layer between our OMS and their service
- **Testing** — unit tests for the .NET service layer and component tests for the React side; also covered error scenarios where the Gift Card Service is unavailable

## What I learned

Microfrontend architecture means working within strict contract boundaries — the CS tool is owned separately from the platform it runs on, so changes need careful coordination. This was also my first time working deeply on a cross-team integration where both sides had to agree on the API shape before any code was written.
