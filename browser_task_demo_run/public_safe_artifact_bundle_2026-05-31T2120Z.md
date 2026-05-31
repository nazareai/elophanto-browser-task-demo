# Public-safe artifact bundle — browser task demo

Created: 2026-05-31T21:20Z  
Scope: checkpoint 9 public-safe bundle/page-section source  
Live example: read-only OWASP Prompt Injection source capture

## What this bundle proves

This bundle gives operators enough evidence to inspect the browser-task demo without exposing private data. It references only sanitized artifacts from the live run: the normalized example dossier, public source URLs, visible verification receipt, safe transcript/screenshot references, and manifest/checksum information.

## Normalized example dossier

- `example_dossier_2026-05-31T2024Z.md`
- Purpose: stranger-legible explanation of the selected live browser task, why it was safe, which public sources were visited, how untrusted prompt-injection examples were handled, and what non-action boundaries were enforced.

## Public source URLs

1. `https://simonwillison.net/2024/Jun/6/what-we-need-to-know-about-prompt-injection/`
   - Public URL attempted first.
   - Result: 404 page.
   - Safe-use note: recorded as a failed public-source attempt; no form submitted and no state changed.

2. `https://owasp.org/www-community/attacks/PromptInjection`
   - Public URL used as the primary source.
   - Result: OWASP Prompt Injection page loaded and captured.
   - Safe-use note: page text was treated as untrusted data only. No instruction-like content from the page was followed.

Receipt file: `visited_urls_2026-05-31T2018Z.txt`

## Visible verification receipt

- `artifact_set_visible_verification_2026-05-31T2022Z.png`
- What it shows: PASS state, artifact directory label, counts for transcript/screenshots/URL log/execution record/manifest, and manifest SHA reference.
- Public-safety note: this image exposes no credentials, cookies, vault values, logged-in account state, or private source content.

## Safe transcript and screenshot references

| Artifact | Public-safe reference | Why it is safe |
|---|---|---|
| Task transcript | `task_transcript_2026-05-31T2018Z.md` | Describes browser actions and boundary decisions; no secrets or private account content. |
| Source page top screenshot | `screenshots/01_owasp_prompt_injection_top.jpg` | Public OWASP page view only. |
| Source capture screenshot | `screenshots/02_source_capture_overview.jpg` | Public OWASP page content only. |
| Untrusted-content examples screenshot | `screenshots/03_untrusted_content_examples.jpg` | Public examples from OWASP shown as data, not instructions. |
| Visible page text | `visible_page_text_2026-05-31T2018Z.txt` | Extracted visible public page text only. |
| Execution record | `execution_record_2026-05-31T2018Z.json` | Lists allowed/prohibited actions and confirms no external mutation. |

## Manifest and checksum information

Manifest file: `artifact_manifest_2026-05-31T2022Z.json`

Selected SHA-256 hashes from the manifest:

| Relative path | SHA-256 |
|---|---|
| `artifact_set_visible_verification_2026-05-31T2022Z.png` | `35f5846c8075c9b6521c13fbdb2587225841859968ce62b14192b9b78b4ab4bd` |
| `task_transcript_2026-05-31T2018Z.md` | `672df8763bbd9d3018728c3240d94c9af5fdbda1b4b45c5133754d0d01e7f22b` |
| `visible_page_text_2026-05-31T2018Z.txt` | `54703c82ce507647ca7186c2a8c572ab2ffc899dbdfc20031f818611cd21a55e` |
| `visited_urls_2026-05-31T2018Z.txt` | `38e343df49d57a69ad72446dbe8e7628d309b3fcc313d91d55cab8f345a64852` |
| `execution_record_2026-05-31T2018Z.json` | `77d31885b5abec58772d2876a9464963a8692add4c21870106ad3c74daa00afe` |
| `screenshots/01_owasp_prompt_injection_top.jpg` | `2e7f6198c6744172d615e67cc1aa527b24df13e103b357366cd6bcde4649ef1e` |
| `screenshots/02_source_capture_overview.jpg` | `a67ba2092fe2764ae02833e4d1b2610fb4cdb9f79d70ab65f8db71ddb3d987c7` |
| `screenshots/03_untrusted_content_examples.jpg` | `03b61ad09acb655a097466034cba9c72e042cf066c9ba1c49ea3914534508803` |

## Omitted private/local details

The public page and this bundle intentionally omit:

- raw cookies, localStorage, sessionStorage, auth headers, browser profile data, and vault values;
- private tabs, logged-in account pages, personal data, inbox contents, account identifiers, or payment details;
- absolute local filesystem paths in reader-facing page copy, except where a local-only operator receipt already exists and is not intended as public web content;
- raw browser internals, network headers, and any machine-specific details not required to verify the public read-only run.

Reason for omission: the proof standard is to expose enough receipts to validate behavior while preventing credential leakage, user deanonymization, or accidental publication of private local context.

## Public page insertion note

The demo page should reference this bundle from its receipts/privacy area as the canonical public-safe artifact map. If the page is deployed, link targets should remain relative and should not reveal absolute local paths.