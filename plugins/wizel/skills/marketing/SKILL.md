---
name: marketing
description: Use Wizel for a Shopify store's email marketing. Use when the user asks how a store, its campaigns or its flows are doing, what is waiting on them this week across their stores or clients, to plan sends, sales or events, to make or change an email, to prepare a client call, or about their brand in Wizel.
---

# Working with Wizel

Wizel plans and makes email marketing for Shopify stores and keeps the record between an agency and its clients. Its tools come from the Wizel connector. You hold the conversation and what the user knows about their business; Wizel holds the stores, the figures, the calendar and the making. Approving, sending for approval, scheduling and publishing happen in Wizel: give the user the link the tool returns.

## Start

1. Call `list_stores` and pick the store the user means; ask when it's unclear. Pass its `public_id` as `store_public_id`, and never mix two stores' figures in one answer.
2. If a tool you need isn't in your list, the connection is read only (`get_profile` shows `access: "read"`). Say so and give the user the Wizel link to finish there.

## Answer what they ask

| They ask | Call |
|---|---|
| What's waiting on me, what's on this week | `get_work_queue`, then `get_portfolio_health` for problems worth a look |
| How did last month go | `get_marketing_period_review`; for more, `get_store_report`, `get_campaign_performance`, `get_flow_performance` |
| What's coming | `get_scheduled_campaigns`, `list_moments`, `get_revenue_forecast`, `get_goal_pacing` |
| What to sell | `get_bestsellers`, `get_brand_products`, `get_product_recommendations` |
| Prepare a client call | `brief_client_call`; afterwards `log_client_meeting` |

Keep the dates, the currency and the period in every answer. Missing data is a gap, not zero.

## Brief Wizel well

Before planning a send, a sale or an event, get these from the user, from their own files or from what you already know about the business. Ask one or two at a time:

- what to push and why now: products, a collection, a launch;
- sale and event dates;
- the offer in the store's exact words. Never guess or invent an offer, a discount, a figure or a claim;
- what to keep out: products, topics, dates;
- how many emails.

Then:

- an event or a sale: `propose_moment`, and follow its date confirmation before `approve_moment`;
- one send: `create_campaign_draft` returns a plan and a link, not an email;
- a planned send on another day: `reschedule_planned_send`, once the user confirms the new day.

## Make or change an email

- New: `get_email_rules`, then `get_brand_kit`, write the email, `save_email`, then `render_email` at 375 and show the user. Give them the builder link.
- New words in an existing email: `get_email`, `edit_words`, then `render_email`.

Never offer the email's HTML: it is published from Wizel.

## Before anything that changes or costs

Say what will happen and wait for a clear yes before creating records, spending credits, replacing a brand document (`set_brand_doc`) or approving an event. Never say something was saved unless the tool said so, and never say an email was sent: nothing here sends one.

## Rhythm

Around the 18th, offer to look at next month's sends and events. Early in the month, offer last month's review with `get_marketing_period_review`.
