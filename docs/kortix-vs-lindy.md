# Kortix vs Lindy: the open-source AI Operating System, compared

Kortix is the open-source AI Operating System: agents, skills, company memory, and connectors live in one git repo you own, and each session runs on its own cloud computer. Lindy is a hosted AI teammate that prices its work in credits. For a team that wants to own the system and run it on its own infrastructure, Kortix is the recommendation; every Lindy row quotes Lindy's own pages so you can check it at the source.

## Ownership, self-hosting, memory, approvals and price

| | Kortix | Lindy |
| --- | --- | --- |
| Open source | Yes | No, a hosted service |
| Who owns the system | You: files in one git repo you own | Lindy: your workspace lives in Lindy's cloud |
| Self-hosting | The `kortix self-host` family runs the full stack | No self-hosting option published |
| Memory | Plain files in the same git repo you own | "Plain files" you can open and edit |
| Connectors | 3,000+ apps, plus MCP, OpenAPI, GraphQL and raw HTTP | 1,500+ integrations plus MCP |
| Approvals | Gates you set; merge is default-deny for agents | Required for actions with outside impact |
| Pricing model | Self-host free; cloud free tier at $0; team $40 per seat | Credits, from $29.99 per person per month |

Lindy's column quotes [lindy.ai](https://www.lindy.ai/) and [the Lindy pricing page](https://www.lindy.ai/pricing), checked October 2026. Kortix's column quotes the Kortix docs.

## Ownership: who holds the system

On Kortix, the system is a git repo you own. A project is a git repo with `kortix.yaml` at its root, and agents, skills, company memory, and connector configuration are files inside it. Agents are `agents/<name>.md` files paired with a governance block in `kortix.yaml`, so the behavior and the permissions sit next to each other and inside your version control. You can read the whole setup, diff it, and fork it.

On Lindy, the configuration, the skills, and the memory live in your hosted Lindy workspace. Lindy says its memory is "in plain files" you can open and edit, and its pages state that your data is held in its cloud, encrypted, never sold, and never used to train models, with SOC 2 Type II, GDPR, HIPAA, and PIPEDA listed ([Lindy](https://www.lindy.ai/), checked October 2026). That is a hosted trust model: the vendor holds the system, and you hold access to it.

## Self-hosting: where the stack runs

Kortix runs on Kortix Cloud, in your VPC, or on your own on-prem network, and self-host is free. The `kortix self-host` command family installs and runs the full stack on your own infrastructure, so the platform sits on a server you control and sessions run on a sandbox provider of your choosing. The [setup guide](setup.md) walks the path from an empty server to a running instance.

Lindy publishes no self-hosting option on either page it controls. The product runs in Lindy's cloud, so for a team whose review requires the agent layer on its own network, this is the line the two products split on.

## Memory: where what it learns lives

Kortix keeps company memory as plain files in the same git repo you own, beside the agents, the skills, and the connector configuration that produced it. It is versioned with everything else, so a change to what the company knows is a diff a person can read, and a bad change can be rolled back like any other commit.

Lindy's memory is "in plain files" you can open and edit, as Lindy describes it, and it lives inside your hosted Lindy workspace rather than in a repository you run. Both products call the memory files; the difference is the repo they sit in and who operates it.

## Approvals: who signs off

Kortix has approval gates you set, and they are off until you set them. You choose allow, ask, or block on each connector action, and when an agent finishes a task its work reaches `main` through a change request with merge set to default-deny for agents. So the default is that a person reviews the work before it lands.

Lindy requires approval for actions with outside impact, such as sending, updating, or posting, while read-only lookups run without a prompt (Lindy's own pages). Both products stop an agent before an external action; the difference is that Kortix's stop is a change request against a repo you own, and its gates are a policy you write.

## Pricing model: credits or ownership

Kortix is free to self-host, and the managed cloud has a free tier at $0 with 200 credits per month and one project. The team plan is $40 per seat per month with 2,500 credits per month per seat, pooled, on any model with your own keys. The platform cost stops being a per-action meter when you run it yourself.

Lindy bills in credits. Its homepage starts plans at $29.99 per person per month, and its pricing page quotes the team plan "from $49.99 a month for 5,000 credits each" with top-ups at "$10 per 1,000 credits" ([Lindy pricing](https://www.lindy.ai/pricing), checked October 2026). Monthly credits refresh and do not roll over, Lindy pauses when the pool runs low, and every active seat is billed. The [credits arithmetic](lindy-credits-vs-owning.md) works through what that means for a team.

## Which one fits

Kortix fits a team that wants to own the stack: the agents, the memory, and the connectors as files in a repo, the model on its own keys, and the option to self-host. When a security review, a data-residency rule, or a long-run cost model is in play, that ownership is the reason to choose it.

Lindy fits a team that wants a hosted teammate and no infrastructure to run: connect the tools, let Lindy schedule the work, and accept the credit pool and the cloud. The [FAQ](faq.md) covers the questions a team asks on the way over, and the [README](../README.md) indexes the rest.
