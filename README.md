# CF AI Header Guard

An AI-powered web security header analyzer built on Cloudflare Workers AI and KV.
It intelligently fetches and evaluates HTTP response headers, detects CDN and edge anomalies, and produces structured AI-driven security assessments using Llama 3.3.

Deployed link: https://cf-ai-web-security-header-explainer.haleyfchen.workers.dev/

## Features
- Real-time header fetching and analysis
- AI scoring and issue explanations
- Automatic CDN detection and path fallback
- KV caching for fast repeat analysis
- Built with Hono + Workers AI

## Highlights
- Uses Llama 3.3 to classify missing/misconfigured headers with severity (high/medium/low) and rationale.
- Smart fetching: Normalizes URLs, follows redirects, and detects CDN edge or bot-blocked pages.
- Runs entirely on Cloudflare Workers with KV caching and instant cache-bypass refresh.
- Comprehensive checks: Evaluates CSP, HSTS, X-Frame-Options, Referrer-Policy, Permissions-Policy, and cookie security.
- Gracefully manages timeouts, non-HTML responses, and assets (PDFs, images, etc.).
- Hono API + React Router UI + Tailwind + TypeScript.

## Stack
- Cloudflare Workers AI (`@cf/llama-3.3-8b-instruct`)
- KV storage
- Hono.js
- Wrangler for deployment

## Run Locally
```bash
npm install
npm run dev
