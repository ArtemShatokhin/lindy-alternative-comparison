# FAQ: questions a team asks when it switches from Lindy

Kortix is the open-source AI Operating System, and it answers the questions a team raises when it moves off a hosted AI teammate priced in credits. Lindy is a hosted service with no self-hosting option on its own pages. Each answer names the product, the mechanism, and where the fact comes from, so a team can check the ones that matter to it.

## Is Kortix a drop-in replacement for Lindy?

Not a like-for-like swap, because the two products sit on different sides of the ownership line. Lindy runs in Lindy's cloud on a credit plan, while Kortix is the open-source AI Operating System you can self-host, with your agents, skills, memory, and connectors in one git repo you own. A team that wants the same job done but the system on its own side moves to Kortix; a team that wants a hosted teammate and no infrastructure stays with Lindy.

## Where do our agents, skills, and memory go?

They become files in a git repo you own. On Kortix, an agent is an `agents/<name>.md` file paired with a governance block in `kortix.yaml`, skills are files, company memory is plain files, and connector configuration is files, all versioned together. Lindy says its memory is "in plain files" you can open and edit, held in your hosted Lindy workspace ([Lindy](https://www.lindy.ai/), checked October 2026). Both products give you files; Kortix puts them in a repository you run.

## Can we run it on our own servers?

Yes. Kortix runs on Kortix Cloud, in your VPC, or on your own on-prem network, and self-host is free. The `kortix self-host` command family installs and runs the full stack on your own infrastructure, with sessions on a sandbox provider of your choosing. Lindy publishes no self-hosting option on its homepage or pricing page, so a switch is what moves the agent layer onto your network. The [setup guide](setup.md) has the path.

## Do we have to change the models we use?

No. Kortix runs any model provider with your own keys, or the ChatGPT plan you already pay for, and a self-hosted instance ships no managed models, so your keys are the path. A hosted service keeps model choice on its side, so Lindy is not something you point at your own keys. Bringing your own keys also means model cost lands on your existing provider account rather than inside a credit meter.

## How do approvals work for an agent's actions?

Kortix has approval gates you set, off until you set them, and you choose allow, ask, or block on each connector action. When an agent finishes a task, its work reaches `main` through a change request, and merge is default-deny for agents, so a person reviews the diff before it lands. Lindy requires approval for actions with outside impact, such as sending, updating, or posting, while read-only lookups run without a prompt (Lindy's own pages). Both stop an agent before an external action; Kortix's stop is a reviewable change request against a repo you own.

## How does the cost compare after we switch?

It depends on seats and consumption under Lindy, and on how you run Kortix. Lindy bills in credits from $29.99 per person per month, with the Team plan quoted "from $49.99 a month for 5,000 credits each," top-ups at "$10 per 1,000 credits," no rollover, and a pause when the pool runs low ([Lindy pricing](https://www.lindy.ai/pricing), checked October 2026). Kortix is free to self-host, and the managed cloud has a free tier at $0 with 200 credits per month and one project, or $40 per seat per month with 2,500 credits per seat, pooled. The [credits arithmetic](lindy-credits-vs-owning.md) works through a team-sized example.

## Do our Lindy credits carry over if we switch?

Lindy's own pages say monthly credits refresh each cycle and do not roll over, so there is no balance that accrues across months to carry. A Kortix repo you own does not run on those credits at all; self-hosting has no credit meter, and the managed cloud runs on Kortix's own free and team plans. Treat the unused part of a Lindy pool as spent at the reset, per Lindy's pages.

## How does the team reach the agents day to day?

Kortix reaches the team where it works: the web, desktop, and mobile apps, the CLI, and Slack or Microsoft Teams, where a message starts a session and follow-ups stay in it. A session runs one agent on its own cloud computer and returns finished work as a change request. So the daily surface is familiar, and what changes is where the work lives and who reviews it before it lands.

For the full head-to-head, see [Kortix vs Lindy](kortix-vs-lindy.md); to run it yourself, see the [setup guide](setup.md). The [README](../README.md) indexes the repository.
