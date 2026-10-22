# vps plans: What to Check Before You Commit, and Every GoMami Plan Priced Side by Side

Most "vps plans" pages give you a spec sheet and a monthly number. The two things that actually decide whether a plan is worth buying — what the bill looks like after the first term, and what happens the week you burn through your traffic allowance — usually get left out.

This page covers one provider in detail: GoMami Networks, a small host that sells nothing but China-route servers in Hong Kong, Tokyo, Singapore, and Los Angeles. Its plans start at $29/month and run to $999/month, so the spread is wide enough to work as a practical example of how to read any VPS plan list. Prices below come from GoMami's own store pages unless noted.

> **Quick picks if you don't want to read the whole thing**
> - Cheapest way onto China-optimized routing: **JPN.Pulse.Nano or SIN.Pulse.Nano, $29/mo** — 2 vCPU, 2 GB RAM, 40 GB NVMe, 500 GB outbound, 1 Gbps.
> - Best single-thread performance for a database or game server: **HKG.Turin.Mini, $69/mo** — 2 vCPU on EPYC 9575F, 4 GB, 100 GB NVMe, 1 TB, 2 Gbps.
> - Most traffic per dollar: **LAX.Pulse.Titan, $999/mo** for 30 TB and a 10 Gbps port; the LAX Nano already gives 1 TB at $29.
> - 👉 [Compare every GoMami plan on the store page](https://bit.ly/Gomami)

## How to read a VPS plan list without getting fooled

Check four things before the specs: the renewal price, whether traffic is metered inbound or outbound, what the port speed is actually for, and whether the CPU is chosen for clock speed or core count.

**Renewal price.** GoMami publishes one monthly price and doesn't run first-term teaser pricing; paying annually comes out cheaper than monthly. That's unusual. The mainstream shared-VPS market works the opposite way — Hostinger's KVM 2 is listed at $8.99/mo and renews at $14.99, DreamHost's Stack 8 goes from $9.49 to $14.99, HostGator's Snappy 4000 from $8.36 to $18.70, per Gizmodo's September 2026 roundup of 8 GB plans. Promo terms differ between hosts, so treat those as ballpark figures. A provider quoting the same number every month is easier to budget for, even when the number is higher.

**Traffic direction and overage.** GoMami meters outbound only; inbound is free, and the quota resets each billing cycle. What happens after you exceed it differs by product line, and that difference matters more than the quota itself.

**Port speed.** A 10 Gbps port paired with 30 TB of monthly traffic is a burst ceiling; sustained throughput will sit lower. A 1 Gbps port with 500 GB works the other way — you'll hit the traffic cap long before the port becomes the constraint.

**CPU choice.** The EPYC 9575F in the Turin line boosts to 5.0 GHz; the EPYC 7763 in most Pulse plans boosts to 3.5 GHz. For MySQL InnoDB queries, game loops, or anything where one thread does the work, the higher clock is worth more than extra cores. For containers and multi-tenant workloads, the reverse.

## Every GoMami VPS plan, by location

GoMami's lineup is organised by hardware platform and datacenter. There's no small/medium/large tiering. Hong Kong carries three lines (Turin, Pulse, Forge), while Tokyo, Singapore, and Los Angeles carry Pulse only. All plans run KVM with NVMe storage and carry the same "China Mainland Optimized Pro" routing label.

### Hong Kong — HKG Turin (AMD EPYC 9575F, Zen 5, up to 5.0 GHz)

| Plan | vCPU / RAM / NVMe | Traffic (out) | Port | Price/mo | Order |
| --- | --- | --- | --- | --- | --- |
| HKG.Turin.Mini | 2 / 4 GB / 100 GB | 1 TB | 2 Gbps | $69 | [Order](https://bit.ly/Gomami) |
| HKG.Turin.Air | 4 / 8 GB / 140 GB | 2 TB | 2 Gbps | $129 | [Order](https://bit.ly/Gomami) |
| HKG.Turin.Pro | 6 / 16 GB / 180 GB | 5 TB | 5 Gbps | $299 | [Order](https://bit.ly/Gomami) |
| HKG.Turin.Ultra | 12 / 32 GB / 220 GB | 10 TB | 5 Gbps | $599 | [Order](https://bit.ly/Gomami) |

Pro and Ultra are marked Windows-ready on the store page. Turin runs PCIe Gen5 U.2 SSDs and DDR5-6400 memory, the newest hardware in the lineup.

### Hong Kong — HKG Pulse (AMD EPYC 7763, up to 3.5 GHz)

| Plan | vCPU / RAM / NVMe | Traffic (out) | Port | Price/mo | Order |
| --- | --- | --- | --- | --- | --- |
| HKG.Pulse.Nano | 2 / 2 GB / 40 GB | 500 GB | 1 Gbps | $49 | [Order](https://bit.ly/Gomami) |
| HKG.Pulse.Mini | 2 / 4 GB / 60 GB | 1 TB | 1 Gbps | $59 | [Order](https://bit.ly/Gomami) |
| HKG.Pulse.Air | 4 / 8 GB / 80 GB | 2 TB | 1 Gbps | $119 | [Order](https://bit.ly/Gomami) |
| HKG.Pulse.Pro | 8 / 16 GB / 100 GB | 5 TB | 3 Gbps | $269 | [Order](https://bit.ly/Gomami) |
| HKG.Pulse.Ultra | 12 / 32 GB / 300 GB | 10 TB | 3 Gbps | $499 | [Order](https://bit.ly/Gomami) |

### Tokyo and Singapore — JPN Pulse and SIN Pulse

Both cities price identically at every tier, and only the Mini's port differs. One table, with the location noted.

| Plan | Location | vCPU / RAM / NVMe | Traffic (out) | Port | Price/mo | Order |
| --- | --- | --- | --- | --- | --- | --- |
| Pulse.Nano | Tokyo / Singapore | 2 / 2 GB / 40 GB | 500 GB | 1 Gbps | $29 | [Order](https://bit.ly/Gomami) |
| Pulse.Mini | Tokyo / Singapore | 2 / 4 GB / 60 GB | 1 TB | 1.5 Gbps Tokyo, 1 Gbps Singapore | $49 | [Order](https://bit.ly/Gomami) |
| Pulse.Air | Tokyo / Singapore | 4 / 8 GB / 80 GB | 2 TB | 1 Gbps | $89 | [Order](https://bit.ly/Gomami) |
| Pulse.Pro | Tokyo / Singapore | 8 / 16 GB / 100 GB | 5 TB | 3 Gbps | $169 | [Order](https://bit.ly/Gomami) |
| Pulse.Ultra | Tokyo / Singapore | 12 / 32 GB / 300 GB | 10 TB | 3 Gbps | $338 | [Order](https://bit.ly/Gomami) |

Pick Singapore if part of your audience sits in Southeast Asia; pick Tokyo for northern and eastern China. Pro and Ultra are Windows-ready in both cities.

### Los Angeles — LAX Pulse

| Plan | vCPU / RAM / NVMe | Traffic (out) | Port | Price/mo | Order |
| --- | --- | --- | --- | --- | --- |
| LAX.Pulse.Nano | 2 / 2 GB / 40 GB | 1 TB | 1 Gbps | $29 | [Order](https://bit.ly/Gomami) |
| LAX.Pulse.Mini | 2 / 4 GB / 60 GB | 2 TB | 1 Gbps | $59 | [Order](https://bit.ly/Gomami) |
| LAX.Pulse.Air | 4 / 8 GB / 80 GB | 4 TB | 2 Gbps | $129 | [Order](https://bit.ly/Gomami) |
| LAX.Pulse.Pro | 6 / 16 GB / 100 GB | 8 TB | 3 Gbps | $259 | [Order](https://bit.ly/Gomami) |
| LAX.Pulse.Ultra | 12 / 32 GB / 300 GB | 15 TB | 5 Gbps | $599 | [Order](https://bit.ly/Gomami) |
| LAX.Pulse.Titan | 12 / 32 GB / 600 GB | 30 TB | 10 Gbps | $999 | [Order](https://bit.ly/Gomami) |

The LAX tiers are the only ones where the traffic allowance roughly doubles versus Asia at the same price.

There's also a launch code on this line: **`Hi,LAX`**, a 20% recurring discount introduced when the Los Angeles node went live in June 2026. It brought the Nano from $29 down to about $23.20/month, and being a recurring discount, the lower rate repeats each term rather than only on the first invoice. Third-party coverage described it as a limited launch promotion tied to available capacity, so check whether it's still accepted in the cart before you count on the lower figure.

A June 2026 third-party review described the LAX hardware as slightly behind GoMami's other lines; the same reviewer raised the rating to "E2" in July after a stability observation period.

### Hong Kong — HKG Forge (dedicated servers)

| Plan | CPU / RAM / NVMe | Traffic | Port | Price/mo | Order |
| --- | --- | --- | --- | --- | --- |
| HKG.Forge.Mini | EPYC 7663 56C/112T / 128 GB / 960 GB | 10 TB | 2 Gbps | $599 | [Order](https://bit.ly/Gomami) |
| HKG.Forge.Air | EPYC 7663 56C/112T / 256 GB / 4 TB | 20 TB | 2 Gbps | $899 | [Order](https://bit.ly/Gomami) |

Forge is a whole TYAN B8033 machine. Overage is billed at $0.06/GB with no throttling, extra IPs cost $10 each (max four per server), and the store page notes instant activation plus self-service OS reinstall. Third-party write-ups mention a one-time $68 setup fee; the store page extract doesn't show it, so confirm before paying.

### Lines GoMami lists without a price

Two more sets of plans appear on the site but can't be quoted as a monthly figure, so they're listed here rather than in the pricing tables above.

| Plan | Specs | Price shown |
| --- | --- | --- |
| HKG.Peak.X5.Mini | 2 vCPU / 4 GB / 40 GB / 1 TB / 2 Gbps | Not displayed on the page |
| HKG.Peak.X5.Air | 4 vCPU / 8 GB / 60 GB / 2 TB / 2 Gbps | Not displayed on the page |
| HKG.Peak.X5.Pro | 6 vCPU / 16 GB / 80 GB / 5 TB / 5 Gbps | Not displayed on the page |

The homepage also surfaces six plan cards with prices — three on a Ryzen 9 9950X (up to 5.7 GHz) at $59, $99, and $199, and three on an EPYC 7763 at $39, $79, and $169. Those cards don't name a datacenter, and their EPYC pricing doesn't line up with the Hong Kong Pulse table above, so don't treat the homepage numbers as any specific city's price. Confirm on the store page before ordering.

## Why $29 is the floor here, and what the premium buys

The median entry price across 391 VPS hosts tracked by CloudsPress in October 2026 is $9.95/month, with a median renewal of $11.46. GoMami's cheapest plan is roughly three times that. The gap buys routing.

Its China-facing return path splits by carrier: CN2 for Telecom, AS9929 for Unicom, CMIN2 for Mobile — three separate premium backbones, each matched to the carrier your user happens to be on. Transit on those networks is expensive; industry commentary puts CN2 GIA IP transit at up to roughly $120 per megabit at the high end, which is the structural reason China-optimized servers don't come cheap. GoMami also claims RTT under 50 ms to mainland China and DDoS scrubbing up to 600 Gbps.

Whether that's worth 3x depends entirely on whether your users are in China. If they're not, a $9 host in Frankfurt does the same job. If they are, the cheap host's "China direct" route is the thing that collapses at 8 PM.

Independent testing gives a mixed but mostly positive picture. DigVPS measured HKG.Pulse.Mini at evening peak and found Telecom and Mobile unchanged from daytime while Unicom fluctuated badly — one test showed Shanghai Unicom and Hunan Unicom differing by nearly a factor of two. After the October 2025 route change to CN2/9929/CMIN2, the same reviewer recorded a 40–100% throughput improvement on the Japan line. A separate test of Turin.Mini put Geekbench 5 single-core at 1101, about 124% above the 7763 comparison machine.

## The real annual cost, and where the discount codes go

Paying yearly is the only way to get a meaningful discount, and the code most commonly cited is `GOMAMI365`.

GoMami's billing docs state annual billing typically saves 15–20% versus monthly. DigVPS describes `GOMAMI365` as 20% off recurring across the full lineup, and a restock channel was still pushing it in September 2026. Third-party sources say it only takes effect on annual orders and does nothing on monthly billing — that condition isn't stated in GoMami's own documentation, so apply it in the cart and confirm the total moved before paying. Run the numbers on the two plans most people shortlist:

- **HKG.Turin.Mini**: $69 × 12 = $828/year at monthly billing; at 20% off annual, $662.40 — a saving of $165.60.
- **JPN.Pulse.Nano**: $29 × 12 = $348/year; at 20% off, $278.40.

The code field sits on the cart page, before Checkout. If the discount doesn't take, that's a support ticket, not a reason to pay and argue later.

One more line item worth pricing in: traffic packs. GoMami sells them self-service at $6 per 100 GB, $30 per 500 GB, $60 per 1 TB, up to $1,200 for 20 TB. They're valid only for the current billing cycle and don't roll over. On Forge, by contrast, overage is metered at $0.06/GB — an extra 1 TB there costs $61.44 on the invoice, roughly the price of a JPN.Pulse.Mini for a month.

👉 [Start with the $29 Tokyo or Singapore Nano and check the annual price at checkout](https://bit.ly/Gomami)

## What the docs say that the sales page doesn't

Four things in GoMami's documentation will affect you more than any benchmark, and none of them appear on the homepage.

**There is no grace period.** Service is suspended on the due date if payment hasn't landed. Five days later the service is terminated and the data may not be recoverable; on day six the invoice is auto-cancelled. Renewal invoices are generated seven days ahead with email notification, and a card on file gets charged automatically. Suspended services restore automatically once payment clears.

**The refund window is 24 hours and applies once.** It covers newly purchased instances, is limited to one per user, and excludes renewal orders, services terminated for terms violations, used account credit, and any IP blackholed by a DDoS attack. Alipay refunds take 1–3 business days, cards 5–10. Once approved, the instance and its data are permanently deleted — back up first.

**Traffic overage on VPS is a throttle, not a bill.** The FAQ says bandwidth "may be throttled" after the monthly quota, with specifics depending on the product, until the cycle resets. Some third-party articles state a hard 20 KB/s figure; the official documentation doesn't commit to a number, so size the plan for your actual monthly volume.

**No uptime percentage is published.** Competitors commonly advertise 99.9% to 99.99% SLAs. GoMami's site and docs don't make an availability commitment, so if a contractual SLA is a procurement requirement, this provider won't satisfy it on paper.

Also in the terms: sustained high CPU that affects other tenants on the same node can get you throttled as a "noisy neighbor," and deliberate bandwidth, CPU, or disk I/O abuse is prohibited.

👉 [Read the plan list and check current stock before ordering](https://bit.ly/Gomami)

## Matching a plan to an actual workload

Hong Kong is the lowest-latency option and the only place Turin and Forge exist. Tokyo and Singapore hit $29. Los Angeles gives the most traffic per dollar.

**A single small site, a proxy, or a dev box:** JPN.Pulse.Nano or SIN.Pulse.Nano at $29. Two cores and 2 GB is enough for one modest site; 500 GB outbound is the constraint, not the CPU.

**A production site with moderate traffic:** HKG.Pulse.Mini at $59. Memory doubles from the Nano's 2 GB to 4 GB, storage goes from 40 GB to 60 GB, and traffic from 500 GB to 1 TB — for $10 more than the Hong Kong Nano, with the lowest latency to southern and eastern China.

**Databases, Redis, game servers, anything single-thread bound:** HKG.Turin.Mini at $69. The 9575F nearly matches a desktop Ryzen 9 9950X in single-core, and the 100 GB baseline fixes the small-disk complaint that followed the Pulse line.

**Multi-container or multi-tenant work:** HKG.Pulse.Air at $119, or JPN.Pulse.Air at $89 if you don't need Hong Kong latency. Four cores and 8 GB is where you stop worrying about contention.

**Serving China and North America from one box:** LAX.Pulse.Mini at $59 with 2 TB, or LAX.Pulse.Air at $129 with a 2 Gbps port. Wider traffic allowances and a US IP.

**A 128 GB database host that can't share a node:** HKG.Forge.Mini at $599. If your workload still fits inside 16 GB, this is a $500/month mistake.

## Ordering, step by step

Log in, pick the location and product line from the left sidebar (Hong Kong splits into Turin, Pulse, and Forge; Japan and Singapore each have Pulse), then hit Order Now on the plan you want. On the configure page, choose the billing cycle — this is where annual pricing appears. Continue to the cart, verify the line item, enter the promo code, then check out. Payment options are credit card, Stripe Alipay, or crypto, and existing account credit can be applied. Tick the terms box, complete the order, and deployment runs automatically, typically within a few minutes, with the IP and credentials arriving by email.

If you're testing before committing real workload, the 24-hour refund window is the time to run your own latency checks from the regions your users actually sit in. It's a single shot per account, so don't burn it on a plan you already know is the wrong size.

👉 [Open the GoMami store and pick a location](https://bit.ly/Gomami)

## FAQ

**Are these managed plans?** No. GoMami is self-managed — KVM with root access, and you handle the OS, software, and security. The documentation covers SSH connection and dashboard basics, not application support.

**What happens when I hit the traffic limit?** Bandwidth may be throttled until the cycle resets, with the specific policy depending on the product line. You can buy a traffic pack in the control panel instead of upgrading; packs expire at the end of the current cycle.

**Can I get a refund if it doesn't work out?** Within 24 hours of activation, on a first purchase, once per user. Renewals, ToS terminations, used credit, and DDoS-blackholed IPs are excluded. Approved refunds delete the instance and its data immediately.

**Do the plans support Windows?** Turin Pro and Ultra, and Pulse Pro and Ultra, are labelled Windows-ready on the store page. Licence cost and activation aren't documented publicly — ask support before assuming it's included.

**Is there a money-back trial or free tier?** No free tier. The 24-hour cancellation window is the closest equivalent.

**Which location should a mainland-China audience pick?** Hong Kong first for latency, then Tokyo for northern and eastern China on a budget, Singapore if Southeast Asia matters, Los Angeles if you also serve US users.

## Before you pay

Match the plan to what you're actually running. A single site needs the $29 Nano; a WordPress install with real traffic needs the $59 Pulse.Mini; a database that's slow because of clock speed needs the $69 Turin.Mini; a 128 GB Postgres box needs Forge and nothing smaller.

Two things to confirm at checkout: whether `GOMAMI365` actually reduced the annual total (and whether you're on a yearly cycle at all), and whether `Hi,LAX` still applies if you're buying into the Los Angeles line. Then check the billing cycle you selected before hitting Complete Order — the due date has no grace period, and the refund window closes after 24 hours.

👉 [Check GoMami's current plan list and prices for your location](https://bit.ly/Gomami)
