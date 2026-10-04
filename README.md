# Reprise

**Give failed payments a second conversation.**

A planned merchant recovery console for failed autopay payments: a voice agent understands the customer's situation, offers an appropriate next step, and leaves a verifiable action trail.

Built for Razorpay's Forward-Deployed Engineer assignment, option 2: a voice agent for autopay recovery using 10 fictional customer records.

## Status

Planning complete; implementation has not started. This repository currently contains the product and engineering plan, not a working application. Do not submit it as a completed assignment yet.

[Read the build plan](docs/BUILD_PLAN.md) · [Provider setup](docs/PROVIDER_SETUP.md)

## Planned demo

1. Select one of 10 fictional customers in the recovery queue.
2. Call a single privately configured, explicitly permitted test number through Bolna.
3. Have a real voice conversation about the fictional failed payment.
4. Create a simulated payment link, request a callback, record an opt-out, or queue human review.
5. Complete the simulated payment page and see the ledger update.
6. Inspect call status, transcript, tool results, and outcome evidence.

Voice and phone transport will be live. Payment collection and message delivery will be explicitly simulated. A successful one-off recovery will not imply that an autopay mandate has been repaired.

## Planned implementation

TypeScript, Next.js, Tailwind CSS, SQLite, and a small Bolna API adapter. A fixture mode will let reviewers explore the app without provider credentials; a live mode will demonstrate the actual phone workflow.

Setup/run commands, verified test results, screenshots, and a recorded demonstration will be added after implementation. Private API keys, test phone numbers, provider payloads containing phone numbers, and local databases must never be committed.

## Prior work

The implementation will draw on engineering patterns from [Duet](https://github.com/mssharatchandra/duet): interruptible voice interaction, deterministic action gates, idempotent side effects, and inspectable evaluation. It will use Bolna for the assignment's voice-agent-provider and telephony requirements instead of depending on Duet's unfinished phone adapter.
