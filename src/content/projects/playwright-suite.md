---
title: Playwright Automation Suite — Supplier Portal
description: A comprehensive end-to-end test suite covering every page of the Supplier Portal, using mocked API responses to keep tests fast, deterministic, and independent of external services.
date: 2025-01-01
tags: [Playwright, TypeScript, Testing, Mock APIs, E2E]
employer: Mountain Warehouse
featured: true
---

## Background

The FinDev team was building a new Supplier Portal — an internal tool for suppliers to manage their product data and orders. As the portal grew, manually testing every path became impractical. I was tasked with building out a proper automated test suite.

## What I built

A full Playwright suite that covers every page and user journey in the portal:

- **Page coverage** — tests for every route in the app: list views, detail pages, forms, modals, and error states
- **Mock API layer** — rather than hitting real API endpoints (which would be slow, flaky, and require test data management), all external calls are intercepted and responded to with fixture data. This means tests run fast and produce the same result every time, regardless of what's in the database
- **Reusable helpers** — shared setup for auth, navigation, and common UI patterns to keep individual test files clean
- **CI integration** — the suite runs on every pull request

## Why mocking matters

E2E tests that depend on real APIs tend to break for reasons unrelated to the code under test — a flaky upstream service, missing test data, rate limits. Mocking at the network level gives you the speed and isolation of unit tests with the coverage of real browser automation.

## Tech

TypeScript throughout. Playwright's `route` API handles the request interception. Fixtures are stored as JSON alongside the tests.
