---
layout: default
title: Privacy Policy
permalink: /privacy/
---

# Crux Privacy Policy

**Effective date:** 5 May 2026
**Last updated:** 5 May 2026

Crux ("the app") is a hangboard training studio for climbers. This policy describes what data the app collects, how it is used, and the rights you have over it.

## TLDR

- The app stores your training data (sessions, force traces, benchmarks, profile) so you can see your trajectory across weeks.
- Your data is tied to an **anonymous account** issued automatically when you first launch the app. There is no email or password sign-in. The account exists only to sync your data across your devices and to scope it under access controls.
- We do **not** sell your data. We do **not** show ads. We do **not** use third-party analytics or marketing trackers. We do **not** share your data with anyone outside the providers needed to run the service.
- You can export or delete your data at any time. Contact us for either.

## What the app collects

### Data you generate
| Category | Examples | Why |
|---------|---------|------|
| Profile | Climbing discipline, grade, training goal, display name (optional), bodyweight, preferred unit (kg/lb) | Personalize benchmarks and training prescriptions |
| Training data | Sessions, individual pulls, force traces, benchmark entries, structured workout runs | Show progress, generate training reads |
| Device pairing state | Names of paired force-gauge devices | Quick reconnect; never leaves your account |

### Data the app receives automatically
| Category | Examples | Why |
|---------|---------|------|
| Anonymous user ID | UUID issued by Supabase Auth on first launch | Scope your training data so it's only readable by you |
| Crash and performance diagnostics | Stack traces, memory pressure, frame drops | Fix bugs; provided by Apple, never linked to your identity |
| Subscription receipts | Apple-managed transaction receipts for Crux Pro | Verify your subscription status; provided by StoreKit, never seen by us as raw payment data |

### What the app does NOT collect

- Email address (we don't ask for one)
- Phone number, name, location, contacts, photos
- Health data from Apple Health (no HealthKit integration)
- Marketing identifiers (IDFA, IDFV not used for tracking)
- Browsing or web activity outside the app

## Where the data lives

- **On your device**: a local SwiftData store. Survives app updates, deleted on uninstall.
- **In our cloud**: a Supabase Postgres database hosted in the European Union, with row-level security so only your anonymous user ID can read or write your rows. Used to sync data across your devices and to power AI training reads.
- **At Apple**: Apple processes your subscription transactions and crash diagnostics per Apple's privacy practices. We never receive your Apple ID, payment details, or raw device identifiers.

## How the data is used

Your data is used only to:
1. Render your training history and progress on your devices.
2. Generate AI-powered training reads about your last 12 weeks (the AI is given your training summary, not raw chat or contact data).
3. Compute benchmarks, trends, and structured workout suggestions.
4. Validate your active Crux Pro subscription.

Your data is **never** used for advertising, profiling, or sale to third parties.

## Subprocessors we rely on

| Provider | Purpose | Region |
|---------|---------|--------|
| [Supabase](https://supabase.com/privacy) | Database + Auth (anonymous accounts only) | European Union |
| [Apple StoreKit / App Store](https://www.apple.com/legal/privacy/) | Subscription billing + crash reporting | Apple's regions |
| [OpenAI](https://openai.com/policies/privacy-policy) | LLM inference for AI training reads (server-side, your raw data never leaves Supabase; only short structured summaries are sent) | United States |

We do not use ad networks, marketing automation, or behavioral analytics platforms.

## Your rights

You can:
- **Export your data**: ask us and we'll send a JSON dump of every row associated with your anonymous user ID.
- **Delete your data**: ask us and we'll delete every row in our cloud associated with your anonymous user ID. Local data is removed when you uninstall the app.
- **Cancel your subscription**: at any time via Settings → Apple ID → Subscriptions on iOS. Cancellation does not delete your training data.

Contact: **reno.quentin@gmail.com** for any privacy request.

## Children

Crux is not directed at children under 13. The app does not knowingly collect data from anyone under 13. If you believe we have inadvertently collected such data, contact us and we will delete it.

## Changes

We may update this policy as the app evolves. Material changes will be announced inside the app and dated above. Continued use of Crux after a change indicates acceptance of the new policy.

## Contact

**Quentin Renaud**
[reno.quentin@gmail.com](mailto:reno.quentin@gmail.com)
