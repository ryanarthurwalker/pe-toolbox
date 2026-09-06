# PE Toolbox

PE Toolbox is a lesson-planning app for PE teachers on iPhone and iPad. It brings lessons, activities, class schedules, and diagrams together to help teachers prepare for the gym, field, or playground.

This repository contains the PE Toolbox website, including the app overview, FAQ, and privacy policy.

## App features

- **Plan lessons:** Organize activities into warm-up, skill development, game, and cool-down sections.
- **Build an activity library:** Browse included games, create custom activities, and organize favorites into collections.
- **Manage the teaching week:** Set up classes and recurring schedules, then connect lessons to class sessions.
- **Create diagrams:** Arrange players and equipment on a playing surface.
- **Export and back up:** Save lessons as PDFs or images, and export backups to transfer planning data between devices.

## Support and privacy

Visit the [support page and FAQ](support.html) for help getting started, or read the [privacy policy](privacy.html) for information about data storage and sharing.

For support or privacy questions, contact [ryansapps@outlook.com](mailto:ryansapps@outlook.com).

## Website

The site uses HTML and CSS, with no dependencies or build step.

| File | Purpose |
| --- | --- |
| `index.html` | App overview and screenshots |
| `support.html` | Support contact and FAQ |
| `privacy.html` | Privacy policy |
| `styles.css` | Shared styles and responsive layout |
| `assets/` | App icon and screenshots |
| `.nojekyll` | Static hosting configuration for GitHub Pages |

### Local preview

Open `index.html` in a browser, or run the following command from the website directory:

```sh
python3 -m http.server 4173
```

Then visit [localhost:4173](http://localhost:4173).

### GitHub Pages

With the website files at the repository root, open **Settings → Pages**, select **Deploy from a branch**, choose **main** and **/(root)**, and save. All page and asset links are relative, allowing the site to run under a repository path or a custom domain.
