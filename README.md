# unmanaged vps hosting: What You Actually Get, the Three-Year Cost Math, and Where BandwagonHost's Flat-Renewal KVM Plans Fit

Unmanaged VPS hosting is a simple trade. The provider keeps a virtual machine running on maintained hardware with a working network and hands you root access. Everything above that line — operating system updates, security patches, firewall rules, your applications, your backups — is your job. If you're comfortable in an SSH session, that's where the savings come from: you stop paying someone to run `apt upgrade` on your behalf.

Pricing is where people get burned, though. Intro rates that jump 85% at renewal, backup add-ons that quietly add 20% to the bill, and spec sheets that put a $4.69 teaser next to a competitor's list price all make cheap VPS look cheaper than it is. This guide covers what you're actually signing up for, what a plan costs by year three, what backups really add, and where BandwagonHost — a budget KVM brand that has sold cheap annual plans for over a decade — beats or loses to Hostinger, DigitalOcean, Vultr and Hetzner.

> **Quick picks**
>
> - **Lowest multi-year bill:** BandwagonHost's 1 GB KVM plan — $49.99/year (about $4.17/month) for 1 vCPU, 20 GB SSD and 1 TB traffic, renewing at the same $49.99 for as long as you keep it. 👉 [See BandwagonHost's current KVM plans and prices](https://bwh81.net/aff.php?aff=77528)
> - **Flat monthly billing:** DigitalOcean's 512 MB droplet at $4/month, no renewal jump.
> - **Most hardware per euro (EU only):** Hetzner's CX21 at €7.50/month — 2 vCPU, 4 GB RAM, 40 GB NVMe.
> - **Refuse to touch a terminal?** Skip this category entirely; managed platforms like Cloudways start around $11/month.

## What "unmanaged" actually covers — and what it leaves to you

The provider's responsibility stops at the hypervisor. They keep the physical machine powered, the network up, and your VM reachable; you own everything installed inside it. There's no control panel waiting unless you install or license one, and there's no sysadmin on call.

| The provider handles | You handle |
| --- | --- |
| Hardware, hypervisor, network uptime | OS updates and security patches |
| Provisioning, billing, IP assignment | Firewall and SSH configuration |
| Replacing failed hardware | Your application stack and its config |
| Keeping the VM reachable | Monitoring, backups, and tested restores |

Support on an unmanaged plan covers provisioning, billing and network reachability. A crashed daemon, a full disk or a broken config file is yours — and most unmanaged hosts are ticket-only to begin with. The litmus test is simple: if reading `journalctl -u nginx` sounds like a normal Tuesday, you're fine. If it reads like a foreign language, buy managed and don't look back.

## BandwagonHost's KVM plans: the full current lineup

BandwagonHost's standard KVM line runs from $49.99 to $1,599.99 per year, billed annually, with no discounted intro rate — the listed price is the renewal price. Plans are managed through the brand's own panel, KiwiVM, and popular sizes periodically sell out while limited specials rotate through the catalog. The table below is the stable core lineup as listed at the time of writing; every plan renews at its listed price while the service stays active.

| Plan | vCPU | RAM / SSD | Monthly traffic | Price (billed yearly) | Buy |
| --- | --- | --- | --- | --- | --- |
| 1 GB | 1 | 1 GB / 20 GB | 1 TB | $49.99 | [ Buy](https://bwh81.net/aff.php?aff=77528) |
| 2 GB | 2 | 2 GB / 40 GB | 2 TB | $99.99 | [ Buy](https://bwh81.net/aff.php?aff=77528) |
| 3 GB | 2 | 3 GB / 60 GB | 3 TB | $149.99 | [ Buy](https://bwh81.net/aff.php?aff=77528) |
| 4 GB | 3 | 4 GB / 80 GB | 4 TB | $199.99 | [ Buy](https://bwh81.net/aff.php?aff=77528) |
| 8 GB | 4 | 8 GB / 160 GB | 5 TB | $399.99 | [ Buy](https://bwh81.net/aff.php?aff=77528) |
| 16 GB | 6 | 16 GB / 320 GB | 6 TB | $799.99 | [ Buy](https://bwh81.net/aff.php?aff=77528) |
| 24 GB | 8 | 24 GB / 480 GB | 8 TB | $1,199.99 | [ Buy](https://bwh81.net/aff.php?aff=77528) |
| 32 GB | 8 | 32 GB / 640 GB | 10 TB | $1,599.99 | [ Buy](https://bwh81.net/aff.php?aff=77528) |
| CN2 GIA-E 1 GB | 2 | 1 GB / 20 GB | 1 TB @ 2.5 Gbps | $169.99 | [ Buy](https://bwh81.net/aff.php?aff=77528) |
| CN2 GIA-E 2 GB | 3 | 2 GB / 40 GB | 2 TB @ 2.5 Gbps | $299.99 | [ Buy](https://bwh81.net/aff.php?aff=77528) |

A few things worth knowing before you pick a row:

- Standard plans let you choose among several US datacenters plus Amsterdam and Vancouver at checkout.
- The two CN2 GIA-E rows cost more for the same RAM because the routing is the product: premium Los Angeles lines aimed at China- and East Asia-facing workloads. Hong Kong locations sit on separate, pricier plans.
- Traffic is a hard monthly quota. Hit the cap and the VPS stops passing traffic until you add more from the panel or the cycle resets — no silent overage billing, but no headroom either.
- The 1 GB plan is enough for a blog, a bot, a small API or a lightweight personal service. It is not enough for a database-heavy stack or anything that compiles.
- These plans reward staying put: cancel one and you generally can't buy it back at the same price, since retired plans leave the catalog.

## What unmanaged VPS hosting costs in year three

Sticker prices are marketing; renewal prices are the product. A September 2026 comparison of 329 unmanaged VPS plans put the median entry price at $5.95/month and the median renewal at $7.99. Hostinger sits at the aggressive end: KVM 1 lists at $6.49/month on a 24-month term, then renews at $11.99 — an 85% jump. Bluehost's NVMe 2 rises a gentler 21%, from $4.69 to $5.69. DigitalOcean and Vultr skip the game with flat monthly pricing.

| Plan | Billed | Year 1 | Year 2 | Year 3 | 3-year total |
| --- | --- | --- | --- | --- | --- |
| BandwagonHost 1 GB | yearly | $49.99 | $49.99 | $49.99 | $149.97 |
| Hostinger KVM 1 | 24-mo term | $77.88 | $77.88 | $143.88 | ≈ $300 |
| DigitalOcean 512 MB | monthly | $48 | $48 | $48 | $144 |

Read that table two ways. On specs, Hostinger wins the first two years outright — 4 GB of RAM and 50 GB NVMe against BandwagonHost's 1 GB and 20 GB SSD. On trajectory, the picture flips in year three: BandwagonHost's third year costs $49.99, Hostinger's costs $143.88, and over five years the gap passes $300. DigitalOcean's 512 MB droplet is actually cheaper than BandwagonHost's plan in years two and three, but it's also half the RAM and half the storage. Hobby boxes that get rebuilt every year favor intro deals; the small server that quietly runs for half a decade favors flat renewal — which is BandwagonHost's entire model.

👉 [Check BandwagonHost's annual KVM plans and current stock](https://bwh81.net/aff.php?aff=77528)

## Backups and snapshots: the second line on the bill

Backup costs are easy to miss because unmanaged list prices rarely show them — and skipping backups on a server only you administer is how data actually dies.

Vultr's automated backups add about 20%, roughly $4 on its $20 Regular 2/4 plan. DigitalOcean's weekly backups on the 4 GiB droplet add about $4.80 to the $24 base, with daily backups closer to 30%. BandwagonHost works differently: manual snapshots through KiwiVM are included at no extra charge, so backups cost your attention instead of a recurring line item. Snapshots have slot limits that scale with the plan, and they live on the same platform as the VPS — for anything you'd genuinely hate to lose, keep an archive copy off the server too.

Whichever host you choose, budget the instance plus backups plus one tested restore before moving anything you care about onto the box. Until you've restored from it once, your backup plan is unverified.

## BandwagonHost vs Hostinger, DigitalOcean, Vultr and Hetzner

No unmanaged host wins everywhere, so here's the comparison as a set of tradeoffs:

| Provider / plan | Price | Renewal | Entry spec | Backups |
| --- | --- | --- | --- | --- |
| BandwagonHost 1 GB KVM | $49.99/yr | same | 1 vCPU · 1 GB · 20 GB SSD · 1 TB | snapshots included |
| Hostinger KVM 1 | $6.49/mo (24-mo term) | $11.99/mo (+85%) | 1 vCPU · 4 GB · 50 GB NVMe · 4 TB | weekly, advertised |
| Bluehost NVMe 2 | $4.69/mo (24-mo term) | $5.69/mo (+21%) | 1 vCPU · 2 GB · 50 GB NVMe · unmetered | — |
| DigitalOcean 512 MB | $4/mo | flat | 1 vCPU · 512 MB · 10 GB SSD | ~+20% weekly |
| Vultr Regular 2/4 | $20/mo | flat | 2 vCPU · 4 GB | ~+20% (~$4) |
| Hetzner CX21 | €7.50/mo | flat | 2 vCPU · 4 GB · 40 GB NVMe · unlimited | — |
| RackNerd 4 GB catalog | ~$24.59/mo | varies by special | 4 GB class | plan off-box |

Where each one wins: Hetzner is more machine per euro than anything on this table if Germany or Finland works for you — the tradeoff is EU-only locations and a dated panel. DigitalOcean (13 regions) and Vultr (36) are the pick when you want hourly billing, API-driven scaling and one-click resizes; that flexibility is what the monthly premium buys. Hostinger has the flashiest intro specs if you accept the year-three renewal. RackNerd competes on catalog price. BandwagonHost's niche is the small always-on box with the lowest multi-year bill, plus CN2 GIA routing if your audience sits in East Asia.

## Who shouldn't buy unmanaged VPS hosting

If your plan for a crashed server is opening a support ticket, unmanaged will frustrate you at any price. Nobody tunes your database, patches your kernel, or answers a chat at 2 a.m. — most unmanaged hosts don't even have chat. Managed hosting exists for exactly this situation; Cloudways' entry tier runs about $11/month on similar cloud hardware.

Unmanaged also assumes a baseline: Linux fundamentals, SSH, firewall rules and package updates — or a budget to hire someone who has them. One cost that surprises people: cPanel is a paid license on unmanaged platforms and wants around 2 GB of RAM to run well, which rules out 1 GB entry plans. If you need point-and-click site hosting, either budget for the license on a bigger plan or pick a host that bundles management.

## After you buy: the first-hour checklist

Once the plan is active, do these before putting anything real on the server:

1. **Patch.** Run the distro's upgrade on first login and enable automatic security updates.
2. **Harden SSH.** Install your key, keep a second session open while you test the new config, then disable password authentication. Getting locked out of an unmanaged box usually means reinstalling the OS from the panel — which wipes the disk.
3. **Set up the firewall.** ufw or nftables, default-deny, open only what the server needs.
4. **Take a snapshot.** On BandwagonHost, grab one in KiwiVM before touching the kernel or sshd; on Vultr or DigitalOcean, switch the paid backup add-on on first.
5. **Restore-test once.** Prove you can rebuild from a snapshot plus your config. Then the server is yours in the way that matters.

Two BandwagonHost-specific notes: payment is by card, PayPal or Alipay, and the stated refund policy is a full refund within 30 days of activation, limited to one refund per account. If the plan feels wrong, decide inside that window instead of at month four.

## Frequently asked questions

**Is unmanaged VPS hosting actually worth the savings?**
Yes, if you can do the maintenance yourself. BandwagonHost's 1 GB plan costs $149.97 over three years; the cheapest managed option referenced in this piece runs about $11/month, roughly $396 over the same period. The difference is your time — patching, monitoring, restores. If that's work you'd do anyway, unmanaged wins by a wide margin.

**What happens if I break the server?**
You fix it or you reinstall. Unmanaged support won't debug your configuration. On BandwagonHost you can reinstall the OS from KiwiVM in minutes, which resolves a broken sshd or firewall at the cost of the disk's contents — hence the snapshot habit above.

**Do I need a control panel?**
Only if you want point-and-click website management. On a 1 GB plan a paid cPanel license is impractical, since it needs about 2 GB of RAM; free lightweight panels or plain config files are the realistic options.

## The short answer, by situation

- **A small always-on box — blog, bot, personal service — that you'll keep for years:** BandwagonHost's 1 GB KVM at $49.99/year with flat renewal is the lowest-risk bill in this piece.
- **A 4 GB-class workhorse inside Europe:** Hetzner's CX21, and it isn't close.
- **Monthly billing, many regions, API-driven scaling:** DigitalOcean or Vultr.
- **No interest in terminals at all:** pay for managed instead; unmanaged's savings evaporate the moment you hire someone to babysit the box.

One practical last note: BandwagonHost's popular sizes do sell out, and specials rotate. If the plan you want is out of stock, take the next tier up rather than squeezing your stack into less RAM than it needs. 👉 [Check BandwagonHost's current plans, stock and prices](https://bwh81.net/aff.php?aff=77528)
