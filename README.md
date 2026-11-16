# Best VPS Hosting: What It Should Cost, How Big a Server You Need, and What Vultr's $300 Credit Really Covers (Plan Table + Pre-Order Checklist)

Most VPS plans land between $20 and $100 a month. Shared hosting sits under $10, a dedicated server starts around $100, and Linux usually runs $10 to $20 a month cheaper than the same box with a Windows licence. Vultr prices at the bottom of that first band: its smallest Cloud Compute instance is **$3.50 a month with an IPv4 address**, and a new account can apply code **FLY300VULTR** for **$300 in credit**. Two things decide whether a cheap server stays cheap, and they're what the rest of this page covers: how much machine your workload actually needs, and what the invoice looks like once the credit is gone.

> **Quick picks**
> - One low-traffic site, a VPN endpoint, or a test box: Cloud Compute Regular at $3.50/mo ($2.50 on IPv6-only, New Jersey only).
> - Several WordPress sites or a small store: High Performance or High Frequency, from $6.00/mo with NVMe storage.
> - Databases with heavy read/write: Optimized Memory, from $40.00/mo.
> - Testing Vultr before you commit: FLY300VULTR gives $300 to new accounts, covers select products only, and can't be combined with other offers.
>
> 👉 Open a Vultr account and apply the $300 credit

## What a VPS costs, and where Vultr sits

Four things set the price: vCPU count, RAM, storage type (SATA SSD against NVMe), and whether the CPU cores are shared with other customers or dedicated to you. Everything else in a plan table is decoration.

Vultr doesn't sell five tidy tiers. It sells more than 120 configurations across 36 regions, from a 512 MB box in New Jersey to an eight-GPU-VRAM data-centre card in Tokyo. List prices are identical in every region except São Paulo, which runs at 1.5 times the list price, and the two cheapest sizes are sold only in New Jersey (plus Atlanta for the IPv6-only variant). If you need a $3.50 server in Frankfurt, that's not an option.

| Family | What it's for | Entry price | Order |
| --- | --- | --- | --- |
| Cloud Compute – Regular | Blogs, dev/test, low-traffic sites. Previous-gen Intel, regular SSD | $2.50/mo (IPv6 only) or $3.50/mo with IPv4 | [Start a Regular instance](https://bit.ly/VuLtr) |
| Cloud Compute – High Performance | Same budget, newer AMD EPYC or Intel Xeon, NVMe | from $6.00/mo | [Start a High Performance instance](https://bit.ly/VuLtr) |
| Cloud Compute – High Frequency | Low-latency workloads. 3 GHz+ Xeon, NVMe | from $6.00/mo | [Start a High Frequency instance](https://bit.ly/VuLtr) |
| Optimized – General Purpose | Web and app servers, e-commerce, APIs. Dedicated vCPU | from $30.00/mo | [Start a General Purpose instance](https://bit.ly/VuLtr) |
| Optimized – CPU Optimized | Video encoding, CI/CD, batch processing | from $28.00/mo | [Start a CPU Optimized instance](https://bit.ly/VuLtr) |
| Optimized – Memory Optimized | Databases, in-memory caches | from $40.00/mo | [Start a Memory Optimized instance](https://bit.ly/VuLtr) |
| Optimized – Storage Optimized | Cassandra, MongoDB, high-IOPS database work | from $75.00/mo | [Start a Storage Optimized instance](https://bit.ly/VuLtr) |
| Bare Metal | Whole-server workloads with no hypervisor | from $120.00/mo | [Check Bare Metal availability](https://bit.ly/VuLtr) |
| Cloud GPU | AI/ML and HPC | $344.00/mo (A16, 16 GB VRAM) to $1,750.00/mo (A100, 80 GB VRAM) | [Check GPU configurations](https://bit.ly/VuLtr) |

The entry price in each row is the smallest size in that family. The 512 MB Regular instance is 1 vCPU with 10 GB of SSD storage, which is enough for a static site, a tunnel endpoint, or a build agent, and not enough for WordPress with a database. The GPU row is more concrete: the A16 carries 6 vCPU, 60 GB of RAM, 350 GB of disk and 6 TB of transfer for $344 a month, while the A100 gets 12 vCPU, 120 GB of RAM, 1,400 GB of disk and 10 TB for $1,750. Those list prices were checked against Vultr's own ordering pages in November 2026, and Vultr revises configurations often enough that you should confirm the exact spec on the order form before paying.

## How big a server do you actually need?

For a single site under 90,000 monthly visits, a 1–2 GB instance with one core is usually enough, and that's the band where most readers should stop shopping.

Here's the sizing that holds up in practice, for a Linux box running a normal web stack:

- **1–2 GB RAM, 1 core** handles 5–10 lightweight sites, or 10,000–50,000 visits a month.
- **4–8 GB RAM, 2–4 cores** handles 20–50 sites, or 100,000–500,000 visits.
- **8 GB and up with multiple cores** supports 50+ sites and 1M+ visits, provided you've actually tuned caching and the database.

Guidance from vendors that sell managed servers lands in the same place by workload: a small business site wants about 2 vCPU and 4 GB; several WordPress installs want 4 vCPU and 8 GB; a store wants 4 or more vCPU and at least 8 GB; SaaS and anything with background jobs needs sizing against real load. Plugins, mail, traffic spikes, nightly backups and concurrent checkout all push those numbers up.

The honest read on Vultr's lineup: the $3.50 Regular instance exists for things that don't have a database. A WordPress site with a control panel and a few plugins wants 2 GB, which puts you a couple of steps up. If you're running several sites, the $6 High Performance tier with NVMe is the better starting point than the cheapest box, because you'll feel the storage type long before you feel the extra cores.

The other side of the question matters just as much. A VPS is a bad purchase if you're new to hosting and still learning cPanel and FTP, if the site isn't earning anything, if traffic is genuinely low, or if you don't want to own patching and firewalls. Shared hosting handles all of that for less money.

## The $300 credit: what it covers, and the mistake that wastes it

Vultr publishes four new-customer codes on its own coupon page: **FLY300VULTR** for $300, **250VULTRFLY** for $250, **FLYTWOHUNDRED** for $200, and **VULTRMATCH**, which matches your first deposit dollar for dollar up to $100. Every one of them carries the same conditions: new customers only, promotional credit applies to select products only, cannot be combined with any other offer, restrictions and terms apply.

Read those four conditions as instructions:

**Pick one code.** You can't stack the $300 credit with a deposit match or with any other promotion on the page. Choose the one that fits how you'll use the account and move on.

**"Select products" is doing real work in that sentence.** The credit is not a $300 balance you can spend on anything in the catalogue. Before you deploy a GPU instance, bare metal, or a stack of add-ons, check that the product is covered, because an uncovered line item bills to your card immediately.

**The credit is a trial with a clock, not savings.** These trial credits run for a fixed window from sign-up, and the published term for Vultr's is 30 days. The money is not the constraint. At $3.50 a month, $300 is worth about 85 months of the smallest instance, and you cannot spend it that way. Run an A100 at $1,750 a month and the same $300 disappears in roughly five days. The window, not the balance, decides what you get.

**Billing switches to your card when the window closes.** Anything still running at that point starts charging at list price. Set a reminder for a few days before the window ends, benchmark what you built, then destroy every instance you don't intend to keep.

Used properly, the credit buys a month of parallel testing: two or three sizes running side by side against your real workload, with actual load-test numbers instead of a spec sheet. That's worth more than the dollar figure suggests.

## Managed or unmanaged: the decision that changes your bill more than specs do

An unmanaged VPS means the provider supplies hardware, the network and a slot in a data centre, and you handle the operating system, the security patching, the web server and the backups. You get root and the lowest price. A managed VPS means the provider does that work inside a defined scope, which costs meaningfully more and hands over some control.

The trap is that "managed" has no standard meaning. Two hosts can both sell a managed VPS where one covers operating system updates, the control panel, the web server, the database and basic application support, and the other covers hardware monitoring and nothing above the hypervisor. Before you pay a managed premium, read the support policy and check exactly which layers are included. Anything not listed is yours.

Vultr sits firmly on the self-managed side. Its documentation library is thinner than the managed hosts' and support is built for people who are comfortable at a root prompt. That's fine if you can run `apt upgrade`, configure a firewall, and set up off-server backups. If those three tasks are unfamiliar, a managed host will cost less over a year than the first outage.

**Linux or Windows?** Most VPS providers are Linux-first, and Windows needs a licensed image, a specialist host, or a provider that explicitly offers Windows Server. If your application needs Windows, confirm availability and licence cost before comparing prices at all, because the licence changes the maths.

## VPS vs cloud hosting vs shared hosting

|  | Shared hosting | VPS | Dedicated server |
| --- | --- | --- | --- |
| Resources | Shared with everyone on the box | Virtualised and fixed to your plan | Entire machine |
| Access | Limited | Root | Full |
| Monthly cost | Low | Medium | High |
| Scales by | Changing plan | Changing plan, sometimes with a reboot | Adding hardware |

The distinction people get wrong is VPS against cloud. A VPS runs on one physical server, partitioned into virtual machines, with fixed resources and a fixed monthly price. A cloud server draws from a pool of machines, scales automatically and bills by usage. If the physical host under your VPS fails, your site goes down until it's restored. If you need automatic failover and elastic scaling, a VPS isn't the product you want, and no amount of extra RAM will make it one. If you want predictable billing and root access on a box you control, the VPS model is the cheaper answer.

## What the best VPS hosting lists leave out: nine checks before you pay

The things that turn a $6 plan into a $30 one rarely appear in a comparison table. Check these before you enter card details, and ask what each one costs if the answer isn't on the page:

1. **A promotional price with no stated renewal rate.** The second year is the real price. If the renewal rate isn't published, assume it's the list rate.
2. **A vague managed scope.** See above. Get the covered layers in writing.
3. **Backups stored only on the primary server.** A backup that dies with the server isn't a backup, and off-site backup is often a paid add-on. Reviewers on G2 single out backup pricing as feeling high relative to the instance cost, so price it before you commit.
4. **No published uptime commitment.** Serious hosts publish a figure, commonly 99.9%, along with sub-500 ms response targets. No number means no recourse.
5. **Unclear resource allocation.** Shared, burstable and dedicated vCPU behave differently under load. "4 cores" without a qualifier is marketing.
6. **Control panel and OS licences that appear only at checkout.** cPanel, Plesk and Windows licensing are separate line items at most hosts. Plesk in particular is an extra purchase on some plans that look cheap up front.
7. **Very few server locations.** Latency to your users is set by geography. Vultr's 36 regions are a strength here, but remember that its two cheapest sizes are New Jersey-only, so the headline price and the location you need may not coexist.
8. **No documented migration process.** Free migration is common but not universal, and a host without a written process expects you to move the data yourself.
9. **Upgrades that require a full server move.** Ask whether resizing is a reboot or a rebuild. The difference is an afternoon of downtime versus five minutes.

Add the recurring extras to any comparison: backups, panel licences, extra IPv4 addresses, bandwidth overage, and monitoring. A $6 server with a $10 backup add-on and a $15 panel licence is a $31 server.

## How Vultr compares with the usual shortlist

Vultr's case is footprint and price. A price tracker that monitors budget cloud providers counts more data-centre locations at Vultr than at any other provider it covers, which matters if you need a box in São Paulo, Johannesburg or Seoul at a predictable monthly rate. The trade-off is a thinner documentation library and support aimed at experienced users.

Where the alternatives fit, based on published specs rather than preference:

| Provider | Verified detail | Where it fits |
| --- | --- | --- |
| Hostinger | 1–8 vCPU, 4–32 GB RAM, 50–400 GB storage, free domain, 74 one-click applications including WordPress and WooCommerce | Users who want guided self-management and a wide app catalogue |
| IONOS | 1–24 GB RAM, unlimited traffic, low entry pricing, Plesk sold separately | Budget Linux or Windows boxes for people with some server knowledge |
| Hostwinds | Managed or unmanaged, Linux or Windows, RAM up to 96 GB, hourly or monthly billing | Workloads that need a big memory footprint or Windows |
| Liquid Web | 100% power and network uptime commitment, 59-second support response target, full managed tiers | Businesses that can't absorb downtime and don't want to administer anything |
| Kamatera | You choose CPU, RAM and storage; 20+ data centres; hourly or monthly billing | Custom configurations and short-lived projects |
| DreamHost | Unmetered bandwidth on every tier, root on all plans, WordPress-tuned tooling | WordPress users who want a simpler panel |
| DigitalOcean | API-first, primarily self-managed, multiple VM types | Developers automating infrastructure |

None of those details are reasons to avoid Vultr. They're the reasons someone else might pick differently.

## FAQ

**Can a $3.50 VPS run WooCommerce?**
No. A 512 MB instance with 10 GB of disk will fall over on a store with a catalogue and concurrent checkout. Typical guidance for e-commerce is 4 or more vCPU with at least 8 GB of RAM, which on Vultr means the High Performance tier or an Optimized General Purpose instance.

**How many sites fit on 1 GB of RAM?**
Five to ten lightweight sites, assuming static pages or well-cached WordPress with modest plugin counts. Move to 4–8 GB once you pass a few dozen sites or start running staging copies.

**What do I need to know to run an unmanaged VPS?**
Operating system updates, firewall rules, SSH key management, log reading, and a backup routine that copies data off the server. If that list is unfamiliar, buy managed hosting or a managed VPS instead.

**Does the $300 credit cover everything on the pricing page?**
No. Vultr's terms say promotional credit applies to select products only, it's for new customers, and it can't be combined with other offers.

**Will my price rise after the first period?**
The credit is a separate balance from your plan price, so when it expires your card is charged the list rate for whatever is running. Vultr's list prices are published per configuration and were unchanged between October and November 2026, but the way to avoid surprises is to check the price of the size you actually ordered, not the entry price of the family.

## Which one to buy

Match the machine to the job and stop there:

- **One low-traffic site, a test box, or a tunnel endpoint:** Cloud Compute Regular at $3.50/mo. Accept that it's New Jersey-only and skip it if your users are in Europe.
- **Several WordPress sites or a small store:** High Performance or High Frequency from $6.00/mo. The NVMe storage is the part you'll notice.
- **A database, a cache layer, or anything memory-bound:** Optimized Memory from $40.00/mo. Shared vCPU is the wrong tool for sustained write loads.
- **You don't want to administer a server:** buy managed hosting elsewhere, or budget for someone who'll run the box for you. A cheap unmanaged VPS you can't maintain is the most expensive option on this page.

Two things to confirm before you pay: that the size you want is available in the region you need, and what your monthly bill will be once any credit has expired. Then decide, deploy, and put a calendar reminder on the day the credit window closes.

👉 [Claim the $300 Vultr credit and pick your instance size](https://bit.ly/VuLtr)
