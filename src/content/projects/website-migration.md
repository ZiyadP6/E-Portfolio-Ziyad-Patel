---
title: Mountain Warehouse Website Migration
description: Migrated the Mountain Warehouse storefront from a legacy platform to a modern Next.js stack — covering the commerce layer, CMS, search, and deployment infrastructure.
date: 2026-04-01
tags: [Next.js, TypeScript, BigCommerce, Contentful, Algolia, Vercel]
employer: Mountain Warehouse
featured: true
---

## The project

Mountain Warehouse's old website ran on a legacy platform that had become difficult to develop on and slow for customers. The Web team undertook a full migration to a modern stack:

- **Next.js** for the storefront (App Router, server components)
- **BigCommerce** as the commerce backend — catalogue, pricing, cart, checkout
- **Contentful** for editorial content — landing pages, banners, campaigns
- **Algolia** for search — fast faceted search across the product catalogue
- **Vercel** for hosting and deployment

## My contribution

I joined the Web team after the migration was underway, contributing to:

- Feature work on the Next.js storefront — building and iterating on pages and components
- Working within the Contentful content model to make pages editable by the marketing team without developer involvement
- Bug fixes and performance work as the new site was rolled out

## What's interesting about this stack

The combination of a headless commerce API (BigCommerce), a headless CMS (Contentful), and a dedicated search service (Algolia) is a common pattern at this scale, but making them work together cleanly takes real architecture thought. Each service has its own data model, and the storefront is the layer that stitches them together at request time.
