# ShipTrack — Full-Stack Logistics Commerce App

ShipTrack is a production-style e-commerce logistics app built to showcase modern full-stack skills: **Next.js 16 App Router**, **MongoDB/Mongoose**, **NextAuth Credentials + RBAC**, **Stripe Checkout + webhooks**, **BullMQ + Redis** background jobs, and a futuristic UI built with **Tailwind**.

> ✅ This repository contains the full source code.  
> (If showcase-only, replace this line with: “This is a public showcase repo; no source code is included.”)

## Live Demo

- Demo: <ADD-LIVE-DEMO-URL>
- Admin panel: `/admin`
- Notes: Orders are fulfilled automatically after payment (real via Stripe webhooks, or simulated when `STRIPE_DISABLED=true`)

## Key Features

### Storefront

- Product catalog, product details, cart, and checkout
- Stripe Checkout (or demo checkout mode)
- Customer order history

### Admin Control Center

- Products CRUD + inventory fields (as implemented)
- Order management (paid → fulfilled/delivered)
- Basic analytics dashboard (as implemented)

### Platform & Reliability

- Secure auth with **JWT sessions** + **role-based access control**
- Stripe webhooks for payment confirmation and order state updates
- **BullMQ** queue worker for fulfillment + email notifications
- **Vercel Cron fallback** to fulfill paid orders when a worker isn’t running

## Tech Stack

- Next.js 16 (App Router)
- MongoDB + Mongoose
- NextAuth.js (Credentials provider)
- Stripe Checkout + Webhooks
- BullMQ + Redis
- Tailwind CSS + TanStack Query

## Project Structure

All application logic lives in `apps/web`:
