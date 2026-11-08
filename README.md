# OVH Dedicated Server Pricing: What €114.99 a Month Really Costs, Which of the Four Ranges Fits Your Load, and Where Unlimited Bandwidth Stops (Full Plan Tables)

OVHcloud's dedicated server range starts at **€114.99 per month ex. VAT** on its Irish site, and the first invoice comes to €229.98 because the one-off installation fee equals a full month of rental. Four ranges sit above that entry point, and for most production workloads the right machine is one configuration step up rather than a whole tier. The tables below price every range and every Advance configuration, work out what year one actually costs, and mark the two points where the "unmetered" traffic claim stops applying.

> **Quick pick.** Web apps, ERP/CRM, a handful of VMs: **ADVANCE-22024 at €154.99/month ex. VAT** (8 cores/16 threads, 64 GB DDR5, 2×960 GB NVMe). Monthly cost is the constraint: ADVANCE-12024 at €114.99. More than 16 cores or 50 Gbps+ private networking: Scale, from €539.99. Game hosting: Game, from €279.99.
> 👉 [See SpinServers' US bare-metal configurations from $79/month with no installation fee](https://bit.ly/Spinservers)

## All four OVHcloud dedicated ranges at a glance

| Range | Cores / memory | Disks | Public · private bandwidth | Entry price |
| --- | --- | --- | --- | --- |
| Advance | 6–24 cores, 32 GB–1 TB RAM | 2–8 | 1–5 Gbps public · 25 Gbps private | €114.99/mo ex. VAT (Ireland) |
| Game | 8–16 cores, 64–256 GB RAM | 2 | 1 Gbps public | €279.99/mo ex. VAT (Ireland) |
| Scale | 16–384 cores, 128 GB–3 TB RAM | 2–36 | 1–220 Gbps public · 50–100 Gbps private | €539.99/mo ex. VAT (Ireland) |
| High Grade | 16–192 cores | 2–36 | 1–220 Gbps public · 50–100 Gbps private | €1,254.99/mo ex. VAT (Ireland) |

Every plan in the line includes anti-DDoS protection, unlimited inbound and outbound traffic, and 500 GB of external storage at no extra cost. The hardware is OVHcloud's own design, assembled and maintained in-house, with liquid cooling and lifecycle management covering the physical side. Public bandwidth across the full catalogue runs from 1 Gbps to 220 Gbps, private bandwidth from 50 Gbps to 100 Gbps. There are more than 40 data centres, and the latency argument for choosing the one closest to your users is worth more than most spec upgrades.

Two pricing caveats before the detail. The German site lists the same four Advance machines at €136.99, €184.99, €191.00 and €237.99 including MwSt., the UK site quotes Advance from £98.99 ex. VAT, and the US site from $136.00 excluding taxes. These are not price rises or discounts. They are different country price lists in different currencies and tax bases, so compare like with like and confirm which data centre the quote applies to.

## The four Advance configurations, priced line by line

| Configuration | CPU | Memory / storage | Monthly ex. VAT | Monthly incl. VAT | Install fee |
| --- | --- | --- | --- | --- | --- |
| ADVANCE-12024 | AMD EPYC 4244P, 6c/12t, 3.8–5.1 GHz | 32 GB DDR5 ECC 5200 · 2×960 GB NVMe Enterprise | €114.99 | €141.44 | €114.99 |
| ADVANCE-22024 | AMD EPYC 4344P, 8c/16t, 3.8–5.3 GHz | 64 GB DDR5 ECC 5200 · 2×960 GB NVMe Enterprise | €154.99 | €190.64 | €154.99 |
| ADVANCE-12026 | AMD EPYC 4245P, 6c/12t, 3.9–5.4 GHz | 32 GB DDR5 ECC 5600 · 2×960 GB NVMe Datacenter | €159.99 | €196.79 | €159.99 |
| ADVANCE-32024 | AMD EPYC 4464P, 12c/24t, 3.7–5.4 GHz | 64 GB DDR5 ECC 5200 · 2×960 GB NVMe Enterprise | €199.99 | €245.99 | €199.99 |

All four carry 3 Gbps unmetered and guaranteed public bandwidth plus 25 Gbps guaranteed unmetered private bandwidth. The Irish VAT rate adds 23%, which is where the incl.-VAT column comes from.

There is one counter-intuitive entry in that table. ADVANCE-12026 costs €5 more per month than ADVANCE-22024 while giving you two fewer cores and half the RAM. What you pay for is newer memory (5600 MT/s against 5200) and Datacenter-class NVMe drives instead of Enterprise-class. If you are not specifically chasing drive endurance or the faster memory bus, the 22024 is the better buy at a lower price.

## What year one actually costs

The installation fee is charged once and matches the monthly price exactly, so the first invoice is double the headline:

- ADVANCE-12024: €229.98 on day one, €1,494.87 across twelve months, ex. VAT
- ADVANCE-22024: €309.98 on day one, €2,014.87 across twelve months, ex. VAT
- ADVANCE-32024: €399.98 on day one, €2,599.87 across twelve months, ex. VAT

Year two drops to twelve monthly payments. Anyone comparing OVHcloud against a provider that charges no setup fee needs to add that first-month figure into the comparison, because it is roughly 8% of the first-year spend on every one of these machines.

👉 [Compare against SpinServers' $79/month entry server, billed month to month with no setup fee](https://bit.ly/Spinservers)

## Where "unmetered" stops being unmetered

The default is unlimited and unmetered traffic. Two exceptions matter.

The first is geographic. Traffic is unmetered everywhere except OVHcloud's Asia-Pacific data centres, which sit outside the standard traffic policy. If your users are in Singapore or Sydney, read the terms for that region before you size the link.

The second is a fair-use lever. OVHcloud reserves the right to limit outbound public bandwidth to 50% of the port speed when a server's egress affects other customers' network quality. On an Advance box with 3 Gbps guaranteed, that ceiling is 1.5 Gbps outbound, not a cut-off. It has never been a headline feature of these plans, and heavy outbound workloads should plan around it.

Everything else about the networking is more generous than the price suggests. Each dedicated server ships with two physical network cards, one on the public internet and one reserved for the private network. The private side runs over vRack, which is how you connect a web server to a database without exposing the database, or link several servers across locations. You can disable the public IP entirely and leave a machine reachable only over the private network. OVHcloud Link Aggregation (OLA) and hardware RAID are available as options.

## Choosing between Advance, Scale and Game

Advance covers 6 to 24 cores, up to 1 TB of RAM depending on model, and either NVMe SSDs or large SAS drives in the Advance-STOR variants. Third-generation units carry dual-port 25 Gbps network interfaces, and the newest use AMD EPYC 4000 and 8000 processors. Thermals are handled with standard rack airflow rather than exotic cooling, which keeps performance variation under 8% at peak, supports CPUs up to 250 W TDP, and holds PUE as low as 1.15 thanks to OVHcloud's water-cooling design. Network availability is covered by a 99.95% SLA with service credits if the target is missed. For web hosting, business applications and moderate virtualisation, this is the range to buy.

Scale exists for the workloads that break the Advance envelope: from 16 cores up to 384, up to 3 TB of RAM, up to 36 disks, and public bandwidth up to 220 Gbps with 50–100 Gbps private. If you are not planning to run large virtualisation clusters, distributed databases or big-data processing, the extra spend buys headroom you will not use. A 12-core ADVANCE-32024 at €199.99 handles a great many production applications on its own.

Game is a narrow product. 8 to 16 cores, 64 to 256 GB of RAM, high-clock CPUs and DDoS protection tuned for game traffic, from €279.99. If you host Minecraft or a similar real-time multiplayer service where per-tick latency decides player retention, the premium is justified. If you are hosting a corporate site, paying it is a waste.

High Grade is the resilience tier for critical workloads, priced from €1,254.99 ex. VAT on the Irish site. Its selling point is redundancy rather than raw core count, so it only makes sense when downtime costs more than the monthly difference.

One operational detail applies to all four: quoted delivery times are indicative and not a contractual condition, and the clock starts at payment. Do not build a launch date around a delivery estimate without confirming it with sales.

## Certifications are options, not defaults

OVHcloud's bare metal line carries ISO/IEC 27001, 27017, 27018 and 27701, CSA STAR, SOC 1–2 Type I, and HDS certification for health data hosting. Two qualifiers come with that list, both from the same page: the certifications are available as an option, and not all of them apply in every location. If you work in a regulated sector and need a specific certificate in a specific data centre, get written confirmation from sales before you order rather than assuming the whole portfolio is covered everywhere.

## A US alternative worth pricing first

For teams whose users are in North America, SpinServers is a useful second quote. It runs bare metal in Dallas, Texas and San Jose, California, and its published entry point is $79 per month for an Intel Xeon E3-1280 v5 with 4 cores/8 threads, 32 GB DDR4 ECC memory, a 1 TB M.2 NVMe drive, 30 TB of monthly transfer and 2×10 Gbps ports.

| Plan | CPU / memory / storage | Transfer · ports | Price | Order |
| --- | --- | --- | --- | --- |
| Intel Xeon E3-1280 v5 | 4c/8t · 32 GB DDR4 ECC · 1 TB M.2 NVMe | 30 TB · 2×10 Gbps | $79/mo | [Check stock](https://bit.ly/Spinservers) |
| Starter Package | 32 GB RAM · 1 TB NVMe · full root access | 10 TB · 10 Gbps | $99/mo | [Check stock](https://bit.ly/Spinservers) |
| Growth Package | 256 GB RAM · 2×1.6 TB SSD | 20 TB · 10 Gbps | $149/mo | [Check stock](https://bit.ly/Spinservers) |
| High Performance Package | 768 GB RAM · 8×2 TB SSD | 40 TB · 10 Gbps | $679/mo | [Check stock](https://bit.ly/Spinservers) |

The structural differences against OVHcloud are worth listing plainly, because they cut in both directions.

Billing is month to month with no setup fee, so there is no €114.99-style installation charge and no first-invoice doubling. Bandwidth is metered rather than unmetered: 30 TB on the entry plan, 10 TB on the Starter, 20 TB on Growth, 40 TB on High Performance. On a 10 Gbps port, 30 TB is roughly 2.8 days of continuous line-rate transfer, so it suits normal web traffic and not bulk media distribution. OVHcloud's unmetered model wins clearly for high-egress workloads.

Geography is the other trade. SpinServers operates two US data centres against OVHcloud's 40-plus locations, so if your users are in Europe or Asia, the latency argument favours OVHcloud regardless of price.

On the operational side, SpinServers provisions instantly from in-stock inventory and offers automated Linux, Windows and ESXi installs, IPMI/iKVM console access, and a free Layer 2 private network (VPC) between your servers. Its network is multihomed on its own ASN with DDoS protection. The company advertises PCI-compliant facilities, though managed compliance work stays with you. One caveat from a 2026 third-party review: month-to-month services of this kind generally carry no refund policy, and pricing varies by location, hardware and availability, so confirm the exact configuration at checkout.

👉 [See current SpinServers inventory in Dallas and San Jose](https://bit.ly/Spinservers)

## When a dedicated server is the wrong purchase

OVHcloud's own guidance is blunt about this. A dedicated server means you own everything from configuration to data to security, and you get no virtualisation layer eating your resources. If you would rather not handle technical management, Public Cloud instances are the intended alternative. If you are building a simple website, shared hosting does the job at a fraction of the cost.

The honest split looks like this: dedicated makes sense when you have a workload with predictable, sustained resource demand and someone on the team who can administer a Linux box. It makes less sense for spiky projects, for teams without sysadmin coverage, or where a managed platform is cheaper than the hours you would spend patching.

## FAQ

**Can the installation fee be waived?** The product pages reviewed here do not mention any waiver or promotion. Ask sales directly before ordering, and if a waiver is offered, get it in writing on the order.

**How long does delivery take?** OVHcloud states that delivery times are indicative only and do not form a contractual condition, counted from payment. Treat any figure you see as an estimate.

**Is the traffic genuinely unlimited?** Unlimited and unmetered by default, with the Asia-Pacific exception and the reserved right to cap outbound public bandwidth at 50% when a server's egress affects other customers.

**Can I install Windows, a custom ISO or a hypervisor?** The range supports multiple distributions, operating systems, databases and hypervisors, and the control panel can preinstall officially optimised images. Custom installations are part of the point of bare metal, since you hold full administrative control.

**Should I pick an Asia-Pacific data centre?** Only if your users are there. Traffic policy differs in that region, so factor the terms into your bandwidth planning rather than assuming the European unmetered model applies.

## Before you order

Match the machine to the load first. A single application server with modest database traffic: ADVANCE-22024 at €154.99 ex. VAT, and budget €309.98 for the first invoice. Static or low-traffic web hosting: ADVANCE-12024 at €114.99. Virtualisation clusters, distributed data or anything that needs more than 16 cores or 50 Gbps private networking: Scale. Real-time game hosting: Game. Critical workloads where downtime dominates the cost model: High Grade.

Then confirm four things before paying: whether the price you are looking at is ex. VAT or incl. VAT and which country's price list it comes from, the exact installation fee, the data centre your order will land in, and whether the specific certification you need is offered as an option in that location.

If you want a US-based quote to compare against before committing, 👉 [check SpinServers' current bare-metal plans and stock](https://bit.ly/Spinservers). No setup fee, month-to-month terms and metered transfer make it a genuinely different deal from OVHcloud's, which is exactly why it belongs in the comparison.
