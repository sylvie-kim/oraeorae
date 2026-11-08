# OraeOrae 🐾

**OraeOrae turns daily care for my two Pomeranians from *typing* into *confirming*: one tap logs both dogs' usual day, and weight, health records and spending sit in one place.**

I'm a non-developer dog owner, and I built this with AI coding agents for my own dogs, Leo and Ami. *Orae-orae* means “for a long, long time.” One of them has hypothyroidism and both have skin issues, but weight, diet, medication and vet notes lived in different places, so I could not see what was actually changing. It started from my own needs as their owner, not from a product idea.

This repository is an overview; the source code stays private.

<p>
  <a href="https://oraeorae-4mnbzwnkgq-uc.a.run.app"><b>▶ Try the live app</b></a>
  &nbsp;·&nbsp; tap <b>🐾 로그인 없이 둘러보기</b> (“look around without logging in”) on the first screen
</p>

![First screen with the look-around button, the guided demo home, and the yearly checkup comparison](images/tour.png)

The app screens are in Korean. Button names are quoted as they appear on screen, with an English translation.

**Who this is for:**
- **Me, first** — I use it every day for Leo and Ami.
- **Owners of more than one dog** — weights side by side, one shared supplement list, one switch to log the same thing for all dogs.
- **Anyone curious** — the demo is open to everyone, no account needed.

## What OraeOrae is for

- **Logging that doesn't get dropped.** Save a normal day once, tap one button each day, and fix only what was different.
- **Seeing what changes their weight.** Food, treats, walks and supplements are logged next to weight, against a goal line.
- **Reading health over the years.** Each yearly checkup sits next to the years before, with a written comparison.
- **Knowing where the money goes.** This month against last month, split by dog or shared items.

## Quick start

1. Open the [live app](https://oraeorae-4mnbzwnkgq-uc.a.run.app).
2. Tap **🐾 로그인 없이 둘러보기** (“look around without logging in”).
3. On Home, tap **🐾 오늘도 평소대로** (“same as usual today”).
4. Open the **건강** (“health”) tab to see two years of sample checkups side by side.

That's the core. The rest of the tabs are in the tour below.

## See it work

```
You:      Back from a walk. Tap 🐾 지금 산책 다녀옴 ("back from a walk").
OraeOrae: Logs a walk for the current time of day, with each dog's usual minutes.

You:      Tap 🐾 오늘도 평소대로 ("same as usual today").
OraeOrae: Fills in both dogs' meals, walks and supplements.
          Tap it twice: still no duplicates.

You:      Open 오늘 ("today"). Change only what was different.
          Enter both dogs' weights side by side.

You:      Upload this year's checkup sheet (photo or PDF) in 건강 ("health").
OraeOrae: Reads the values and compares them year over year.

You:      Scan a receipt in 비용 ("expenses").
OraeOrae: Fills in the expense and splits this month by dog.
```

Checkup reading and receipt scanning work in a signed-in account; they are off in the shared demo.

<img src="images/demo.gif" alt="Tap 'back from a walk' to log a walk, then 'same as usual today' to fill in both dogs' meals and supplements; the expenses tab shows this month split by dog" width="300" />

Typing every meal and walk for each dog is why I stopped logging before. Here, the day is already filled in; I only confirm it.

## How it flows

**Usual day saved once → one tap each day → fix what was different → weight, health and spending trends**

| Tab | Works like | What it does |
|---|---|---|
| Home | **A routine keeper** | **🐾 오늘도 평소대로** fills in each dog's usual food (in grams), walks and supplements. **🐾 지금 산책 다녀옴** logs a walk. |
| **오늘** (“today”) | **A daily logbook** | Change only what was different; both dogs' weights side by side. |
| **체중** (“weight”) | **A weight coach** | Trend chart, target line, change since the last weigh-in. Daily coach cards suggest a next step from the last 7 days of weight, food and walks (Gemini, with a rule-based fallback). |
| **건강** (“health”) | **A records folder** | Yearly checkups side by side, a trend chart per value, medications, vaccines, vet visits, and skin photos by body part. |
| **비용** (“expenses”) | **A household bookkeeper** | Receipt scan, monthly comparison, per-dog filter, category breakdown, 6-month trend. |

![OraeOrae screens: one-tap routine and walk, daily log, weight trend, expenses by month and by dog](images/screens.png)

It installs on a phone (PWA) with Google sign-in.

> Coach cards and checkup summaries are for reference only and do not replace a veterinarian.

## About the demo

- The demo shows Leo and Ami's **real photos and weights**, shared on purpose. Meals, walks, medications, two years of checkups, and expenses are **sample data**, labelled as such.
- Everyone shares one demo account, so new records from other visitors may appear. You can add records and use the one-tap buttons, but not edit or delete them. Leo and Ami's profiles and weights are read-only. Photo uploads, receipt scanning, and AI analysis are off there.

## How it's built

- Solo, non-developer owner, building with AI coding agents such as Claude Code. First attempt in 2025, rebuilt from scratch on Google Cloud in June 2026.
- Every change goes through a pull request with type checks, unit tests, and a build in CI; merging deploys automatically.
- Stack: TypeScript · React · Vite · Tailwind · Express · PostgreSQL (Drizzle) · Gemini · Google Cloud Run, Cloud SQL, Cloud Storage · GitHub Actions

## Status

- Live and used for Leo and Ami. Sign-ups are invite-only; the demo is open to everyone.
- Goal: make the health history easy to share with a new vet. This is not built yet.

---

Confirm, don't type, so the record keeps going for a long, long time.
