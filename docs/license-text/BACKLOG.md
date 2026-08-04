[//]: # ( ---------------------------------------------------------------------- )
[//]: # (+ Authors: 	Ran# <ran.hash@proton.me> )
[//]: # (+ Created: 	2026/08/04 18:26:57.404232 )
[//]: # (+ Revised: 	2026/08/04 18:26:57.404232 )
[//]: # ( ---------------------------------------------------------------------- )

# License translation backlog

Tracks which `docs/license-text/pbl-<version>.<lang>.txt` files exist and which are
still missing. Missing files are not an error — the page automatically falls back to
the English text for any language/version combination that isn't present, with no
"translated" notice shown in that case. This file exists so it's easy to see at a
glance what's still outstanding.

Language codes match the site's language picker: `gl, en, es, pt, fr, de, zh, ja`.

## PBL v2.0 (current — `pbl-v2.0.<lang>.txt`)

| Lang | File | Status |
|------|------|--------|
| en | `pbl-v2.0.en.txt` | done (canonical) |
| gl | `pbl-v2.0.gl.txt` | **missing** |
| es | `pbl-v2.0.es.txt` | **missing** |
| pt | `pbl-v2.0.pt.txt` | **missing** |
| fr | `pbl-v2.0.fr.txt` | **missing** |
| de | `pbl-v2.0.de.txt` | **missing** |
| zh | `pbl-v2.0.zh.txt` | **missing** |
| ja | `pbl-v2.0.ja.txt` | **missing** |

None of the v2.0 translations have been done yet. v2.0 is the long document (~2,000
lines, governance/voting/forking clauses) — full translation attempts for all seven
languages failed on 2026-08-04 (output-size limits on single-shot generation, and the
account's monthly spend limit was hit partway through retries). Redoing this properly
means translating each language in small chunks across multiple turns, not as one pass.

## PBL v1.0 (superseded — `pbl-v1.0.<lang>.txt`)

| Lang | File | Status |
|------|------|--------|
| en | `pbl-v1.0.en.txt` | done (canonical) |
| gl | `pbl-v1.0.gl.txt` | done |
| es | `pbl-v1.0.es.txt` | done |
| pt | `pbl-v1.0.pt.txt` | done |
| fr | `pbl-v1.0.fr.txt` | done |
| de | `pbl-v1.0.de.txt` | done |
| zh | `pbl-v1.0.zh.txt` | **missing** |
| ja | `pbl-v1.0.ja.txt` | done |

v1.0 is short (~80 lines) so six of the seven translations completed before hitting
any limit. Chinese (`zh`) never got a v1.0 pass — its agent run was spent entirely on
a partial, incomplete v2.0 attempt and died before reaching v1.0.

## Adding a translation

1. Translate `pbl-v2.0.en.txt` (or `pbl-v1.0.en.txt`) into the target language,
   preserving every structural convention documented in the parser comments in
   `docs/index.html` (`renderLicenses` / `parseLicenseText` area): section dividers,
   `N.`/`Na.` clause numbering, `"Term"`-alone-on-a-line definitions, `- ` bullets,
   `a) ` lettered items, and all literal file-format field names/paths/extensions
   left untranslated.
2. Save it as `docs/license-text/pbl-<version>.<lang>.txt`.
3. No code change needed — the page fetches whatever file exists for the current
   language and falls back to English automatically if it's absent.
