# JSC Website — editable static site

This is a lightweight static website for Jaap Suyk Consultancy. It can be hosted on Netlify and edited in GitHub. No build command or framework is required.

## Quick edit guide

- **Brand colours, site name, domain, description, email and LinkedIn:** edit `js/site-config.js`. The theme values are centralised there.
- **Visible wording and section order:** edit `index.html`. Search for the heading or paragraph you want to change.
- **Layout, fonts, spacing and responsive styles:** edit `css/styles.css`. Default CSS colour variables are at the very top; `site-config.js` overrides them on page load.
- **Interactive behaviour and structured data:** edit `js/main.js`.
- **Search crawl settings:** `robots.txt` and `sitemap.xml`.

## Before launch — important

1. In `js/site-config.js`, set `siteUrl` to the exact live HTTPS domain, e.g. `https://www.example.com` (no trailing slash needed).
2. Add a verified public contact email and the correct LinkedIn profile URL to `email` and `linkedinUrl`. Do not publish guessed contact details.
3. Replace `YOUR-DOMAIN-HERE` in `sitemap.xml` with the real domain. Update the Sitemap line in `robots.txt` to the real sitemap URL.
4. Upload the project to a GitHub repository, then connect that repository to Netlify. Set the publish directory to `.` and leave the build command blank.
5. In Netlify, enable form detection and redeploy so the `jsc-enquiry` Netlify Form is detected. Set up a form notification to the verified JSC inbox. Submit a real test enquiry after deployment.
6. Connect the domain in Netlify Domain management and follow the DNS records Netlify provides at your domain registrar. Wait for HTTPS to activate.
7. Add the live sitemap URL to Google Search Console and Bing Webmaster Tools. Verify both services and request indexing after the domain is live.
8. Review the wording of every service claim and all clinical/regulatory statements before launch. This site does not imply that JSC itself is a regulator or guarantees product approval.

## SEO and AEO included

- Descriptive page title and meta description; semantic heading hierarchy and crawlable HTML copy.
- Open Graph and social-sharing metadata.
- `ProfessionalService` JSON-LD with company location, APAC footprint and areas of expertise.
- Visible, concise FAQ section with matching `FAQPage` JSON-LD generated from the page content. Search engines decide independently whether to display rich results.
- Mobile responsive design, keyboard-operable market selector, accessible form labels and `robots.txt` / XML sitemap templates.

SEO/AEO is not a guarantee of rankings or AI citations. The next improvements with the highest long-term value are accurate service-specific landing pages, original case studies or examples (with permission), clear author/company credentials, and genuinely useful market-entry articles. Do not publish unsupported claims or create thin country pages just to target keywords.

## Current scope / limitations

This is a static marketing website, not a CMS. To change text, edit `index.html` in GitHub; to change colours, edit `js/site-config.js`. The contact form is configured for Netlify Forms, but it will only receive submissions after Netlify detects the form and notifications are configured.
