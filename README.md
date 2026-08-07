# SST Trigger Environment

A minimal static test harness deployed via GitHub Pages, used to validate that the GTM Web Container (`GTM-TTZ2JRGD`) correctly fires a purchase event into the Server-Side Tagging pipeline built in [`shopify-ga4-mass-balance-monitor`](https://github.com/anijic/shopify-ga4-mass-balance-monitor).

This is a validation tool, not a production system. It exists solely to confirm that a client-side `dataLayer.push()` purchase event is captured by the GTM Web Container and forwarded through the deployed SST proxy.

**How it works:**
- Loads the GTM Web Container snippet.
- Displays a "Fire Test Purchase Event" button.
- On click, pushes a synthetic `purchase` event with a test transaction ID (`SST-TEST-*`) to `dataLayer`.
- Used with GTM Preview/Tag Assistant to confirm the event reaches the Server Container.

See the [SST case study](https://github.com/anijic/shopify-ga4-mass-balance-monitor/blob/main/CASE_STUDY_SST_PROXY.md) for the full validation evidence produced using this environment.
