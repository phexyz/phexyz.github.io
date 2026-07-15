---
layout: post
title: "Slopify III: the converged plan, after stress-testing every incentive"
date: 2026-07-14 00:00:00 -0400
tags: [idea]
---

This is the plan that survived adversarial review. The [pitch]({% post_url 2026-07-14-slopify %}) and the [first lifecycle design]({% post_url 2026-07-14-slopify-lifecycle-and-incentives %}) made a clean claim: every actor's self-interest points the same way, toward an honest graduation. Then the design got attacked, mechanism by mechanism, against how real systems actually behave. The first attack was fatal and rewrote the core. What follows is the version that holds — and an honest list of what still doesn't.

## The thesis (unchanged)

Anyone vibe-codes a slop app and ships it live behind a shared login. Others bet on it. The bet has a fundamental, because to judge a slop app you have to open and use it — so speculation and real usage are the same action, and the price chart is an unfakeable-at-scale traction signal. That signal is what a VC would pay to find first. Winning apps graduate to a real round; the people who bet early cash out. `slopify.show` is the showcase, `slopify.ventures` is the market.

## The unit and legal structure — the decision the review forced

The v1 answer was "make the unit a security sold under Regulation Crowdfunding." **That is dead.** Reg CF imports Rule 501's **12-month resale lockup** — the exact rule Wefunder, Republic, and StartEngine operate under — which structurally forbids the continuous secondary trading that *is* the product. You cannot run a live bonding curve on an instrument nobody may resell for a year. The whole unit choice had to reopen.

The resolution is to stop forcing one instrument to be both the casino chip and the equity, and **split it into two layers** — exactly how real markets already separate a continuously-traded derivative from the locked, private equity underneath it.

**Layer 1 — Slop Contracts (the always-on market).** The tradable unit is a **milestone/event contract** — "will this app graduate to a priced round by date T" — priced continuously, operated as (or on the rails of) a **CFTC-regulated event market**, the Kalshi model. It is legal as a *market*, not gambling, because the line is function not branding: the contract carries a real information signal (verifiable usage/retention), so it is a commodity contract, not a house wager. Holders own a contract, not shares — which is what makes it freely tradable with no securities lockup.

**Layer 2 — Graduation Equity (the exit).** Graduation is a real **Reg D 506(c) priced round** to accredited VCs — ordinary startup financing, no retail-lockup problem, because it is primary issuance plus an optional secondary. Each app is a **series under a platform master LLC**, so forming the fundable entity is one click, not a law firm.

**The bridge — how Layer 1 holders cash out when the VC invests.** At graduation the Slop Contracts settle. YES-holders get paid from a settlement pool funded by two sources: the losing (NO) side of the contract market, and a **graduation bonus** the company/VC pays in as the price of the traction the market manufactured. Contract-holders who want continued upside roll winnings into the app's series equity (via a pooled Reg A+ vehicle for non-accredited holders, or directly into the 506(c) round if accredited).

This is the spine of the final plan: **continuous speculation lives where continuous trading is legal (event contracts); the equity exit lives where equity is legal (Reg D at graduation); a settlement bridge connects them.**

## The lifecycle, with each actor's aligned incentive

| Stage | What happens | Builder | Early buyer | Player | VC | House |
|---|---|---|---|---|---|---|
| **1. Mint** | Builder describes app; platform generates, hosts it behind shared login; builder must **stake** to list. | Only lists if they believe; stake = skin in game | — | — | — | Stake is a free spam filter |
| **2. Curve** | App lists; Slop Contracts trade on a continuous curve. Judging it means using it. | Earns trading fees on volume | Cheap early entry into a real contract | Cheap thrill *and* a real app to use | Watches a usage-backed signal | Rake on every trade |
| **3. Flywheel** | Most-traded apps get most placement; ranking is **retention-weighted**, not launch-hype. | Must build for retention, not just launch loud | Position appreciates as real users return | Surfaced the apps worth the money | Signal sharpens into a shortlist | More volume, more rake |
| **4. Anti-manip** | Bets keyed to verified identity; retention-weighting; platform sees identity+usage+money in one place. | Legit stake protected; alts detected | Fair game, not racing fake pumps | Not rigged | A board it can trust | Trust preserved = longevity |
| **5. Graduation** | App clears a retention+usage threshold → **506(c) round**; contracts settle; holders paid from the pool. | Growth capital, keeps majority | **Cash-out** — the whole point | Bragging rights, winnings | De-risked deal, live traction proof | **Carry** on the round + settlement |
| **6. After** | Builder upside **vests through on-platform graduation**; graduated equity registered with platform as transfer agent. | Paid *most* by graduating here; free to grow | Winnings out, or rolled into real equity that survives builder exit | — | Clean cap table via series LLC | Keeps transfer-agent + market relationship |

Read the columns: at every stage each actor's best move also serves the others, and all five want graduation to happen — and to happen *honestly*, because the value only exists if the signal was real.

## Mechanisms borrowed, and for what

| Borrowed from | Used for |
|---|---|
| **pump.fun** | Bonding-curve price discovery; burned-LP principle (make value structurally un-strandable); realistic ~1% graduation rate as the base case |
| **Kalshi / CFTC event contracts** | The tradable unit; the function-not-branding defense against "this is gambling" |
| **Reg D 506(c)** | The graduation round — accredited, no lockup, standard VC financing |
| **Series LLC** | One-click fundable entity per app, so securities formation isn't per-app legal work |
| **Republic** | Transfer-agent + secondary-market operator role as the platform's moat |
| **Reg A+ Tier 2** | Pooled vehicle to let non-accredited winners roll into equity without per-app filings |
| **App Store notarization** | Safety moderation of apps shipped under the shared login |

## Residual risks that survived the review (not solved — stated plainly)

1. **The regulatory stack is heavy, and it fights the vibe.** A CFTC event market + Reg D + series LLC + transfer/settlement infrastructure is a licensed fintech, not a weekend project. "Anyone ships slop in an afternoon" collides head-on with derivatives and securities compliance. Best mitigation: rent licensed rails (Kalshi-type partner for contracts, a broker-dealer ATS for equity) instead of building them. It is still the biggest obstacle by far.
2. **State gambling regulators.** Even CFTC-legal, the "gamble on slop" framing invites state cease-and-desists — exactly what Kalshi-style products are fighting now. The federal/state conflict is unresolved industry-wide; branding on the market side of the line is necessary but not obviously sufficient.
3. **The settlement pool is a knife-edge parameter.** If YES-holders are paid mostly by NO-holders, it is zero-sum gambling with extra steps and the "fundamental" evaporates. If they are paid mostly by the company/VC bonus, that cost suppresses valuations and can deter graduation. There is a funding mix that works; it is narrow and unproven.
4. **The oracle conflict.** "Did it graduate" and "what is the real retention" must be measured by a trusted source — but the platform is simultaneously the market operator, the metric oracle, and the rake-taker. That is a conflict of interest at the exact point the whole signal depends on. Needs independent or cryptographically-auditable metrics, or the signal is manipulable at its source.
5. **Wash-trading still prices a real signal.** Identity + retention-weighting raises the cost of faking, but a funded builder can buy genuine sybil-resistant usage. Real money now bets on the chart, so the incentive to corrupt it scales with the prize. The signal is only ever as good as the anti-collusion layer.
6. **The median experience is losing money on slop.** ~99% never graduate; their contracts expire worthless. That is disclosed and fine in principle, but it means player retention — not app retention — is the actual survival question, and it rests on whether slop is entertaining enough to keep people paying to lose. Unproven.
7. **Four-sided cold start.** Needs licensed rails, VCs, builders, and players at once. Harder than a normal two-sided marketplace; probably requires hand-seeding a few genuinely funny apps and a few committed funds before any flywheel turns.

## Verdict

**Buildable — but only as a licensed fintech wearing a meme coat.** The "vibe-code and gamble" surface hides a securities-and-derivatives exchange, and the honest version of this company spends its first year on licensing and partnerships, not on the fun part. The two-layer structure is what makes it legally coherent; without it, the Reg CF lockup or the gambling classification kills it outright.

**The single riskiest bet:** that the two-layer structure is actually permissible at retail scale in the US without being shut down by the CFTC, the SEC, *or* state gambling regulators — *and* that enough apps genuinely graduate to keep "front-run a seed round" from decaying into "pay to lose money on slop." Everything else is engineering. That one is existential, and it will not be known until a regulator responds to the real thing.

---

### Adversarial log — what the plan survived

| # | Attack | Grounded in | Outcome |
|---|---|---|---|
| 1 | Reg CF's 12-month resale lockup forbids the continuous secondary trading that is the product | Regulation Crowdfunding Rule 501 (Wefunder/Republic/StartEngine) | **Fatal — patched.** Unit split into CFTC event contracts (tradable) + Reg D equity at graduation |
| 2 | "Gamble on slop" is unlicensed gambling under state law | Kalshi state cease-and-desists; function-not-branding test | Mitigated (market not house), residual state risk retained |
| 3 | Settlement pool funded by losers = zero-sum gambling, not a real exit | Prediction-market payout structure | Patched with a graduation-bonus funding source; parameter flagged as knife-edge |
| 4 | Platform is market-maker, oracle, and rake-taker — conflict at the signal source | Exchange/oracle separation norms | Unsolved — flagged, needs auditable metrics |
| 5 | Wash-trading now prices a real VC signal, so manipulation pays real money | pump.fun volume-faking | Mitigated (identity + retention-weighting), residual retained |
| 6 | Per-app securities filings are impossible at slop volume | Reg A+ / series-LLC practice | Patched with series LLC + pooled vehicle |
| 7 | Builder-flight strands holders once popular | pump.fun graduation; transfer-agent model | Patched: vested-on-platform upside + graduated equity survives exit |
| 8 | Four-sided cold start | Two-sided-marketplace failure literature | Unsolved — flagged, hand-seed strategy only |

*Convergence note: attacks 1, 3, 6, 7 forced concrete mechanism changes; 2, 4, 5, 8 are residual risks the design cannot fully close and does not pretend to. A live codex-as-verifier pass ([handoff prompt in `_drafts`](https://github.com/phexyz/phexyz.github.io/tree/main/docs/_drafts)) would push further, but the load-bearing fix — the two-layer instrument — is in.*
