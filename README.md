# VIZCAM | Smart Security & Automation Solutions

Premium static business website for VIZCAM in Manjeri, Kerala. Designed for hosting on GitHub Pages at **https://www.vizcam.me/**.

## Deploy to GitHub Pages

1. Create a **public** GitHub repository (suggested name: `vizcam-website`). You do **not** need a paid web hosting plan for this site.
2. Download and **extract** the provided website ZIP. On GitHub, open your new repository > **Add file** > **Upload files**, then drag **the contents** of the extracted folder (not the ZIP itself) into GitHub. The root of the repo must contain `index.html`, `CNAME`, `.nojekyll`, `assets/`, `css/`, and `js/`. Commit files to `main`.
3. Repository > **Settings** > **Pages** > **Build and deployment** > **Source: Deploy from a branch** > branch `main` > folder `/(root)` > **Save**.
4. Under **Custom domain** enter `www.vizcam.me` > **Save**. Keep the `CNAME` file with exactly that domain. Confirm the custom domain remains configured after commits.
5. In GoDaddy DNS (only if GoDaddy manages your nameservers), configure the following: 

   | Record type | Name | Value |
   |---|---|---|
   | A | @ | 185.199.108.153 |
   | A | @ | 185.199.109.153 |
   | A | @ | 185.199.110.153 |
   | A | @ | 185.199.111.153 |
   | CNAME | www | YOUR_GITHUB_USERNAME.github.io |

   Replace `YOUR_GITHUB_USERNAME` with the account that owns the GitHub repository (not the repo name). For example, account `exampleuser` would use `exampleuser.github.io`. There is **no** `/vizcam-website` path in the DNS value. The four `A` records are GitHub Pages' official IPv4 values, *not* GoDaddy hosting IPs.

6. Remove/rewrite old **website-only** conflicting `@` A and `www` CNAME/A records if present. Do NOT change MX, mail-related TXT/SPF/DKIM/DMARC, other email configuration, or domain nameservers casually. `service@vizcam.me` and `hr@vizcam.me` need separate email hosting setup; GitHub Pages does not provide email.
7. When the GitHub Pages DNS check succeeds and an HTTPS certificate is issued, select **Enforce HTTPS** in Settings > Pages. Check https://www.vizcam.me and https://vizcam.me (the second should redirect to the primary domain).
8. Test gallery filters, mobile navigation, email links, WhatsApp enquiry, images, and the sitemap. You can submit `https://www.vizcam.me/sitemap.xml` to Google Search Console.

**Important:** A `CNAME` file by itself is NOT enough; the domain must also be entered into the Pages settings and the GoDaddy DNS records must be correct. If GoDaddy is not the active DNS provider, make the DNS changes at the current DNS host instead.

GitHub official docs:
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

## Contact configuration
- Customer services: `service@vizcam.me`
- Careers: `hr@vizcam.me`
- Phone / WhatsApp: `+91 89438 54151`
- Location: Manjeri, Malappuram, Kerala, India

## Notes
- The quotation form creates a prefilled WhatsApp message and requires the visitor to press **Send** in WhatsApp. No server-side processing or email delivery occurs.
- The gallery currently contains **illustrative security system graphics**, not photographs of completed VIZCAM installations. Replace them when approved project photos are available.
- Core content includes optional English/Malayalam switching; individual technical text remains English.
- Font files load from Google Fonts when available, with local sans-serif fallbacks.
- Edit `index.html`, `css/styles.css`, `js/script.js` and `assets/` in the repo to update the site. Every commit to `main` will trigger a new Pages deployment once configured.
- For domain protection, consider verifying `vizcam.me` in your GitHub personal account Pages settings with GitHub-provided TXT verification before publishing.
- Do not commit private credentials, password files, or sensitive client project photos/data to a public repository.
