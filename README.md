# GST Builder

Browser-first GSTR-1 preparation MVP. The current slice demonstrates CSV upload, automatic column mapping, canonical invoice normalization, basic GST reconciliation, row-level validation, a draft JSON export, and privacy/legal messaging.

## Run

```bash
npm install
npm run dev
```

## Product and API guardrails

The processing engine is intentionally separated from the UI in the product design so it can be extracted into a paid API. Before API launch, add authentication, tenant isolation, encrypted transport, configurable retention, deletion endpoints, audit logs, rate limits, usage metering, versioned schemas, a DPA, Terms of Service, Privacy Policy, subprocessor list, and a practitioner-reviewed GST rule release process. Never market the draft JSON as portal-upload-ready until it passes the current official GSTN utility for the supported return period.

## Production readiness

The app exports a workbook with Return Summary, Normalized Invoices, Validation Report, and Original Data sheets. The portal action opens the official GST portal for a user-controlled upload; it does not collect credentials, automate login, or bypass portal security. GSTN guidance says JSON can be uploaded from the GSTR-1/IFF return dashboard after login, and third-party JSON is acceptable only when it matches the portal's specified format. A production release requires official schema fixtures, GSTN offline-utility validation, practitioner sign-off, privacy and terms review, dependency audit, CSP and security headers, accessibility testing, file-fuzz testing, and API tenant controls before public filing claims.
