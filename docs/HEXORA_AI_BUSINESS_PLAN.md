# HEXORA AI — Business Plan

## Product
HEXORA AI is a planned, Filipino-SME-focused social media marketing workspace. It helps online sellers plan campaigns and prepare publish-ready content without hiring a full marketing team.

This repository currently contains an MSD Digital Finds website. This document records the proposed product direction; it does not claim that an AI service, payment processor, publishing integration, or subscription system is already operational.

## Target customers
- Philippine online sellers and micro/small businesses
- Home-based businesses and service providers
- Freelance social media managers managing several client pages

## Customer problem
Small businesses often struggle to publish consistently, write clear product copy, plan campaigns, and measure what content works. The initial product should reduce content-planning time and make marketing tasks repeatable.

## Initial offer
A self-service content studio with:
1. Business profile and brand voice setup
2. Facebook/Instagram post and caption drafts
3. Hashtag and call-to-action suggestions
4. 7-day and 30-day content calendars
5. Product-description and promotional-copy templates
6. Export to copyable text/CSV; manual approval before publishing

## Proposed pricing for validation
These are hypotheses to test with customers, not active checkout prices:
- Starter: PHP 299/month
- Pro: PHP 599/month
- Business: PHP 999/month
- Agency: PHP 1,999/month

Do not charge customers until the product, terms, support process, privacy notice, refund/cancellation process, and payment flow have been tested.

## Revenue strategy
1. Start with a small paid pilot or done-for-you content service to validate demand.
2. Convert repeated tasks into self-service product features.
3. Offer monthly plans only after customers demonstrate recurring use.
4. Track acquisition cost, active paying customers, churn, support time, AI cost per customer, and gross margin.

## Free-first constraints
- Prefer free development tools and free tiers during validation.
- Do not promise unlimited AI generation.
- Add per-user quotas, request limits, and cost monitoring before enabling paid AI calls.
- Keep AI generation optional behind a provider adapter; provide deterministic demo/mock content for development.
- Do not store provider secrets in Git.

## Trust and safety requirements
- Never publish to a customer's social account without explicit per-account authorization and clear confirmation.
- Do not collect social passwords.
- Use official OAuth/API integrations only when approved and available.
- Keep payment status server-verified; never trust a browser redirect as proof of payment.
- Store the minimum customer data required and provide account/data deletion procedures.
- Keep admin-only operations protected and logged.

## Success criteria for the first pilot
- At least 5 target businesses interviewed
- At least 3 businesses test the workflow
- At least 1 customer agrees to pay for a clearly described pilot
- Users can create, edit, save, and export a content plan without assistance
- Usage limits and estimated AI costs are visible to the owner

## Non-goals for the first release
- Fully autonomous social publishing
- Guaranteed sales, engagement, or revenue claims
- Complex agency/team permissions
- Multi-provider payment orchestration
- Mobile native application

## Current status
Planning baseline only. Features, integrations, pricing, and revenue are not yet verified as implemented or live.
