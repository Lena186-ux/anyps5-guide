# Launch record

- Domain: `anyps5guide.com`; primary HTTPS apex. `www` redirects to apex through `vercel.json`.
- Repository: https://github.com/Lena186-ux/anyps5-guide (public, main).
- Vercel project: `anyps5-guide`, project ID `prj_SYc3giPi40GaTZRpA7kYUO6UzhmK`, team `team_5s6oVoWbOc9fBNOIw4er096N`.
- First Ready deployment: `dpl_kaEtDys6AJxckb3oCW69tY2Dp6Fg`.
- Production alias: https://anyps5-guide.vercel.app.
- Build: `node build.mjs`; 10 static content routes plus 404, sitemap, robots and local assets.
- No test suite added or run. No analytics or ad account configured.
- Source is pushed to GitHub. Vercel Git connection failed; production was published with the authenticated CLI. Automatic deployment from GitHub is not configured.

## DNS

NameSilo records persisted and were re-read after a page reload:

| Name | Type | Value | TTL |
| --- | --- | --- | --- |
| @ | A | 216.198.79.1 | 3600 |
| @ | A | 64.29.17.1 | 3600 |
| www | CNAME | 55da96f9a33176d8.vercel-dns-017.com | 3600 |

Values were returned by Vercel's domain verification tool. The `_domainconnect` TXT record was retained. Original parking records are preserved in `dns-before.json`; no mail records were present.

Final domain configuration on 2026-10-11: Vercel displays Valid Configuration for both domains. The www hostname has a domain-level 308 redirect to the apex, preserving paths. TCP queries to NameSilo authoritative DNS and 1.1.1.1 return the new apex addresses; www returns the specified CNAME.

HTTPS origin verification with the hostname and Vercel address (normal certificate validation enabled) returns 200 for the apex and 308 for `https://www.anyps5guide.com/compatibility/`, with Location `https://anyps5guide.com/compatibility/`. Local default DNS and the in-app browser still use old parking addresses, so normal browser access to the custom domain has not been confirmed from this machine. The production Vercel alias is accessible in the in-app browser. Do not bypass certificate warnings or change correct DNS merely to work around local caching.

SEO methodology: gefei_seo `load_guide`, keyword topic, 2 credits charged, request `req_b024c1b078d45234`. No new search-volume or difficulty queries were made; no current demand or ranking estimates are claimed.

## Update workflow

Edit `build.mjs` and local CSS/assets. Run `node build.mjs`, commit and push only inside this repository, then run `vercel deploy --prod` from this directory. Preserve the project identity in `.vercel/project.json` and do not reuse another site's project ID. If this checkout is recreated, link explicitly to `anyps5-guide` before deployment.

## Content updates

Read the latest upstream source, pin its commit, and update the check date with any revised claims. Expand compatibility only from source-linked evidence. Do not infer playability from conversion success. Distinguish check dates from actual test dates.
