# Water Treatment Laboratory — Academic Website Starter

A responsive, English-language website for **Dr. Alireza Jalali** and the **Water Treatment Laboratory** at the University of Tehran. Built with **GitHub Pages + Jekyll + Pages CMS**. Blue-and-white Modern Editorial design, split homepage hero, and content editing without touching site code.

> **Before launch:** Have the professor approve the English laboratory name, title, introductory text, publications and contact information. The Google Scholar profile was rate-limited during research; publications included here were verified against publisher records separately. No student profiles, open positions, projects, or news items have been invented. Upload an approved professor portrait.

## 1. Upload to GitHub (no coding required)

1. Create a **free GitHub account**. Ideally use an account owned by the professor or an institutional organization, with student editors granted collaborator access.
2. Create a **Public** repository named **`YOUR-USERNAME.github.io`** (replace with the exact GitHub username). If using an organization, use its exact name.
3. Extract the ZIP. Upload **all its contents** to the *root of the repository*, **not the outer folder and not the ZIP**. Include hidden `.pages.yml` and `.gitkeep` files. If hidden files are not visible, use your file manager's *show hidden files* option or create `.pages.yml` manually in GitHub.
4. In the repository open **Settings → Pages → Build and deployment**. Select **Deploy from a branch**, branch **`main`**, folder **`/(root)`**, then **Save**.
5. When GitHub Pages finishes building, visit **`https://YOUR-USERNAME.github.io/`**. If GitHub reports a build error, inspect **Actions** or the Pages build log.

If you use a normal project repository such as `water-lab` rather than `YOUR-USERNAME.github.io`, change `_config.yml` to:

```yaml
url: "https://YOUR-USERNAME.github.io"
baseurl: "/water-lab"
```

The best beginner route is the root user-site name described above, with `baseurl: ""`.

## 2. Enable the content editor

1. Visit **https://app.pagescms.org/**.
2. Sign in with GitHub and install the Pages CMS GitHub App with permission **only for this repository**.
3. Open this repository on the `main` branch. Pages CMS reads **`.pages.yml`** from the repository root.
4. Sidebar groups: **Website & Professor**, **Research & Publications**, **People & Opportunities**, and **News, Teaching & Recognition**.
5. Edit an item and save. Pages CMS writes the changes into GitHub; GitHub Pages then rebuilds the site. A visible change may take several minutes.
6. For new entries, set **Published on Website = true** when the information is confirmed. New items are drafts by default.

Pages CMS documentation: https://pagescms.org/docs/quick-start/

## 3. What the professor can edit

| Task | Section in Pages CMS | Result |
|---|---|---|
| Name, email, hero, social links, portrait | Website & Professor → Site Settings & Contact | Homepage, About, footer and Contact updated |
| Biography | Website & Professor → Professor Biography | About page updated |
| Research focus | Research & Publications → Research Areas | Research page and homepage cards |
| New research projects | Research Projects | Projects page |
| Publications | Publications | Searchable and year-filtered publication listing; featured papers on homepage |
| Current students and researchers | People & Opportunities → Team Members & Alumni | People page; select Alumni toggle for former members |
| Calls for applicants | Open Positions | Opportunities page; choose Open or Closed |
| News and updates | News & Updates | News page; latest approved items appear on homepage |
| Courses | Teaching | Teaching page |
| Honors | Awards & Honors | Awards page |
| Talks | Talks & Media | Talks page |

For an item to be visible it must have **Published on Website** enabled. To remove an item from public display, turn that toggle off and save. The item stays in the GitHub repository. **GitHub public repositories are publicly readable even when a CMS item is unpublished. Never store private student details, confidential documents or unpublished sensitive research in this repository.**

### Portrait and laboratory photos

- Go to **Website & Professor → Site Settings & Contact**.
- Replace **Professor Portrait** with a photo that the professor authorizes.
- Optionally replace **Hero Laboratory Image** with an approved group or laboratory photo.
- Image uploads go to `assets/uploads/` automatically. Prefer compressed JPG or WebP images (under roughly 500 KB–1 MB each when possible).
- The bundled SVG illustrations are original decorative placeholders; they are not actual photographs of the laboratory.

### Publication maintenance

The initial publication selection is manually curated, **not synced** to Google Scholar. Add publications through the CMS and include title, authors, venue, year, and DOI. Do not paste a full DOI URL in the DOI field: enter only `10.xxxx/...`. Choose **Feature on Homepage** for up to a few selected papers. If you want automatic Google Scholar import later, that would require a separate, carefully reviewed workflow; this starter does not claim to support it.

### Team entries

Use **Team Members & Alumni → New**. Enter full name, degree/role, approved photo, short description, and toggle Alumni for former members. Ask permission before publishing photos and personal information. **The professor's main profile is edited in Site Settings**, not in Team Members.

### Open positions

Use **Open Positions → New**, enter confirmed role/eligibility/deadline in Detailed Content, choose status Open or Closed, and set Published on Website. The default empty state makes **no promise of current openings**.

## 4. All 12 sections

Home; Research Areas; Research Projects; Publications; Our Team; Open Positions; News & Updates; About the Professor; Contact; Alumni; Teaching; Awards & Honors; Talks & Media (13 pages including Home, with 12 requested content sections).

## 5. Site architecture

- `_config.yml` — Jekyll configuration and collection permalink rules.
- `.pages.yml` — CMS editor schema: collections and forms.
- `_data/site.yml` — editable global site information, hero, and contact.
- `_data/about.yml` — editable biography.
- `_areas`, `_projects`, `_publications`, `_people`, `_positions`, `_news`, `_teaching`, `_awards`, `_talks` — editor-managed content.
- `_layouts`, `_includes` — reusable templates. Changes to the design are technical, unlike editing content.
- `assets/css/main.css` — typography, colors and responsive styling.
- `assets/js/site.js` — mobile navigation and publication filtering, no dependencies.
- `assets/img/` — bundled original SVG illustrations and temporary portrait placeholder.
- `assets/uploads/` — uploaded images and documents.

## 6. Optional local development

With Ruby/Bundler installed, run `bundle install` and `bundle exec jekyll serve`, then open `http://127.0.0.1:4000`. Local installation is **not needed** to upload the site to GitHub Pages.

GitHub Pages supports Jekyll from a branch without needing a separate database or paid hosting. This starter avoids custom Jekyll plugins.

## 7. Limits and handoff

- The CMS is for **content editing**, not arbitrary drag-and-drop redesigns. For changing core layout/navigation/CSS you (or another maintainer) edit code.
- GitHub Pages rebuild is not instant. Site visitors may see the previous version briefly after a CMS save.
- The hosted CMS requires GitHub authorization, and its account/permission features may change; test the professor's actual login and editing access before handing off.
- GitHub Pages is static: no password-protected backend, built-in application portal, or form submission database. The contact button opens email.
- Google Fonts may be unavailable in some networks; system serif and sans-serif fallbacks are included.
- All visible UI text and CMS field labels are in English. A separate Persian setup guide is included for the initial administrator.

## Verification references

See **`SOURCES_AND_FACT_CHECK.md`** for verified academic facts and publication DOIs, and what still requires professor approval.
