# Instant Website Pro Contractor Publishing System V6

This repository is a **nonvisual publishing and safety foundation** for the V6 contractor program. It protects imports, public/private boundaries, checks, deployment, monitoring, and rollback without deciding what a contractor’s website should look like.

The two supported routes share one public contract:

- **Desktop:** ChatGPT/Codex builds the approved website in `public/`, runs the checks, and publishes through an isolated private GitHub repository.
- **Phone fallback:** ChatGPT produces one complete approved `website.zip`; the owner uploads that one file when connected tools cannot complete the GitHub step. A workflow validates it before atomically replacing `public/`.
- **Hosting:** Cloudflare Pages Git integration deploys `public/` from GitHub `main`, plus optional Pages Functions under `functions/`.

A rejected phone package never changes the existing public site.

## Blank-canvas rule

The committed `public/` directory is a neutral waiting shell, not a design template. The real website begins with an owner-reviewed homepage concept derived from approved facts, media, trade, customers, service area, proof, and business personality. Only after the owner approves that concept does ChatGPT build the full site. The full build may replace every file in `public/` and use an original page structure, local fonts, SVG graphics, icons, imagery, animation, CSS, and JavaScript permitted by the safety policy.

## Privacy boundary

```text
private business-assets source      owner facts, originals, approvals; never commit
                |
                v
handoff/                            minimum approved public facts and decisions
                |
                v
public/                             deployable website files only

protected infrastructure
  .github/ functions/ infrastructure/ scripts/ tests/ templates/ AGENTS.md
```

## Repository map

```text
.github/workflows/                validation, phone import, rollback, health checks
public/                           public website files only
functions/api/                    optional Cloudflare Pages form endpoints
handoff/                          minimum approved public build context
infrastructure/                   protected V6 contracts and activation record
scripts/                          validator, packager, importer, live checker
tests/                            production and hostile-input regression tests
templates/                        optional implementation snippets
website.zip                       one-file phone transport; initial copy is a placeholder
```

## V6 package contract

`website.zip` must contain the whole production website with `index.html` at ZIP root, pass `infrastructure/importer-policy.json`, and use manifest/workflow/repository package version `6.0`. It must contain no wrapper folder, nested archive, bundled video, secret, private business source, raw capture, office workbook, or protected program file.

The manifest records every page, preserved old route, public document, icon, external media item, optional form, and the confirmed contractor profile. Old working URLs stay at the same path and purpose by default. Exact permanent redirects are exceptions; wildcard-to-home migration is rejected.

## Standard Cloudflare Pages setup

Use **Git integration**, no framework preset, the repository root, a blank build command, `public` as the build output directory, and `main` as the production branch. Authorize the Cloudflare GitHub app only for the intended repository when possible. A tested `exit 0` build command is acceptable only if a particular existing Pages project refuses an empty field and is rehearsed with this exact static contract.

Dashboard drag-and-drop is a limited static fallback: it does not compile this repository’s `functions/` folder and cannot later be converted into a Git-integrated project. Do not present it as equivalent to the normal route.

## Local checks

```bash
python3 scripts/release_check.py
python3 scripts/validate_site.py public --mode production --repo-root .
python3 scripts/package_site.py --source public --output website.zip --repo-root .
```

The packager creates a deterministic ZIP, imports it into a temporary directory, reruns production validation, and compares the extracted files before replacing the previous package.

## Launch and rollback

Normal owner experience uses one scoped setup authorization, a separate hosted-preview approval, and a separate final go-live approval. Routine repository, Pages preview, HTTPS, redirect, check, monitoring, and restore-point work proceeds under the setup authorization. Sign-ins, provider approvals, purchases, conflicts, destructive actions, or changed public scope still require the owner.

For immediate hosting recovery, use Cloudflare deployment history. For source recovery, run **Roll back website files** with a known-good full commit SHA. Never force-push or erase normal history.

Complete `infrastructure/ACTIVATION_REHEARSAL.md` before distributing a new template revision.
