# India Smart Tools

A static, browser-first utility website with seven tools: CTC take-home estimate, income-tax estimate, job-offer comparison, EMI, CGPA, attendance and PDF object-stream optimization.

## Run locally

Open `index.html` in a modern browser, or run a local static server:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy to Cloudflare Pages

1. Create a GitHub repository and upload the contents of this folder.
2. In Cloudflare Pages, create a project and connect that repository.
3. Framework preset: **None**. Build command: leave blank. Build output directory: `.` (repository root).
4. Deploy.
5. Replace `YOUR-DOMAIN.example` in `robots.txt` and `sitemap.xml` after choosing your real domain.

## Important implementation notes

- This is a static HTML project, not an Astro application. It can be deployed as-is to a static host.
- Tailwind CSS, PDF-Lib and Google Fonts are loaded from third-party CDNs; an internet connection is needed for those assets.
- The PDF tool re-saves PDF object streams in the browser. It does **not** recompress embedded images, so it must not be marketed as guaranteed PDF size reduction.
- Tax output is an estimate for resident individuals below 60 using normal slab income. It does not calculate special-rate income, surcharge, senior-citizen slabs or every deduction condition. Confirm with the Income Tax Department or a qualified tax professional before filing.
- CTC output excludes income-tax TDS and assumes the component percentages supplied by the visitor. Professional tax varies by state and employer payroll treatment.
- CGPA percentage conversion depends on the university. Select the conversion rule required by your institution.
- No analytics or advertising scripts have been added. Add them only after publishing a privacy policy and completing the relevant consent and policy work.

## Before public launch

- Replace the placeholder domain in `robots.txt` and `sitemap.xml`.
- Publish a real contact method and add it to the site and policy pages.
- Review the privacy policy for your actual hosting, analytics and advertising setup. The current release has no analytics or ad scripts.
- Run a full cross-device, accessibility, performance and policy review before applying for advertising approval.

## Verification

The delivered HTML was checked for JavaScript syntax and key calculator scenarios. This is not a substitute for testing on real devices, browsers, tax edge cases, accessibility review or a formal security audit.
