# PE Toolbox website

A small static website with an app overview, support page and privacy policy. No installation or build step is needed. All links are relative, so the site works at a GitHub Pages repository URL or a custom domain.

## Before publishing

- The public support and privacy contact is `ryansapps@outlook.com`. Keep this inbox monitored for user requests.
- Review the privacy policy against your release build and actual support-email practices. It reflects the current source: device-local storage, manual exports/backups, no account and no integrated advertising or analytics SDKs.
- The provided screenshots still show the earlier name “PE Planner”. The website identifies this in a caption. Replace the images with updated captures when ready.
- An App Store download button is intentionally absent because no live listing URL was provided. Add the real listing link when it is available; use Apple's official badge if adding a badge.

## Publish on GitHub Pages

1. Create a repository for the website, for example `pe-toolbox`.
2. Upload the **contents of this folder** into that repository's root, keeping `assets` as a folder. `index.html` must be at the repository root, not inside another `website` folder. Include `.nojekyll` if uploading with Git; the plain HTML site also works with GitHub's default processing if a browser upload omits that hidden file.
3. In the repository, open **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, select **main** and **/(root)**, then save.
4. Wait for GitHub to show the published address, enable **Enforce HTTPS** if available, and open all three pages to verify the published site and contact link.

Only the website files are needed in the website repository. Uploading the iOS app project is unnecessary.

If you prefer to use the existing app repository, place these website files in its `docs` folder and select **main /docs** in Pages settings instead.

## App Store Connect URLs

Use the exact HTTPS base address GitHub gives you. For a repository named `pe-toolbox`, it usually looks like `https://YOUR-USERNAME.github.io/pe-toolbox/`.

| App Store Connect field | Website URL |
| --- | --- |
| Marketing URL (optional) | Your published base URL |
| Support URL | Your published base URL + `support.html` |
| Privacy Policy URL | Your published base URL + `privacy.html` |

Apple also requires an easily accessible privacy-policy link **inside the app**. The current `SettingsView.swift` does not include one; add the final published URL there before submission. This website task does not modify the iOS app.

The website addresses the public web pages used in submission, not every App Store requirement or an assurance of approval. If the release adds accounts, real purchases, analytics or cloud services, update the policy, support answers and App Store privacy disclosures to match. The current purchase service is a mock, so the website makes no purchase or subscription claims.

## Files and editing

- `index.html`: app overview and screenshots.
- `support.html`: support contact and FAQ, including guidance from the app’s onboarding.
- `privacy.html`: privacy policy.
- `styles.css`: shared responsive design.
- `assets/`: supplied app icon and four original App Store graphics.
- `.nojekyll`: tells GitHub Pages to serve static files directly.

Open `index.html` directly to preview, or run `python3 -m http.server 4173` from this folder and open `http://localhost:4173`.

## References

Checked on September 6, 2026:

- [Apple: platform version information, including Support and Marketing URLs](https://developer.apple.com/help/app-store-connect/reference/app-information/platform-version-information/)
- [Apple: App Privacy Details](https://developer.apple.com/app-store/app-privacy-details/)
- [Apple: App Review Guidelines, section 5.1.1](https://developer.apple.com/app-store/review/guidelines/#data-collection-and-storage)
- [GitHub: configuring a Pages publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [GitHub: Pages visitor IP logging](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages)
