# MoneyReceipt

**Understand the real cost before you pay or sign.**

MoneyReceipt turns financial documents — bills, leases, loan agreements, paystubs, insurance quotes, job offers and other contracts — into a plain-language "receipt": the real cost, important deadlines, risks and hidden fees, and the questions to ask before you commit.

This is an interactive prototype in a single HTML file. There is no backend, no login and no API key. Everything runs in your browser.

## Try it

Open `index.html` in any modern browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then visit <http://localhost:8000>. Start with **Try the demo lease** on the home page.

## Features

- **Upload flow:** drag and drop PDF, JPG, PNG or DOCX (up to 25 MB), with a document-type selector and error states for unsupported, empty or oversized files.
- **Financial summary:** total and recurring cost, payment schedule, interest rate and APR, taxes, hidden fees, renewal and cancellation terms, late fees, deposits, salary and deductions, bonuses and benefits.
- **Evidence for every finding:** each result links to the page and section it came from and shows the quoted passage. Missing terms say "Not found in this document."
- **Two-part trust model:** *source quality* (was the exact passage found?) is separate from *reliability* (does the passage support the conclusion?). Conflicting clauses, estimates and counted dates are rated lower, with a written reason.
- **Decision brief:** a readiness status ("Confirm conflicting terms first", "Questions remain", "Ready to review") with Understand / Verify / Act checklists.
- **What-if scenarios and showdown:** per-document calculators (leave a lease early, pay extra on a loan, change a 401(k) contribution and more). Save up to three scenarios and compare them with the document as written.
- **Contract change detector:** compare two versions of a contract and see every changed amount, fee, date, term and risk, with the before and after wording side by side.
- **Accuracy Lab:** 20 automated checks that run the app's own calculation, evidence, reliability and date logic against tricky cases.
- **Deadlines:** a timeline with relative dates, copy buttons and Google Calendar links, plus a cross-document "coming up" hub.
- **Questions to ask:** grouped by who should answer, with Not asked / Asked / Answered tracking.
- **History, compare and notes:** saved analyses (search, filter, sort, delete), side-by-side comparison of any two documents, and personal notes per document.
- **Exports:** a printable HTML summary, plain text, or copy to clipboard.
- **Glossary** of 27 money terms in plain English, a dark/light theme, a responsive layout, and keyboard and screen-reader support.

## Prototype limits

- Uploaded files are **not read**. They are checked for type and size only and produce clearly labeled *example* results for the chosen document type. Full results come from the seven built-in demo documents.
- Saved analyses live in your browser's `localStorage`. Anyone using the same browser can see them, and clearing site data removes them.
- Scenario results are estimates, and each one states its assumptions.

## Tech

- React 18 (UMD) with in-browser Babel, loaded from public CDNs
- Hand-written CSS with light and dark themes, plus inline SVG icons and charts
- No build step and no dependencies to install

## Disclaimer

MoneyReceipt provides informational summaries only and is not legal, tax, investment, or financial advice.
