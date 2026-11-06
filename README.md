# greencloud vps pricing: What Each Plan Actually Costs, APAC vs US/EU Traffic Differences, and How to Pick the Right Tier

GreenCloud's Ryzen KVM line starts at **$6/month** for 1 vCPU, 1 GB RAM and 15 GB NVMe storage, and tops out at $80/month for 8 cores and 16 GB. Everything on this line is billed month to month, so the price you sign up at is the price you keep paying — there's no separate renewal rate hiding further down the checkout page. The detail most comparison posts skip: the same plan costs the same in Asia-Pacific and US/EU datacenters, but the APAC versions carry roughly half the monthly traffic allowance, and buying that traffic back afterwards costs five times more per gigabyte in Asia than in the US or Europe.

Before the full breakdown, the short version for anyone who just wants to order:

> **Quick verdict:** For most individual users — a personal site, a proxy, a dev box — the **RyzenKVM-2 at $10/mo** (2 GB RAM, 30 GB NVMe) is the sensible entry point. The $6 plan works for lightweight stuff, but 1 GB fills up fast once you add a panel. **[👉 Check current Ryzen KVM plan availability](https://greencloudvps.com/billing/aff.php?aff=6679)**

## The full Ryzen KVM price list

GreenCloud's flagship line runs Ryzen cores at 3.5+ GHz with NVMe storage and a 10 Gbps port as standard, with IPv6 included by default. Five tiers, Linux only, identical prices in every region.

| Plan | CPU / RAM | NVMe | Traffic (APAC / US-EU) | Price | Order |
| --- | --- | --- | --- | --- | --- |
| RyzenKVM-1 | 1 core / 1 GB | 15 GB | 750 GB / 1.5 TB | $6/mo | [ Order RyzenKVM-1](https://greencloudvps.com/billing/aff.php?aff=6679) |
| RyzenKVM-2 | 1 core / 2 GB | 30 GB | 1 TB / 2 TB | $10/mo | [ Order RyzenKVM-2](https://greencloudvps.com/billing/aff.php?aff=6679) |
| RyzenKVM-3 | 2 cores / 4 GB | 50 GB | 2 TB / 4 TB | $20/mo | [ Order RyzenKVM-3](https://greencloudvps.com/billing/aff.php?aff=6679) |
| RyzenKVM-4 | 4 cores / 8 GB | 80 GB | 4 TB / 8 TB | $40/mo | [ Order RyzenKVM-4](https://greencloudvps.com/billing/aff.php?aff=6679) |
| RyzenKVM-5 | 8 cores / 16 GB | 150 GB | 6 TB / 12 TB | $80/mo | [ Order RyzenKVM-5](https://greencloudvps.com/billing/aff.php?aff=6679) |

The APAC row covers Singapore, Japan, Hong Kong and Vietnam. US/EU locations get double the traffic at every tier for the same money — 1.5 TB versus 750 GB on the entry plan, 12 TB versus 6 TB at the top. That's the most useful thing to understand about GreenCloud's pricing structure: bandwidth into and out of Asian datacenters costs more to provision, so the company prices it into a lower allowance rather than a higher bill. If your users are global and your traffic is heavy, a US or EU location is simply better value.

The network behind these plans is worth a sentence too. GreenCloud owns its hardware outright and operates 30 locations across 4 continents, with Tier-1 carriers including NTT, IIJ, Softbank, Telstra and Arelion on a 600+ Gbps aggregate backbone. For anyone choosing an APAC location, that carrier list matters more than the marketing numbers — it's why the Tokyo and Hong Kong nodes can offer direct peering options that cheaper US-only hosts can't.

The price steps are easy to plan around. Each tier doubles the previous one — $6 to $10 doubles RAM and storage, $10 to $20 adds a second core on top of that, then $40 and $80 keep doubling. When you outgrow a tier, the next one costs exactly 2x.

## Paid add-ons: how the upgrades actually work

You don't have to switch tiers to get more resources. GreenCloud sells à la carte upgrades at **$3 per extra 1 GB of RAM, $3 per extra CPU core, and $3 per extra 10 GB of SSD**, billed monthly alongside the plan.

There's a cap, and it's the part people miss: you can add at most an amount equal to the plan's original configuration. A 4 GB plan can grow to 8 GB maximum, and the same rule applies to cores and storage. Upgrades also depend on spare capacity on your actual host node, so they're not guaranteed to be available at any given moment. If you expect to need double the RAM within a few months, jumping to the next tier usually works out the same per GB anyway — the add-ons mainly make sense for short-term, modest bumps.

Overage traffic is a different story, and it's asymmetric. If you burn through your allowance, extra bandwidth on a US/EU KVM plan costs **$3/TB per month**; on APAC plans it's **$15/TB per month**. On a 10 Gbps port the rate is $4/TB. That's the clearest illustration of the APAC premium: a $6 plan in Los Angeles can top up traffic for $3 a terabyte, while the same plan in Singapore costs five times that. Anyone running a bandwidth-heavy proxy in Asia should budget for this before ordering, or pick the US/EU location instead.

## The other lines: Budget KVM, Windows, and everything else

Ryzen KVM is only one product line. GreenCloud's catalog is genuinely large — one tracking site listed 234 active plans across the company's lines — so here are the entry points that matter for most buyers:

- **Budget KVM / SSD KVM** — the cheaper sibling of the Ryzen line. Same five-tier structure, same $6/$10/$20/$40/$80 monthly prices, but storage is RAID-10 SATA SSD instead of NVMe. US/EU traffic matches the Ryzen line (1.5 TB up to 12 TB); APAC gets the halved allowances. Each plan includes one free backup/snapshot slot. A budget annual option has been advertised in the past at roughly **$25/year for a 2 GB RAM plan** in the New York location, per a third-party comparison — treat that as a historically advertised price rather than a guaranteed current listing, and check the store for what's actually on sale.
- **Budget Windows VPS** — Windows Server 2022 with RDP, unmetered bandwidth on 1 Gbps, **from $8/month**. Stepping up the config gets expensive quickly: the 5 GB RAM / 5 core class runs about **$40/month**, five times the entry price.
- **Specialty lines** — Storage KVM VPS for cheap bulk disk, Forex VPS for trading platforms, macOS VPS on Mac Pro hardware, EPYC-based VDS for dedicated virtual hardware, and bare-metal dedicated servers deployed within hours.

Payment coverage is broad: debit/credit cards, PayPal, Alipay, UnionPay, crypto, Perfect Money and bank transfer are all accepted. **[👉 Browse all current GreenCloud product lines and prices](https://greencloudvps.com/billing/aff.php?aff=6679)** if you want to compare the lines side by side before choosing.

## The refund policy, in actual detail

GreenCloud does have a money-back guarantee, but the fine print decides whether it applies to you. Under the current terms of service, new customers can request a refund on their **first VPS service within 7 days of registration**. That's it — one service, one week, new accounts only. Control panel add-ons like cPanel or DirectAdmin are never refundable.

The exclusions knock out a lot of common purchases:

- Payments made in cryptocurrency are non-refundable.
- A service that has used 10% or more of its allocated bandwidth is non-refundable — on the APAC $6 plan, that's just 75 GB.
- Promotional and flash-sale plans, dedicated servers, and proxies are non-refundable.

The billing mechanics are worth knowing before checkout too. Invoices are issued 14 days before the due date; paying 2 days late triggers a 10% late fee, service can be suspended after 1 day overdue and terminated after 3. One more trap: opening a PayPal or credit card dispute instead of a support ticket suspends all your services immediately. Cancellations go through the client area (Services → Request Cancellation), and cancelling doesn't automatically mean a refund — a cancelled, non-refunded VPS can be rebuilt later for $5 if you change your mind.

Monthly billing remains the practical safety net here: worst case, your exposure is one month's fee plus nothing else.

## What a year actually costs — and where RackNerd undercuts it

Monthly pricing looks cheap until you annualize it, so here's the honest math. RyzenKVM-1 runs $72/year, RyzenKVM-2 $120/year, RyzenKVM-3 $240/year, RyzenKVM-4 $480/year, RyzenKVM-5 $960/year. No prepay discounts on this line — the monthly rate is the rate.

Compare that with RackNerd, the name that shows up in every budget VPS search. Its Black Friday limited KVM deals went down to **$10.60/year for 1 GB RAM / 25 GB SSD / 2 TB traffic** — about $0.88 a month, roughly one-seventh of GreenCloud's entry price annualized. Even RackNerd's regular standard line starts around $26.99/year for a 512 MB plan. On pure dollars-per-year, RackNerd wins decisively.

Where the comparison flips:

- **Locations.** RackNerd's Asian coverage amounts to Tokyo and Singapore on select plans. GreenCloud offers Hong Kong, Tokyo, Singapore, Hanoi and Ho Chi Minh City across APAC, plus 30 locations overall.
- **Hardware.** GreenCloud's $6 plan rides a 3.5+ GHz Ryzen core with NVMe on a 10 Gbps port. RackNerd's cheap annual plans run Xeon cores with RAID-10 SATA SSD on 1 Gbps. For database or IO-heavy work, that difference is real.
- **Refunds.** RackNerd's standard KVM line carries a 30-day money-back guarantee. GreenCloud's 7-day guarantee is shorter and comes with the exclusions above, and its promotional plans have no refund at all — so the "just try it" cost of experimenting is lower on RackNerd's standard line.
- **Commitment.** RackNerd's best prices require annual prepay on limited-stock deals; GreenCloud's Ryzen line is month to month with no lock-in.
- **Operating systems.** RackNerd doesn't sell Windows or macOS VPS in comparable breadth. GreenCloud does both.

If absolute lowest annual cost is the goal and a US location works, RackNerd's promo deals are cheaper and easier to walk away from. If you need an Asian location, better single-core performance, Windows or macOS, or month-to-month freedom, GreenCloud's structure makes sense.

## Deals and discounts: what actually exists right now

Don't go hunting for coupon codes on this one. GreenCloud runs event-based promotions announced on its official blog, and the company stated plainly in late October that it would **not hold a Black Friday sale this year** — its 13th birthday event (October 26–31) was the only major promotional window of the season. That event included a 13% account-credit cashback on invoices of $500 or more, a "pay for 12 months of standard Windows VPS, get 6 extra" bonus, limited flash-sale plans, and a prize wheel for purchases over $50. All of it has ended.

Two practical rules from how their promotions work. First, if you see "10% off sitewide" style GreenCloud codes on coupon aggregator sites, treat them as unverified — the company's own promotions don't generally work that way, and the only reliable test is entering the code at checkout. Second, when GreenCloud does run sales, flash-sale plans come with strings attached: they're non-refundable, can't be transferred between locations, and some can't even change location until they've been active for a month. The birthday flash plans follow exactly those rules. If you missed the anniversary sale, the next meaningful discount window is probably the next seasonal event; between those, the listed monthly prices are simply the prices. **[👉 Check the official store for any current offers](https://greencloudvps.com/billing/aff.php?aff=6679)** in case something limited has appeared since this was written.

## Quick answers to the questions that actually come up

**Does the price go up on renewal?** No. These are monthly plans, so the renewal invoice matches your signup price. There's no promotional-first-term structure to expire on you.

**Why does the same plan include less traffic in Asia?** The monthly price is identical; only the allowance differs. APAC bandwidth costs more to provision, so the APAC plans carry roughly half the traffic — 750 GB versus 1.5 TB on the $6 tier — and topping up costs $15/TB versus $3/TB.

**Is the $6 plan actually usable?** For a lightweight proxy, a small static site, or a personal sandbox, yes — 1 GB RAM and a fast Ryzen core handle that. Add cPanel or run a database alongside a web app and you'll want the $10 plan's 2 GB. Each plan includes 1 IPv4 address and IPv6, managed through a SolusVM-style control panel.

**Can I get a refund if I change my mind?** Only within the first 7 days, only on your first VPS as a new customer, and not if you paid in crypto or used 10% of your bandwidth. Promotional plans are excluded entirely. Assume monthly billing is your real exit ramp.

**How reliable is it?** GreenCloud advertises 99.99% network and power uptime with a public status page, plus 24/7 support with an average ticket response of 9 minutes. Those are the company's own figures rather than an independent audit, but they're specific and checkable. One thing to set expectations on: the service is unmanaged — you get hardware and network support, but configuring your own software stack is on you.

## Choosing: a decision shortcut

Match your situation and order:

- **Cheapest possible Linux box, light usage:** RyzenKVM-1 at $6/mo in a US/EU location, where the traffic allowance doubles for free.
- **A small site or proxy with real usage:** RyzenKVM-2 at $10/mo. Most people should start here.
- **Self-hosted apps or light production:** RyzenKVM-3 at $20/mo; 2 cores and 4 GB cover most stacks.
- **Heavy traffic with global users:** a US/EU Ryzen tier — and budget $3/TB for any overage rather than $15/TB in APAC.
- **Windows or macOS:** Budget Windows from $8/mo, but price out the config you actually need first — the 5 GB class already costs $40/mo.
- **Paying by crypto or planning to buy a flash-sale plan:** skip the refund expectation entirely, since both are excluded from the guarantee.

Before you click order, confirm two things on the plan page: the exact datacenter
