# Contributions and source provenance

This release contains the Arosa source snapshot at `676d4f02d4e04c556a81e275b59ab0e97ad64ee0`. Arosa existed before the hackathon. The baseline is `588d8c2`, the last source commit before October 27, 2026 in Eastern time. The event building window runs October 27 through November 4.

## New public-release work

- Complete application source publication with an MIT license, setup instructions and third-party notices.
- Independent provider configuration for general, Modeling and Underwriting research, with tests.
- Explicit web administrator configuration and synthetic replacement of the production-derived report fixture.
- Startup requirements, provider migration checklist and architectural demo guide.

## Demonstration attribution

- **Pre-existing foundation:** zoning tools, Underwriting, floor-plan editor, IFC/Pascal exchange and the scripted Blender/Bonsai worker. Do not present these as newly authored during the event.
- **New Meta integration:** independent Modeling research with Muse Spark (`acres-research/meta.mjs`, `service.mjs`, and `research.mjs`), and selection-guided SAM/Muse Image workflows (`meta-visual.mjs` and the photo UI).
- **New architectural presentation:** plan-aware interior illustration, improved walkthrough materials/lighting and licensed architectural assets, followed by black-frame recovery, interaction, timing and phone performance changes in `app-starter/frontend/` and `app-starter/public/architecture-assets/`.
- **New full-source release:** the publication, independent general/Underwriting Meta routing, removal of implicit public administrators, and documentation identified above.

The video should demonstrate the new agent using the existing architectural tools, and the new walkthrough behavior. Verify a real Meta run before recording any narrated agent action. A file appearing in the table below does not make all of its older behavior eligible as new work.

## Event-window product work

The table below is generated from the baseline-to-snapshot Git diff. Added and modified describe source history, not a claim that every feature in a modified file was new. Pascal and Blender existed before the event; the demo must highlight event-window changes to their workflow.

| Source path | Change since baseline |
|---|---|
| `acres-research/README.md` | Modified |
| `acres-research/alerts.mjs` | Modified |
| `acres-research/alerts.test.mjs` | Modified |
| `acres-research/architecture-tools.test.mjs` | Modified |
| `acres-research/architecture.test.mjs` | Modified |
| `acres-research/assembly-topology.test.mjs` | Modified |
| `acres-research/assembly.mjs` | Modified |
| `acres-research/capabilities.mjs` | Modified |
| `acres-research/capabilities.test.mjs` | Modified |
| `acres-research/citation-claims.test.mjs` | Modified |
| `acres-research/city-closed-sales.test.mjs` | Modified |
| `acres-research/codex.mjs` | Modified |
| `acres-research/comparable-pool.test.mjs` | Modified |
| `acres-research/comparable-price.test.mjs` | Modified |
| `acres-research/deal-search-evidence.test.mjs` | Modified |
| `acres-research/deal-tool-costs.test.mjs` | Modified |
| `acres-research/deal-valuation.test.mjs` | Modified |
| `acres-research/deck-freshness.test.mjs` | Modified |
| `acres-research/deliverable.mjs` | Modified |
| `acres-research/entitlements.mjs` | Modified |
| `acres-research/entitlements.test.mjs` | Modified |
| `acres-research/envelope.mjs` | Modified |
| `acres-research/envelope.test.mjs` | Modified |
| `acres-research/feasibility-taxes.test.mjs` | Modified |
| `acres-research/feasibility.mjs` | Modified |
| `acres-research/feasibility.test.mjs` | Modified |
| `acres-research/harness.test.mjs` | Modified |
| `acres-research/keep.mjs` | Added |
| `acres-research/keep.test.mjs` | Added |
| `acres-research/land-value-paths.test.mjs` | Modified |
| `acres-research/lanes.mjs` | Modified |
| `acres-research/ledger.mjs` | Modified |
| `acres-research/ledger.test.mjs` | Modified |
| `acres-research/listing-filter-jev.mjs` | Modified |
| `acres-research/listing-filter-jev.test.mjs` | Modified |
| `acres-research/listing-intent.test.mjs` | Modified |
| `acres-research/listing-investigation-prompt.mjs` | Modified |
| `acres-research/listing-investigation-provider.mjs` | Modified |
| `acres-research/listing-investigations.mjs` | Modified |
| `acres-research/listing-investigations.test.mjs` | Modified |
| `acres-research/listing-research-context.test.mjs` | Modified |
| `acres-research/listing-search-filters.test.mjs` | Modified |
| `acres-research/manager.mjs` | Modified |
| `acres-research/market-data-checks.test.mjs` | Modified |
| `acres-research/market-listings.test.mjs` | Modified |
| `acres-research/market-refresh.mjs` | Modified |
| `acres-research/market-store.mjs` | Modified |
| `acres-research/market-store.test.mjs` | Modified |
| `acres-research/market.mjs` | Modified |
| `acres-research/market.test.mjs` | Modified |
| `acres-research/meta-visual.mjs` | Added |
| `acres-research/meta-visual.test.mjs` | Added |
| `acres-research/meta.mjs` | Added |
| `acres-research/meta.test.mjs` | Added |
| `acres-research/modeling-workflow.test.mjs` | Modified |
| `acres-research/nyc-history-coverage.test.mjs` | Modified |
| `acres-research/nyc-zoning-lookups.test.mjs` | Modified |
| `acres-research/nycdb.mjs` | Modified |
| `acres-research/plan-save-access.test.mjs` | Modified |
| `acres-research/proforma.mjs` | Modified |
| `acres-research/proforma.test.mjs` | Modified |
| `acres-research/project-state.mjs` | Modified |
| `acres-research/project-state.test.mjs` | Modified |
| `acres-research/research.mjs` | Modified |
| `acres-research/same-lot-site.test.mjs` | Modified |
| `acres-research/saved-searches.test.mjs` | Modified |
| `acres-research/scheme-outlines.mjs` | Modified |
| `acres-research/scheme-outlines.test.mjs` | Modified |
| `acres-research/scheme-plans.mjs` | Modified |
| `acres-research/schemes.mjs` | Modified |
| `acres-research/service.mjs` | Modified |
| `acres-research/service.test.mjs` | Modified |
| `acres-research/site-directory.test.mjs` | Modified |
| `acres-research/skills/creative-zoning/SKILL.md` | Modified |
| `acres-research/skills/keep-building/SKILL.md` | Added |
| `acres-research/skills/market-and-proforma/SKILL.md` | Modified |
| `acres-research/store.mjs` | Modified |
| `acres-research/store.test.mjs` | Modified |
| `acres-research/tax-485x.mjs` | Modified |
| `acres-research/usage-metrics.mjs` | Modified |
| `acres-research/wallet.test.mjs` | Modified |
| `acres-research/zoning-rules.json` | Modified |
| `acres-research/zoning.mjs` | Modified |
| `acres-research/zoning.test.mjs` | Modified |
| `app-starter/auth.js` | Modified |
| `app-starter/frontend/architecture-loader.mjs` | Modified |
| `app-starter/frontend/architecture-model.mjs` | Modified |
| `app-starter/frontend/architecture-view.jsx` | Modified |
| `app-starter/frontend/black-frame.mjs` | Added |
| `app-starter/frontend/concept-view.jsx` | Modified |
| `app-starter/frontend/context-recovery.mjs` | Added |
| `app-starter/frontend/daylight-environment.mjs` | Added |
| `app-starter/frontend/interior-layout.mjs` | Added |
| `app-starter/frontend/interior-scene.jsx` | Added |
| `app-starter/frontend/photo-renderer.jsx` | Added |
| `app-starter/frontend/photo-scene.mjs` | Added |
| `app-starter/frontend/visual-workbench.jsx` | Added |
| `app-starter/frontend/walk-clock.mjs` | Added |
| `app-starter/frontend/walkthrough.jsx` | Modified |
| `app-starter/frontend/wall-uv.mjs` | Added |
| `app-starter/model-intake-proxy.mjs` | Modified |
| `app-starter/package-lock.json` | Modified |
| `app-starter/package.json` | Modified |
| `app-starter/public/app.js` | Modified |
| `app-starter/public/architecture-assets/bed.glb` | Added |
| `app-starter/public/architecture-assets/credits.html` | Added |
| `app-starter/public/architecture-assets/door-color.jpg` | Added |
| `app-starter/public/architecture-assets/door-normal.jpg` | Added |
| `app-starter/public/architecture-assets/door-roughness.jpg` | Added |
| `app-starter/public/architecture-assets/nightstand.glb` | Added |
| `app-starter/public/architecture-assets/plaster-normal.jpg` | Added |
| `app-starter/public/architecture-assets/plaster-roughness.jpg` | Added |
| `app-starter/public/architecture-assets/sink.glb` | Added |
| `app-starter/public/architecture-assets/sofa.glb` | Added |
| `app-starter/public/architecture-assets/tile-color.jpg` | Added |
| `app-starter/public/architecture-assets/tile-normal.jpg` | Added |
| `app-starter/public/architecture-assets/tile-roughness.jpg` | Added |
| `app-starter/public/architecture-assets/toilet.glb` | Added |
| `app-starter/public/architecture-assets/vanity.glb` | Added |
| `app-starter/public/architecture-assets/wood-color.jpg` | Added |
| `app-starter/public/architecture-assets/wood-normal.jpg` | Added |
| `app-starter/public/architecture-assets/wood-roughness.jpg` | Added |
| `app-starter/public/conversation-view.js` | Modified |
| `app-starter/public/core-model.js` | Modified |
| `app-starter/public/core-view.js` | Modified |
| `app-starter/public/core.css` | Modified |
| `app-starter/public/core.js` | Modified |
| `app-starter/public/deals.js` | Modified |
| `app-starter/public/home.css` | Modified |
| `app-starter/public/index.html` | Modified |
| `app-starter/public/listing-filter-schema.js` | Modified |
| `app-starter/public/listing-inspector.js` | Modified |
| `app-starter/public/listing-investigation.js` | Modified |
| `app-starter/public/listings.css` | Modified |
| `app-starter/public/listings.js` | Modified |
| `app-starter/public/modeling.js` | Modified |
| `app-starter/public/nyc-address.mjs` | Added |
| `app-starter/public/onboarding.css` | Modified |
| `app-starter/public/report-view.js` | Modified |
| `app-starter/public/report.css` | Modified |
| `app-starter/public/schemes-view.js` | Modified |
| `app-starter/public/send-option.css` | Modified |
| `app-starter/public/styles.css` | Modified |
| `app-starter/public/surfaces.css` | Modified |
| `app-starter/public/theme.js` | Modified |
| `app-starter/public/wallet.css` | Modified |
| `app-starter/public/wallet.js` | Modified |
| `app-starter/public/workspace-shell.css` | Modified |
| `app-starter/tests/architecture-loader.test.mjs` | Added |
| `app-starter/tests/architecture-model.test.mjs` | Modified |
| `app-starter/tests/arosa-auth.test.mjs` | Modified |
| `app-starter/tests/ask-bar.test.mjs` | Modified |
| `app-starter/tests/axe-audit.test.mjs` | Added |
| `app-starter/tests/black-frame.test.mjs` | Added |
| `app-starter/tests/chat-shell-design.test.mjs` | Modified |
| `app-starter/tests/chat-submission-ack.test.mjs` | Modified |
| `app-starter/tests/context-recovery.test.mjs` | Added |
| `app-starter/tests/core-do-all-checklist.test.mjs` | Modified |
| `app-starter/tests/core-page.test.mjs` | Modified |
| `app-starter/tests/deal-listing-links.test.mjs` | Modified |
| `app-starter/tests/deal-value-basis.test.mjs` | Modified |
| `app-starter/tests/deals-paging.test.mjs` | Modified |
| `app-starter/tests/home.test.mjs` | Modified |
| `app-starter/tests/interior-layout.test.mjs` | Added |
| `app-starter/tests/interior-materials.test.mjs` | Added |
| `app-starter/tests/listing-filter-controls.test.mjs` | Modified |
| `app-starter/tests/listing-filter-replay.test.mjs` | Modified |
| `app-starter/tests/listing-investigation-dialog.test.mjs` | Modified |
| `app-starter/tests/listing-search-link.test.mjs` | Modified |
| `app-starter/tests/listings.test.mjs` | Modified |
| `app-starter/tests/model-intake-proxy.test.mjs` | Modified |
| `app-starter/tests/modeling-library.test.mjs` | Added |
| `app-starter/tests/nyc-address.test.mjs` | Added |
| `app-starter/tests/photo-scene.test.mjs` | Added |
| `app-starter/tests/plan-page-fixture/server.mjs` | Modified |
| `app-starter/tests/plan-text-attachment.test.mjs` | Modified |
| `app-starter/tests/product-answer.test.mjs` | Modified |
| `app-starter/tests/runtime-render.test.mjs` | Modified |
| `app-starter/tests/schemes-view.test.mjs` | Modified |
| `app-starter/tests/site-demo-assets.test.mjs` | Added |
| `app-starter/tests/theme-contrast.test.mjs` | Modified |
| `app-starter/tests/walk-clock.test.mjs` | Added |
| `app-starter/tests/wallet-ui.test.mjs` | Modified |
| `app-starter/tests/workspace-shell.test.mjs` | Modified |
| `docs/ROADMAP.md` | Modified |
| `docs/arosa-cloudflare-cutover.md` | Modified |
| `docs/arosa-deployment.md` | Modified |
| `docs/developer-onboarding.md` | Modified |
| `docs/hackathon-housing.md` | Added |
| `docs/project-state.md` | Modified |
| `infra/acres-deploy-research` | Modified |
| `infra/acres-pull-secrets` | Modified |
| `licenses/SAM-LICENSE.txt` | Added |
| `package-lock.json` | Modified |
| `package.json` | Modified |
| `site/.firebaserc` | Added |
| `site/README.md` | Modified |
| `site/build.mjs` | Modified |
| `site/firebase.json` | Added |
| `site/proxy/index.mjs` | Added |
| `site/proxy/package.json` | Added |
| `site/public/index.html` | Modified |
| `site/public/privacy.html` | Modified |
| `site/public/site.js` | Modified |

## Publication boundary

All product source areas are included: `app-starter`, `acres-research`, `planning`, `worker`, `acres-mcp`, `site`, `infra` and `scripts`. This clean initial history excludes private Git history, operator instructions, internal screenshots, old handoff notes, credentials and customer databases. The old production-derived report fixture is replaced with synthetic data. Generated dependencies and installed worker binaries are obtained separately with their original licenses.

## Attribution

Project-authored source: Hyatus Living and its contributors. Third-party software and asset credits are preserved in `LICENSES.md` and the linked notices. The Representative must verify all event participants in the submission form; publishing a source snapshot does not determine who is eligible to enter.
