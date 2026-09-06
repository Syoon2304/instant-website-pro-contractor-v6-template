# V6 creator activation rehearsal

Complete this rehearsal with disposable accounts, repository, Pages project, and test domain before calling a V6 template live. Local checks cannot prove permissions, provider authorization, deployment, DNS, HTTPS, delivery, or rollback.

## 1. Exact template

- Publish the exact `contractor-website-v6-starter` tree at the URL in `RELEASE CONFIG.json` and mark it as a GitHub template.
- Record the exact commit in `RELEASE CONFIG.json`; `PENDING_ACTIVATION` is not a passing value.
- Create a new private repository from the public template and keep `main` as the default branch.
- Confirm the template’s Actions workflow has the permissions documented by the creator guide.
- Run **Validate website source** and confirm the exact reviewed starter passes.
- Make a harmless change to `public/` without updating `starter-tree.sha256`; confirm starter-mode validation rejects it, then revert normally.

## 2. Homepage-first build

- Using a fictitious contractor, confirm the assistant builds only a homepage concept first.
- Request `Randomize` and confirm the replacement is substantially different.
- Approve the concept, then confirm the full site—not just the homepage—is built and validated.

## 3. Phone one-ZIP fallback

- Replace `public/` with the known-good production fixture and create `website.zip` with `scripts/package_site.py`.
- Restore the waiting shell, upload only that ZIP through the same phone-browser steps taught to students, and commit it.
- Confirm the workflow validates and atomically replaces `public/`.
- Upload wrapper-folder, traversal, symlink, duplicate-path, oversize, and invalid-contract fixtures. Each must fail while the last good site remains unchanged.

## 4. Desktop route

- Open a new private repository in Codex.
- Confirm the agent follows `AGENTS.md`, keeps private material out, uses the approved homepage concept, works on a branch, and runs production checks.
- Confirm review shows real website files rather than only a binary ZIP.

## 5. Cloudflare Pages Git integration

- In Workers & Pages, create a Pages project through **Git integration** and authorize the Cloudflare GitHub app for the disposable repository.
- Select no framework. Use repository root, leave the build command blank, set output directory `public`, and production branch `main`.
- If the dashboard refuses a blank command, rehearse `exit 0` with this exact static repository and record that exception.
- Confirm static pages and `functions/api/health.js` deploy at the `pages.dev` preview.
- Confirm a push to `main` creates an automatic deployment.

Do not use dashboard drag-and-drop to claim a Functions rehearsal: Cloudflare documents that it does not compile a `functions/` folder. A Direct Upload project also cannot later be switched to Git integration.

## 6. Domain and website behavior

- Add the apex domain through the Pages project’s **Custom domains** screen.
- Configure the path-preserving `www` to apex redirect and verify nested paths and query strings.
- Verify HTTPS, headers, CSP, 404 behavior, canonical URLs, robots file, sitemap, and every declared old route on cellular data.
- Test click-to-call and request-an-estimate on a phone. Confirm a private/home address is absent for a service-area test business.
- Confirm credentials, reviews, warranties, response times, financing, and emergency claims are absent unless approved evidence exists.

## 7. Optional forms and media

- If enabled, configure encrypted deployment secrets and public variables from `form-environment.template.txt`.
- Verify a real form delivery, direct contact fallback, allowed origin, Turnstile action/hostname, missing consent rejection, upload rejection, oversize rejection, and safe `/api/health` output.
- Verify every external media URL, poster, CSP host, accessibility treatment, and live-check allowlist entry.

## 8. Monitoring and rollback

- Set `SITE_URL` to the disposable HTTPS domain and run the live health workflow manually.
- Verify Cloudflare deployment rollback.
- Verify the GitHub rollback workflow with a known-good full commit; it must create a new validated commit without rewriting history.

## 9. Completion behavior

- Confirm one setup authorization is enough for routine technical work, while hosted-preview and go-live approvals remain separate.
- Confirm completion produces or explicitly records the owner’s decline of the Business Asset Package, including final-export and QR testing when applicable.

Record the repository, template commit, Actions run, Pages project, settings, domain, test results, failures, rollback evidence, and intentionally disabled options. Never record secrets.
