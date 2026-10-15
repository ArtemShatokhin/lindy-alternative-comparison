# Lindy credits vs owning the system: the arithmetic

Kortix is the open-source AI Operating System, so you can self-host the stack and bring your own model keys instead of buying credits by the month. Lindy bills in credits, and Lindy's own pages publish the numbers. Those figures imply an arithmetic worth setting against what owning the system costs.

## The numbers Lindy publishes

- **Free:** "$50 in credits for free," no credit card, and the free credits last 7 days.
- **Plans:** Lindy's homepage FAQ says plans "start at $29.99 per user per month," and its pricing page quotes the Team plan "from $49.99 a month for 5,000 credits each."
- **One credit:** the homepage FAQ puts credits at "about a cent each."
- **Top-ups:** "Admins can top up at $10 per 1,000," on both the homepage and the pricing page.
- **Two rules:** monthly credits refresh each cycle and do not roll over, and when the pool runs low "Lindy pauses" until the credits reset.
- **Seats:** every active person is billed. Lindy's FAQ says anyone who signs up, joins the workspace, or @mentions Lindy in Slack takes a seat.

Each quote comes from [lindy.ai](https://www.lindy.ai/) or [the Lindy pricing page](https://www.lindy.ai/pricing), checked October 2026. Run the figures through the same meter and they agree.

## The meter is one cent a credit

```text
$10 / 1,000 credits        = 1.0 cent each
$49.99 / 5,000 credits     = just under 1 cent each
$29.99 / 3,000 credits     = just under 1 cent each
$50 free / 1 cent each     = about 5,000 credits
```

So the top-up rate and the plan rates describe the same meter: roughly one cent per credit. The $50 of free credits is about 5,000 of them, and the Team plan's "5,000 credits each" is about $50 of credit value sold inside a monthly plan.

## What a team actually draws

Two properties of the model shape the monthly total. The pool is shared, so the team's credits are one bucket that everyone draws from. Seats are billed, so the total tracks both how many people are active and how many credits the work consumes.

Take a team of five on the quoted Team plan. If the quoted price is per seat, as the word "each" implies, five seats at the floor come to **$249.95 a month** for a shared pool of **25,000 credits** (5,000 each). That is arithmetic on Lindy's own quoted figures, not a quote from Lindy; check the live page before you buy.

Two more rules from Lindy's pages sit on top of that number. Monthly credits do not roll over, so an unused pool is gone at the reset. And Lindy pauses when the pool runs low, so a busy month is a limit you hit rather than a bill you simply extend.

## What owning the system costs instead

| | Kortix Cloud | Kortix self-hosted |
| --- | --- | --- |
| Platform cost | Free tier at $0; team $40 per seat per month | Free |
| Credits | Free tier 200 per month; team 2,500 per seat per month | None to meter |
| Models | Any model, your own keys | Any model, your own keys |
| Where it runs | Kortix Cloud, your VPC, or on-prem | Your own server |

At five seats, the Kortix Cloud team plan is five times $40, or **$200 a month**, with a pooled **12,500 credits**. Self-hosting the same open-source stack is **$0 in platform fees**, because you bring the machine and the model keys you already pay for. The [setup guide](setup.md) covers what that machine needs.

## Why the meter is the whole argument

Renting a hosted worker prices the work per credit, and the platform underneath stays the vendor's. Owning the system turns a recurring per-credit spend into machines and keys you already control, and it puts the agents, the memory, and the connector configuration into a git repo you own. When a team runs the same work every month, that shift is the difference between a bill that grows with usage and a cost that does not.

The feature side of the same decision is in [Kortix vs Lindy](kortix-vs-lindy.md), the questions a team asks are in the [FAQ](faq.md), and the [README](../README.md) indexes the repository.
