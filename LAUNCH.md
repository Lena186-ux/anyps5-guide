# Launch record

- Domain: `anyps5guide.com`; primary HTTPS apex. `www` redirects to apex through `vercel.json`.
- Repository: https://github.com/Lena186-ux/anyps5-guide (public, main).
- Vercel project: `anyps5-guide`, project ID `prj_SYc3giPi40GaTZRpA7kYUO6UzhmK`, team `team_5s6oVoWbOc9fBNOIw4er096N`.
- First Ready deployment: `dpl_kaEtDys6AJxckb3oCW69tY2Dp6Fg`.
- Production aliases: https://anyps5guide.com (canonical), https://anyps5-guide.vercel.app.
- Latest Ready application deployment (2026-10-11): `dpl_tYTjcdbWLWuhgp7HMGLtRdZFJp83`, source commit `837c32f`; includes Google and Bing ownership meta tags.
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

HTTPS origin verification with the hostname and Vercel address (normal certificate validation enabled) returns 200 for the apex and 308 for `https://www.anyps5guide.com/compatibility/`, with Location `https://anyps5guide.com/compatibility/`. Propagation subsequently completed: the custom domain is accessible in the in-app browser and through ordinary HTTPS requests. Both apex addresses return the same valid sitemap with normal certificate validation.

SEO methodology: gefei_seo `load_guide`, keyword topic, 2 credits charged, request `req_b024c1b078d45234`. No new search-volume or difficulty queries were made; no current demand or ranking estimates are claimed.

## Update workflow

Edit `build.mjs` and local CSS/assets. Run `node build.mjs`, commit and push only inside this repository, then run `vercel deploy --prod` from this directory. Preserve the project identity in `.vercel/project.json` and do not reuse another site's project ID. If this checkout is recreated, link explicitly to `anyps5-guide` before deployment.

## Content updates

Read the latest upstream source, pin its commit, and update the check date with any revised claims. Expand compatibility only from source-linked evidence. Do not infer playability from conversion success. Distinguish check dates from actual test dates.

## Search engine setup — 2026-10-11

- Google Search Console: `sc-domain:anyps5guide.com` verified through the root DNS TXT provided by Google; HTTPS URL-prefix property also verified through a global HTML meta tag. Keep the verification TXT and meta tags in place.
- Bing Webmaster Tools: only `https://anyps5guide.com/` added and verified through the global `msvalidate.01` meta tag. No other account sites imported.
- Canonical sitemap: https://anyps5guide.com/sitemap.xml, 10 URLs, public HTTP 200 and `application/xml`, valid sitemap namespace. `robots.txt` allows all crawlers and declares this URL. Both production IPs also return the same XML to requests using a Googlebot user agent; these requests do not prove Google's own crawler fetched it.
- Google accepted sitemap submission, including a retry after DNS verification. Its report still says “Couldn't fetch / Could not read sitemap”, discovered URLs 0. The exact cause is not supplied by GSC; a public transport/XML issue was not reproduced. This remains an open follow-up.
- Bing sitemap: **Success**, 10 URLs discovered, 0 errors, 0 warnings.
- Google homepage index inspection: not indexed / URL unknown to Google. Live test at 17:32 Asia/Shanghai says the URL can be indexed. Manual index request failed twice with Google's “problem submitting indexing request, try again later” message; no successful queue submission is claimed.
- Bing homepage index inspection: discovered on 2026-10-11, not yet crawled/indexed. Homepage indexing request accepted (“Indexing requested”). Live test at 17:35 says the URL can be indexed, with no SEO/GEO issues found.
- GSC aggregate indexing/performance reports are still processing, with its UI suggesting checking after approximately one day. Empty reports are not evidence that every site page is unindexed.
- Next check: GSC sitemap fetch result and homepage request, then both engines' indexing reports after processing. Verification and sitemap submission do not guarantee indexing. No recurring monitor configured.
- Methodology this setup: gefei_seo `load_guide`, topic `gsc`, **2 credits**, request `req_955d6dc18d41161c`; no paid keyword/domain queries repeated.
- Production builds succeeded for verification-tag changes; no test suite added or run.

## Google sitemap follow-up — 2026-10-11

This section supersedes the initial Google homepage status above.

- A fresh homepage inspection in the domain property now explicitly says **URL is on Google / Page is indexed**. Googlebot Smartphone last crawled it successfully at **2026-10-11 17:32:47 Asia/Shanghai**. User-declared and Google-selected canonical are both `https://anyps5guide.com/`. The previously opened URL-prefix inspection retained an older unknown-URL result; use a fresh inspection rather than interpreting the older result as current.
- Live inspection of `https://anyps5guide.com/sitemap.xml` at **17:39:57 Asia/Shanghai** reports crawl allowed, successful fetch. The inspected response details confirm **200 OK**, **application/xml**, and source shows the actual 10-URL sitemap, not HTML or a login/challenge page.
- Parsed the fresh public XML: standard urlset namespace, 10 unique URLs, all on the canonical HTTPS origin. Cloudflare's public resolver returned the two configured Vercel A addresses and no AAAA answer. A query to Google's 8.8.8.8 resolver timed out from this machine and cannot establish Google's DNS view.
- Manual actions and Security issues reports both say no issues detected.
- The canonical sitemap was resubmitted after Google's successful live fetch; GSC confirmed acceptance. The sitemap report still retains Couldn't fetch. This report-level failure has not been confirmed resolved, and no specific current transport or syntax defect was found to justify changing production code, security protections or DNS.
- Retried homepage indexing in the URL-prefix property, then through a fresh domain-property inspection. Both requests returned Google's generic submission error; no successful new queue submission is claimed. The homepage is nevertheless already indexed independently of these retries.
- The remaining Google sitemap report and manual-request errors require later service processing/retry; do not assert a specific root cause without evidence. Google's official troubleshooting guidance supports using live inspection's crawl/fetch results: https://support.google.com/webmasters/answer/7451001?hl=en.
- Reused the previous gefei_seo GSC guide (request `req_955d6dc18d41161c`); **0 additional credits** in this follow-up. No production code changes or additional deployment were needed. No tests added or run.
