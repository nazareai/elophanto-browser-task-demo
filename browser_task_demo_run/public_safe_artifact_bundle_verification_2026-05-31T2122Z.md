# Checkpoint 9 verification — public-safe artifact bundle

Verified: 2026-05-31T21:22Z

## Created bundle

- `public_safe_artifact_bundle_2026-05-31T2120Z.md`
- SHA-256: `a8695674e09cdf324fc8af0301fe744c1699fd8f716aa03f2ae5a13bc9b265d4`
- Size: 4,888 bytes

## Page section updated

- Updated `../browser_task_demo_page_draft.html` receipts area.
- Added link to the public-safe bundle using a relative URL: `browser_task_demo_run/public_safe_artifact_bundle_2026-05-31T2120Z.md`.
- Added checksum highlights for the visible verification image, task transcript, and visited URL log.
- Added stricter privacy wording to exclude raw browser internals, network headers, and machine-specific details not required for verification.

## Required checkpoint contents

| Required item | Result |
|---|---|
| Normalized example dossier | PASS — `example_dossier_2026-05-31T2024Z.md` referenced. |
| Public source URLs | PASS — Simon Willison 404 attempt and OWASP Prompt Injection URL referenced. |
| Visible verification receipt | PASS — `artifact_set_visible_verification_2026-05-31T2022Z.png` referenced with SHA-256. |
| Transcript/screenshot references where safe | PASS — transcript, three screenshots, visible text, and execution record referenced with safety rationale. |
| Manifest/checksum information | PASS — manifest referenced and selected SHA-256 hashes included. |
| Omitted private/local details note | PASS — omitted cookies, storage, auth headers, vault values, browser profile data, private tabs, logged-in pages, personal data, account identifiers, payment details, raw browser internals, network headers, and unnecessary machine-specific details. |
| Public-safe link behavior | PASS — page uses relative artifact links and contains no `redacted local path` absolute paths in HTML. |

## Browser render verification

Initial local HTTP and `file:` attempts failed in the browser bridge with local preview host (redacted)/local loopback preview host (redacted) access errors and tunnel rewriting, even though curl returned `200 OK`. I then rendered the sanitized public-safe bundle directly in the browser document and captured a successful visual receipt.

- Browser title: `Public-safe artifact bundle preview`
- Rendered heading: `Public-safe artifact bundle`
- Rendered sections: What this bundle proves; Normalized example dossier; Public source URLs; Safe receipt references; Manifest and checksum highlights; Omitted private/local details.
- Browser screenshot receipt A, top/source section: `redacted local browser-bridge screenshot path; public-safe visible receipt is embedded/linked in this bundle`
- Browser screenshot receipt B, receipt/checksum section: `redacted local browser-bridge screenshot path; public-safe visible receipt is embedded/linked in this bundle`
- Browser screenshot receipt C, omitted-private-details section: `redacted local browser-bridge screenshot path; public-safe visible receipt is embedded/linked in this bundle`
- Browser text extraction: PASS — includes dossier, public URLs, visible verification receipt, transcript/screenshot references, manifest/checksum highlights, and omitted-private-details note.

Visible coverage by screenshot:

| Required visible item | Screenshot receipt |
|---|---|
| Header, proof statement, normalized dossier, public source URLs | A |
| Visible verification receipt, transcript reference, screenshot references, manifest/checksum highlights | B |
| Omitted private/local details note | C |

This resolves both prior verification gaps: the checkpoint output is browser-rendered, captured, and the required lower-page receipt/checksum/omission sections are visibly confirmed.