# Reviewly

**Turn happy customers into Google reviews, automatically.**

Reviewly is a web app that helps local businesses collect more online reviews. After a customer visit, Reviewly sends a short, friendly email or text with a direct review link, then tracks who clicked and who still hasn't left a review.

---

## The Problem

Reviews drive new customers for local businesses like salons, dentists, repair shops, and restaurants, but most owners struggle to collect them:

- **They forget to ask**: after a busy day, follow-ups never happen.
- **Asking in person is awkward**: staff feel uncomfortable requesting reviews face to face.
- **The review process is clunky**: customers don't know where to go or can't find the right page.
- **No visibility**: owners can't tell who was asked, who responded, or which requests worked.

The result is a handful of reviews from the few customers who volunteer, while many happy customers never post.

## The Solution

Reviewly makes asking easy and consistent. Add a customer after each visit (or upload a list), and Reviewly sends a friendly request with a one-tap link straight to the business's review page. A simple dashboard shows requests sent, links clicked, and reminders pending.

## Key Features (MVP)

- **Customer entry**: add customers manually in seconds or upload a CSV (name, email, phone, visit date).
- **Review link setup**: paste your Google review link once; Reviewly uses it in every message.
- **Email and SMS requests**: short, personal messages with `{{customer_name}}` and `{{business_name}}` placeholders.
- **Editable templates**: customize wording and tone to match the business.
- **Automatic follow-up**: one gentle reminder a few days later if the link wasn't clicked.
- **Click tracking**: see who opened and clicked the review link.
- **Opt-out handling**: every message includes an unsubscribe option, and opted-out customers are never contacted again.
- **Dashboard**: requests sent, click rate, and customers still pending.

## How It Works

1. **Connect**: paste your Google review link and set up your business name.
2. **Add customers**: enter them after each visit or upload a list.
3. **Send**: Reviewly sends a friendly request by email or text.
4. **Follow up**: a single reminder goes out automatically if there's no click.
5. **Track**: watch click rates and see which customers still haven't responded.

## Target Users

- Salons, barbershops, and spas
- Dentists, clinics, and other appointment-based practices
- Auto repair shops, cleaners, and home service providers
- Small restaurants and cafes
- Any local business that depends on Google reviews

## Important Considerations

- **Review platform rules**: platforms discourage "review gating" (only sending happy customers to the public review page) and incentivized reviews. Reviewly sends the same link to every customer and does not offer rewards for reviews.
- **Message consent**: SMS and email must follow local laws (consent, opt-out, sender identification). Opt-out must be built in from day one.
- **Click tracking, not review tracking**: Reviewly can see link clicks but generally cannot confirm that a review was actually posted.

## Planned Roadmap

**v1.0: MVP**
- Account signup and login
- Business profile and review link setup
- Customer add and CSV import
- Email requests with templates
- One automatic follow-up
- Click tracking and basic dashboard
- Opt-out handling

**v1.1**
- SMS requests
- QR code and short link for in-store use
- Multiple review platforms (Google, Facebook, Yelp)
- Scheduled sending (for example, 2 hours after the visit)

**v2.0**
- Integrations with booking and POS tools
- Multi-location support
- Private feedback form for unhappy customers (kept separate from the public review flow)
- Team accounts and staff leaderboards
- Monthly report of new reviews and rating trend

## Proposed Tech Stack

> Suggestions only; finalize before building.

| Layer | Option |
|---|---|
| Frontend | React / Next.js |
| Backend | Node.js (Next.js API routes) or similar |
| Database | PostgreSQL |
| Auth | Email + password, or a hosted auth provider |
| Email delivery | Transactional email service (Resend, Postmark, or SendGrid) |
| SMS delivery | Twilio or a similar provider (v1.1) |
| Link tracking | Short redirect links with click logging |
| Scheduling | Cron job or queue-based worker for follow-ups |
| Hosting | Vercel / Render / Fly.io |
| Payments (billing) | Stripe |

## Pricing Idea (Draft)

| Plan | Price | Includes |
|---|---|---|
| Free | $0 | Up to 20 requests per month, email only |
| Starter | ~$19/month | 200 requests per month, follow-ups, click tracking |
| Growth | ~$39/month | 1,000 requests per month, SMS, multiple platforms |

## Success Metrics

- Click-through rate on review requests
- Number of requests sent per business per month
- Customers added per active business
- Free-to-paid conversion rate
- Monthly churn

## Open Questions

- Is email enough for the first version, or do local businesses expect SMS from day one?
- What is the easiest way for busy staff to add customers (manual entry, CSV, QR code at checkout)?
- How should SMS costs be passed on to customers in the pricing model?

## Project Status

**Planning stage.** No code has been written yet.

## Getting Started

_Setup instructions will be added once development begins._

## Contributing

_Contribution guidelines to be added._

## License

_To be decided._
