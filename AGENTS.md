# Codex operating instructions — Contractor Website V6

These instructions apply to every Codex task in this repository.

## Mission and evidence

Build and maintain a truthful, distinctive, accessible, fast contractor website. Keep technical implementation away from the owner’s normal conversation. Ask only for ordinary business facts, meaningful creative direction, major outcome approval, or an unavoidable account/security action.

Use evidence in this order:

1. Explicit owner approval in the current task.
2. `handoff/APPROVED_BUILD_BRIEF.md` and `handoff/DESIGN_LOCK.json`.
3. Approved public facts in `handoff/PUBLIC_BUSINESS_FACTS.json`.
4. The current production website in `public/`.
5. The connected V6 Contractor Website Program source and private business-assets source, when available.

Never invent a business fact. Resolve a missing or conflicting claim before publishing it.

## Path and privacy boundaries

Ordinary website work may edit `public/` and the four `handoff/` files when the facts or decisions being recorded are approved. Do not edit `.github/`, `functions/`, `infrastructure/`, `scripts/`, `templates/`, `tests/`, `website.zip`, or `AGENTS.md` unless the task explicitly requests infrastructure maintenance.

Never commit private business records, raw interview notes, source media, license or insurance scans, permits, invoices, estimates, customer or employee data, credentials, secrets, recovery codes, or the private business-assets folder. Only approved public-ready derivatives belong in `public/`.

## Design sequence

1. Confirm enough business facts, proof, media, customers, services, service area, and emotional qualities to design responsibly.
2. Privately develop three genuinely different written directions, synthesize their strongest ideas, and build **only a homepage look-and-feel concept**.
3. Let the owner Approve, request a normal change in plain language, or say `Randomize`. A Randomize request must produce a substantially different concept while respecting any plain-language direction supplied with it.
4. Do not build the remaining pages until the homepage concept is approved.
5. After approval, build every approved page, preserved old URL, action, policy, responsive state, and function. The approved homepage concept—not the starter shell—becomes the design reference.

The committed `public/` directory is a disposable safety shell, never a visual template. For a first production build, replace its starter-only pages and assets. Original local fonts, SVG artwork, icons, textures, imagery, animation, and JavaScript are welcome when they support the business’s distinct character and remain accessible, performant, and policy-compliant.

## Public build contract

- Work on a branch and request review for ordinary desktop work; do not push directly to `main` unless the approved phone importer is performing its tested atomic update.
- Preserve every known working old public URL at the same path and purpose by default. Use an exact permanent redirect only when the destination truly replaces that purpose and the move plan is approved. Never sweep old pages to the homepage.
- Treat services, service areas, addresses, telephone numbers, hours, emergency availability, response times, prices, financing, warranties, licenses, insurance, bonding, certifications, years in business, reviews, awards, and project claims as evidence-sensitive.
- Prefer **Call** and **Request an Estimate** when confirmed. Never imply continuous monitoring.
- Never publish a private/home address for a service-area business. Publish an address only when customers may visit it and the owner approves public use.
- Avoid mass-produced or near-duplicate city pages. Every service and service-area page must help a real customer decide.
- Use semantic HTML, keyboard access, visible focus, readable contrast, useful alt text, reduced-motion behavior, responsive layouts, and one clear `h1` per page.
- Declare every public document and external media item in `site-manifest.json`. Keep video external, retain an optimized poster, and allow only the exact needed hosts.
- Do not add analytics, advertising pixels, chat widgets, embeds, or marketing forms without the matching approved business use and privacy treatment.
- Keep form recipients and secrets in the deployment environment. Turnstile widget action and `TURNSTILE_EXPECTED_ACTION` must match.

For every production change, keep `site-manifest.json` and `version.json` synchronized at schema, workflow, and repository package version `6.0`. Each page uses a canonical relative `file_path` plus root-relative `url_path` and `canonical_url_path`. Keep the complete favicon/app-icon family declared and linked.

GitHub `main` is the approved website record. Cloudflare Pages Git integration is the normal final host. ChatGPT Sites, a Work preview, or a local preview is temporary and must never be described as the live launch.

## Launch authorization

After the owner approves the finished website, ask once for a plain-language setup authorization covering: one new isolated private GitHub repository, one new Cloudflare Pages preview, the standard V6 settings, the non-`www` domain as primary, a path-preserving `www` redirect, HTTPS, automatic deploys, checks, monitoring, and a restore point.

Once granted, perform those routine actions quietly without asking separate technical questions. Pause only for an unavoidable sign-in, provider authorization, security verification, purchase, account ambiguity, unexpected conflict, destructive action, or a change in public scope. Hosted-preview approval remains separate. Final go-live approval remains separate.

Phone fallback: when connected-app or browser automation cannot create the repository, guide the owner through creating a private repository from the course template and uploading the single generated `website.zip`. ChatGPT still prepares and validates the ZIP. Cloudflare Pages Git integration remains the normal deployment path; dashboard drag-and-drop is not an equivalent fallback for this repository’s `functions/` directory.

## Required checks

From the repository root, run:

```bash
python3 scripts/release_check.py
python3 scripts/validate_site.py public --mode production --repo-root .
```

Also inspect common phone and desktop widths. Test navigation, click-to-call, request-an-estimate, contact fallback, services, service-area explanations, proof links, forms, keyboard use, reduced motion, preserved old routes, and the 404 page. Live delivery and reachability remain pending until the activation rehearsal passes.

## Completion and Business Asset Package

Do not call the program complete until the live HTTPS site is verified and the owner has received or explicitly declined the Business Asset Package. When applicable, create from approved branding and public facts: master logo exports, browser/device icons, Open Graph sharing image, concise brand guide PDF, two-sided print-ready business card with a tested direct HTTPS QR code, social avatar and cover exports, email-signature graphic, and a ZIP manifest. Keep these assets private unless the owner asks to publish them, and test the final exports themselves.

Before review or handoff, summarize visible changes in plain language, identify changed facts and their source, provide current phone and desktop evidence, report exact checks, identify unresolved live gates, and include a rollback note for risky changes.
