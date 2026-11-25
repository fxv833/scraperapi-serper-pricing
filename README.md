# Serper Alternative: What ScraperAPI Costs per 1,000 Google Searches, Which Plan Fits Your Volume, and When Switching Isn't Worth It (Full Pricing Table)

Serper charges $1.00 per 1,000 searches on its $50 pack, covers Google only, and returns no AI Overview. ScraperAPI is the alternative most Serper users end up evaluating once they also need product pages, and it bills on a different mechanism: a Google or Bing SERP request costs **25 credits**, so the $49 Hobby plan buys 4,000 searches, or **$12.25 per 1,000**. That number decides most of what follows, which is why this starts with cost math instead of a feature list.

Below are all ScraperAPI plans with the prices readable on its pricing page in October 2026, the effective per-1,000 cost for each request type, a list-price comparison against Serper and five other APIs, and the cases where you should keep Serper and add something else.

> **Short version:** ScraperAPI makes sense if you need Amazon, Walmart, eBay or anti-bot pages *and* Google/Bing results from one API and one invoice. If all you want is cheaper Google SERPs, it moves you the wrong way: **$12.25/1k on Hobby against Serper's $1.00/1k**. The free plan gives 1,000 credits a month, 5,000 for the first seven days, and there is a 7-day no-questions refund.
> 👉 [See every ScraperAPI plan and the credit cost per domain](https://www.scraperapi.com/pricing/?fp_ref=coupons)

## Serper's baseline, so the comparison has a floor

Serper is a prepaid-credit API: **$50 buys 50,000 searches** ($1.00/1k), $375 buys 500,000, and the advertised **$0.30/1k only unlocks with $3,750 upfront**. Credits stay valid for **6 months**, and new accounts get **2,500 free queries**.

Throughput is tied to the pack size. The $50 tier allows **50 queries per second**; the 300 QPS default ships with the $3,750 tier, and higher limits go through sales. Endpoints cover Google web, Images, News, Maps, Places, Videos, Shopping, Scholar, Patents and Autocomplete, in 100+ countries. There is no Bing, DuckDuckGo, Yahoo, Baidu, Yandex, Amazon or YouTube endpoint, and no AI Overview field at any price.

So the bar for any Serper alternative is simple: beat $1.00/1k for Google results, or give me something Serper structurally cannot return. ScraperAPI fails the first test and passes the second, depending on your workload.

## Every ScraperAPI plan, and what each one is actually for

ScraperAPI sells monthly credit allowances with a concurrency cap attached. Annual billing takes exactly **10% off** the monthly rate, and annual plans hand you **the full year's credits upfront**, usable on any timeline, with an early renewal available if you burn through them.

| Plan | Credits per month | Concurrent threads | Price | Best for | Get started |
| --- | --- | --- | --- | --- | --- |
| Free | 1,000 (5,000 for first 7 days) | 5 | $0 | Testing the domain cost estimator on your own URLs | [Start free](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Hobby | 100,000 | 20 | **$49/mo**, or $44.10/mo annual ($529.20/yr) | Solo projects: ~4,000 Google SERPs or 20,000 Amazon pages | [Open Hobby](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Startup | 1,000,000 | 50 | Quoted on the pricing page | Apps that outgrew Hobby but still target US/EU | [Open Startup](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Business | 3,000,000 | 100 | Quoted on the pricing page | First tier with country-level geotargeting and unlimited analytics history | [Open Business](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Scaling | 5,000,000 | 200 | Quoted on the pricing page | First tier with pay-as-you-go overage | [Open Scaling](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Professional | 10,500,000 | 300 | Quoted on the pricing page | Continuous high-volume pipelines | [Open Professional](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Advanced | 21,500,000 (limited-time +500K bonus) | 500 | **$1,975/mo**, or $1,777.50/mo annual ($21,330/yr) | Multi-source data pipelines with priority routing | [Open Advanced](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Enterprise | 22,000,000+ | 500+ | Custom quote | Volume contracts and custom concurrency | [Request Enterprise pricing](https://www.scraperapi.com/pricing/?fp_ref=coupons) |

Two things in that table matter more than the sticker prices. First, Hobby and Startup cap geotargeting at **US and EU**; country-level targeting starts at Business. Second, unused credits on a monthly plan are lost at renewal rather than carried forward, which is the opposite of Serper's 6-month credit life and worth thinking about if your usage is seasonal.

I quoted Hobby and Advanced because those are the two prices readable on the pricing page during the October 2026 check. Startup, Business, Scaling and Professional are priced by credit volume on the same live page, and every link above lands on it.

## The credit multiplier is the entire pricing story

ScraperAPI does not have a per-request price. It has a per-domain credit cost, multiplied by your plan's credit rate. That single design choice produces wildly different effective rates:

| What you scrape | Credits per request | Requests on Hobby ($49) | Effective cost per 1,000 |
| --- | --- | --- | --- |
| Standard web page | 1 | 100,000 | **$0.49** |
| Amazon, Walmart, eBay | 5 | 20,000 | **$2.45** |
| Google or Bing SERP | 25 | 4,000 | **$12.25** |
| LinkedIn | 30 | 3,333 | **$14.70** |

Add-ons stack on top: bot-protection bypass (Cloudflare, DataDome, PerimeterX/HUMAN, Akamai) adds 10 credits, `render=true` adds 10, premium proxies add 10, and premium proxies plus rendering together cost 25. A rendered Google SERP is therefore 35 credits, not 25.

Scale changes the picture but does not flip it. On Advanced at $1,975 for 21,500,000 credits, a Google SERP works out to **$2.30 per 1,000** and a standard page to roughly **$0.09 per 1,000**. That is competitive against SerpApi's $3.75/1k top tier and DataForSEO's $2.00/1k live rate. It is still more than double Serper's $1.00.

The practical read: ScraperAPI is an economical page-scraping API that also happens to return Google and Bing results. If SERP is 90% of your traffic, you are paying scraping-API prices for search data. Two controls make this manageable. Every response carries an `sa-credit-cost` header showing exactly what that request burned, and the dashboard's Domain Cost Estimator prices a URL before you send it; `max_cost` caps any single request. 👉 [Start on the $49 Hobby plan and run your own URLs through the estimator](https://www.scraperapi.com/pricing/?fp_ref=coupons)

## What you get that Serper cannot return

The reason to pay 12x Serper's SERP rate is the rest of the API. ScraperAPI handles Amazon, Walmart and eBay pages, bypasses bot protection that would otherwise serve you a challenge page, renders JavaScript, takes screenshots, and keeps sessions and geotargeting in the same request. Serper returns search results and nothing else, so a team doing SERP monitoring plus competitor product scraping runs two vendors, two invoices and two failure modes. Consolidating that is the actual pitch.

Three limits are worth knowing before you commit:

- **Concurrency is measured in threads, not queries per second.** Hobby's 20 threads is not 20 QPS, so do not compare it directly with Serper's 50 QPS. Measure under your own latency.
- **Over-limit requests are refused, not billed.** You get a 429 and the request is turned away. That is good for the bill and bad for the pipeline. Auto-upgrade, which bumps you to the next plan when credits run out, is available on Hobby through Professional. Pay-as-you-go at a fixed per-credit rate, with a monthly spending cap, starts at Scaling. 👉 [Check which plans include pay-as-you-go](https://www.scraperapi.com/pricing/?fp_ref=coupons)
- **The 7-day refund is genuinely unconditional.** No questions asked, and you can cancel any time from the dashboard without a cancellation charge. That is enough time to run a real sample of your URLs and check the parse quality against your schema.

## How the field compares on list price

All figures below are published list prices checked in October 2026, not quotes, and none of these providers has been benchmarked head to head here for latency or success rate.

| Provider | Billing | Free allowance | Entry rate per 1,000 | Engines |
| --- | --- | --- | --- | --- |
| Serper | Prepaid credits, 6-month life | 2,500 queries | $1.00 at $50; $0.30 at $3,750 | Google only |
| PrismCrawl | Prepaid credits, 90-day life | 100 credits | $0.30 at $5; $0.15 at $1,000 | Google, Bing + 10 others |
| Searlo | Prepaid credits | 3,000 credits | $0.80 at $3.99 | Google only |
| SerpApi | Monthly plans | 250 searches | $25.00 at $25/mo; $3.75 at $3,750/mo | Google + others |
| DataForSEO | Prepaid balance | Not listed | $0.60 standard queue; $2.00 live | Google, Bing + SEO data |
| Exa | Prepaid | $10/month + $10 signup | $2.50 keyword; $7 with page content | Own neural index |
| Tavily | PAYG or plans | 1,000 credits/month | $8.00 PAYG; $5–$7.50 on plans | Web search for LLMs |

At identical volumes the gap is stark: 50,000 searches cost **$15 on PrismCrawl, $29.99 on Searlo and $50 on Serper**; 500,000 cost **$110, $199.99 and $375** respectively. If pure Google SERP volume is the whole job, those three are the price floor and ScraperAPI is not in that conversation.

Note the credit-expiry column, because it is where cheap packs quietly get expensive. PrismCrawl credits last 90 days, Serper's last 6 months, ScraperAPI's monthly allowance resets to zero at renewal. Buying a year of searches you will not finish is a discount that evaporates.

## Which setup fits your case

**Google only, under ~100,000 searches a month.** Stay on Serper's $50 pack or move to Searlo at $0.80/1k. ScraperAPI Hobby would give you 4,000 SERPs for the same $49, and the only thing you would gain is the rest of the scraping stack.

**You need Bing, YouTube, Amazon or Walmart pages.** This is where ScraperAPI earns its rate. A single API covering Google and Bing SERPs plus Amazon, Walmart and eBay pages, with bot-protection bypass included, removes one vendor and one integration. Price the mix rather than the headline: 60% Amazon at 5 credits and 40% Google at 25 credits lands near 13 credits per request.

**You need structured AI Overview data.** Serper does not return it at any price, and ScraperAPI's SERP endpoint is built for scraping result pages rather than parsing AI Overview blocks into fields. SerpApi and cloro both publish parsed AI Overview support; verify the shape on a real query before you migrate a pipeline.

**Budget is near zero and you can host it.** FreeSearch is MIT-licensed, self-hosted, needs no API key and imposes no quota, querying DuckDuckGo, Brave, Bing, Yahoo and Wikipedia in parallel and merging results with Reciprocal Rank Fusion. Read its own documentation on the limits, though: upstream engines rate-limit per IP, the Mojeek engine has strict CAPTCHA behaviour, the Google engine is flagged experimental and works best behind proxies, and automated querying may conflict with some engines' terms of service. Its maintainers recommend official APIs for heavy commercial use. Free is real until you need reliability.

## FAQ

**Does Serper have a free tier?**
Yes, 2,500 queries on signup, consistent across the pricing checks from May and October 2026. Confirm on the pricing page before relying on it, since trial sizes change.

**Does Serper support Bing?**
No. Google web, Images, News, Maps, Places, Videos, Shopping, Scholar, Patents and Autocomplete only. Any Bing, YouTube or Amazon requirement means a second provider.

**Is ScraperAPI cheaper than Serper for Google results?**
No. On Hobby a Google SERP costs 25 credits, which is $12.25 per 1,000. It only reaches $2.30/1k at the $1,975 Advanced tier. ScraperAPI is cheaper per *page*, not per *search*.

**Will the low concurrency cap throttle me?**
Hobby's 20 concurrent threads will bottleneck a high-QPS crawler well before the credit allowance runs out. If you push more than roughly 100 requests per second, look at custom plans rather than the standard tiers.

**Do ScraperAPI credits expire?**
Monthly credits reset at each renewal and unused ones are lost. Annual plans are different: you receive the full year's credits upfront and can spend them on any schedule, with early renewal available if you run out.

**What happens when I hit the limit mid-month?**
A 429 response, with no overage charge. Auto-upgrade moves you to the next plan on Hobby through Professional; pay-as-you-go with a spending cap is available from Scaling upward.

## Before you enter a card

Run three things first. Price ten of your real URLs through the Domain Cost Estimator so you know your actual credits per request rather than the generic 25 for SERPs. Decide whether your usage is flat enough for an annual plan, since the 10% saving only pays off if you will spend the upfront credits within the year. And confirm what happens at your ceiling, because a 429 mid-crawl costs more in engineering time than a slightly larger plan.

If the estimator says your workload is mostly pages, ScraperAPI will undercut what you are paying now. If it says mostly Google SERPs, you already have the cheaper option. 👉 [Compare ScraperAPI plans and start with the free credits](https://www.scraperapi.com/pricing/?fp_ref=coupons)
