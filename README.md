# Varun Naidu | Digital Marketing Portfolio

A responsive, single-page portfolio showcasing work across technical SEO, Generative Engine Optimization (GEO), Answer Engine Optimization (AEO), performance marketing, analytics and sales enablement, plus a photography section with travel albums.

Built with HTML, CSS and vanilla JavaScript. No framework, no package installation and no build step.

## Files

The whole site is just three files. Keep them in the same folder:

```text
your-repository/
├── index.html
├── Varun_Naidu_Resume.pdf
└── README.md
```

All photos are embedded inside `index.html`, so there is no `photos` folder to upload. The only file the page links to is the resume PDF, so keep it beside `index.html` with the exact name `Varun_Naidu_Resume.pdf`.

## What's on the Page

- **Results**: headline metrics for organic search, AI-search visibility and paid campaigns
- **About**: professional snapshot
- **Work**: selected projects with case-study dialogs and category filtering
- **Tools**: marketing ROI estimator and workflow explorer
- **Skills**: filterable skills with supporting evidence
- **Experience**: career timeline
- **Certifications**: Anthropic, Google, LinkedIn/Microsoft, eMarketing Institute and AIGPE
- **Photography**: album-based gallery (see below)
- **Contact**: email, phone and a downloadable resume

### Selected Projects

1. **Technical SEO & Organic Growth**: crawlability fixes, JSON-LD and FAQ schema, `robots.txt`, internal linking, keyword and metadata work, Search Console reporting.
2. **Generative Engine Optimization (GEO) & Answer Engine Optimization (AEO)**: AI-search visibility strategy, an `/llms.txt` knowledge bundle, and location-focused landing pages.
3. **Meta Ads Campaign Performance**: 68 campaigns managed, with reporting on delivery, leads, impressions, spend and cost per lead.
4. **Sales Enablement Tools**: a pricing calculator and proposal generator for the sales team.

The figures on the page are reported platform and website-level metrics. They do not by themselves prove that a particular action caused the results. Generative AI reporting reflects impressions, not clicks, and does not cover every AI platform.

## Photography Albums

The Photography section shows an album card for each album. Clicking a card opens its photos in a grid, and clicking a photo opens a full-screen viewer with next/previous buttons, arrow-key support and Esc to close. An "All albums" button goes back to the album list.

| Album | Photos |
|---|---|
| Kashmir | 10 |
| Sikkim | 97 |

The photos are stored inside `index.html` as compressed WebP images (about 1280px on the long edge), which makes the file roughly 6.5 MB. The page loads photos only as you scroll, but the browser still has to download the whole HTML file once, so the first load can take a few seconds on a slow connection.

### Adding photos later

Because the photos are embedded, adding or changing them means regenerating the embedded data, which is easiest to do by asking Claude (send the new photos and the album name). If you prefer to do it yourself:

1. Resize photos to about 1280px on the long edge and save them as WebP.
2. Convert each to a base64 data URI (`data:image/webp;base64,...`).
3. Add it to the `window.PHOTO_DATA` object in `index.html` under the key `album/file-name.jpg`, for example `"sikkim/sikkim-98.jpg"`.
4. Add a matching line to that album's `files` list in the `Photography albums` script:

   ```js
   {f:"sikkim-98.jpg",alt:"Short description of the photo",cap:""},
   ```

   `alt` is a short description for screen readers, `cap` is an optional hover caption, and the order of the lines is the display order.

To add a new album, copy an album block in the same script and give it a new `id`, `name` and `folder`, then add its photos to `PHOTO_DATA` using the `id` as the key prefix.

Note: if a photo has no entry in `PHOTO_DATA`, the page falls back to the `folder` path (for example `photos/sikkim/sikkim-98.jpg`). If that file is not there either, the tile shows "Photo coming soon".

### Photo privacy tip

Phone photos can contain GPS coordinates in their metadata. The embedded photos have had that metadata removed. Do the same for any photo you add.

## Resume Download

The Download Resume buttons link to `Varun_Naidu_Resume.pdf`. Keep the PDF beside `index.html`. To publish an updated resume, replace the file and keep the same name.

## Contact

The contact section lists email, phone and a resume download. There is no contact form, so nothing needs a form service or backend.

## Technology Stack

| Technology | Usage |
|---|---|
| HTML5 | Page structure and content |
| CSS3 | Layout, responsive styling, light/dark themes, effects |
| Vanilla JavaScript | Filters, calculators, album gallery and viewer, navigation |
| JSON-LD / Schema.org | Person and professional profile structured data |
| Local Storage | Remembering the selected theme |
| SVG | Favicon and interface icons |

## SEO, Accessibility & Metadata

- Page title and meta description
- Open Graph and Twitter/X card metadata
- JSON-LD structured data
- Skip-to-content link and keyboard focus indicators
- Semantic HTML, accessible labels and image descriptions
- Reduced-motion support
- Responsive layout and light/dark colour schemes

## Run Locally

Option 1: open `index.html` in your browser.

Option 2: serve it locally (recommended):

```bash
cd your-repository
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Deploy with GitHub Pages

1. Upload the three files (`index.html`, `Varun_Naidu_Resume.pdf`, `README.md`) to the root of a GitHub repository.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the `main` branch and the `/ (root)` folder, then click **Save**.
5. Wait a minute or two. The site will be at `https://YOUR_USERNAME.github.io/YOUR_REPOSITORY/`.

## Professional Experience

- **Amonex Technologies Pvt. Ltd.**, Marketing Lead, August 2025 – Present
- **Lawyal Tech**, Marketing Consultant, February 2025 – April 2025
- **Allied Blenders & Distillers Ltd.**, Territory Sales Executive, January 2023 – July 2024
- **R.N. Enterprises Pvt. Ltd.**, Sales & Marketing Specialist, October 2021 – December 2022

## Contact Details

**Varun Naidu**

- Email: varunnaiduu7@gmail.com
- LinkedIn: https://www.linkedin.com/in/varun-naidu--/
- Portfolio: https://varunnaiduu.github.io/Varun-Naidu-Portfolio/

---

*Portfolio built with HTML, CSS and vanilla JavaScript.*
