# Project: Cinema Cabbage

## Overview
A minimalist web project ("practicing project") designed to showcase content from the Thomas Grasha YouTube channel. The focus is on a clean, high-impact landing page leading to a dynamic video player.

## Collaboration Style (User Preferences)
- **Communication Pattern**: Direct, punchy, and action-oriented.
- **Preference**: Skip the fluff and "small talk." Mirror the user's brevity.
- **Workflow**: Prioritize execution and "doing" over theorizing or long-winded explanations.
- **Tone**: Senior-to-senior, technical, and efficient.

## Project Structure
- `src/pages/index.astro`: Entry point with a full-screen hero background.
- `src/pages/manifest.astro`: Dedicated video player page.
- `src/layouts/Layout.astro`: Shared layout component.
- `src/styles/global.css`: Global styles using Vanilla CSS and Roboto typography.
- `public/3434.jpg`: Hero background asset.
- `YOUTUBE_PLAN.md`: Technical specification for the Random Video feature.

## Technical Conventions & Goals
- **Framework**: Astro (SSG).
- **Styling**: Prefer Vanilla CSS (scoped or global) and Flexbox. Keep the UI minimalist and cinematic.
- **Dynamic Content**: Replace the static iframe in `manifest.astro` with a random video fetcher using the YouTube Data API v3.
- **Security**: API keys must be restricted via HTTP Referrer in the Google Cloud Console.

## Roadmap & Pending Tasks
- [x] Improve mobile responsiveness.
- [ ] Integrate Google Gemini into `t3code` monorepo. (REVERTED)
    - [ ] Fix type errors in `@t3tools/shared` and `@t3tools/web`.
    - [ ] Update `GeminiAdapter` to Effect v4 and ADK v0.6.
    - [ ] Add Gemini support to `ProviderRegistry` and `SettingsPanels`.
    - [ ] Pass `bun typecheck` across the monorepo.
    - [ ] Verify server startup with Gemini settings.
- [ ] Set up Google Cloud Project and enable YouTube Data API v3. (PAUSED)
- [ ] Implement the random video selection logic in `manifest.astro`. (PAUSED)

## Last State Checkpoint (2026-04-17)
- **Focus**: T3 Code Gemini Integration Re-attempt.
- **Status**: Attempted to finalize the integration (tool-calling, orchestration, git text generation). Encountered persistent runtime issues including ADK session lifecycle race conditions and PubSub API mismatches in Effect v4. All changes were reverted to a stable state (`df9d3400`) after the implementation failed to produce responses in the UI.
- **Next Up**: UI enhancements or resuming the YouTube API integration. Investigative notes on the Gemini crash are available in the session history.

---
*Note: This file is the primary source of truth for project context and collaboration standards.*
