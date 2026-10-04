# Bolna setup for the owner

Use Bolna first because you have used it before and its documentation supports shared-number test calls to Indian destinations. No new carrier account or dedicated purchased number is assumed for the initial demonstration.

1. Sign in to [Bolna](https://platform.bolna.ai/) and confirm your account can use API calls and has sufficient calling credits.
2. In Agent Studio create a temporary test agent. Choose a managed/default English voice pipeline so we can test transport before tuning models. Turn off automatic retries for this test.
3. Use **Get a call from agent** / the Test dropdown. Select an available shared Bolna number and call only your own phone with its country code. Confirm that you can hear and respond to the agent. This checks account/destination access; it is not the finished assignment demonstration.
4. Generate an API key privately. Once the application scaffold exists, put it in its ignored `.env.local` alongside the agent ID and the single permitted test destination. Do not paste credentials or your phone number into chat, code, screenshots, or GitHub.
5. We will supply the recovery prompt and tool configuration, replace the temporary agent configuration, and configure the local HTTPS tool/callback endpoint during implementation.

Expected application configuration names:

```dotenv
BOLNA_API_KEY=
BOLNA_AGENT_ID=
DEMO_PHONE_NUMBER=
APP_BASE_URL=
PROVIDER_TOOL_SECRET=
OPERATOR_TOKEN=
```

These are proposed names; verified implementation instructions will replace this section after the app is built.

If your account cannot use a shared number or call your destination, note the exact provider error without sharing secrets. Do not spend the build window provisioning a dedicated India number or a new carrier account; those can introduce approval delays. We will reassess assignment 3 rather than claim browser-only speech is a completed phone demonstration.

Official references: [outbound test calls](https://www.bolna.ai/docs/outbound/making-calls), [custom tools](https://www.bolna.ai/docs/tool-calling/custom-function-calls).
