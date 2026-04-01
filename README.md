# Edutech - Blogger Template

A modern, responsive Blogger template designed by **EduChainMagThemes**. Built for news, magazine, and educational blog sites with a clean, white, professional layout.

## Features

- **Responsive Design** — Fully responsive across desktop, tablet, and mobile devices
- **Featured Slider + 2x2 Grid** — Homepage hero section with auto-playing slider and 4-card grid
- **Category Sections** — Three customizable category blocks (Entertainment, Fun & Fashion, International)
- **Entertainment Layout** — Big card + small list side-by-side
- **Fun & Fashion** — 3-column image grid with dark overlay; supports adding multiple label widgets
- **International** — Horizontal slider carousel with colored label links and prev/next arrows
- **Latest Updates** — Paginated post listing with thumbnails and excerpts
- **Popular Posts** — Full-width card style with image and title overlay (dark gradient)
- **Related Articles** — Displayed on single post pages, matched by label and title similarity
- **Custom Breadcrumb** — `Home > Label > Post Title` navigation on single post and search pages (JS-injected)
- **Social Share Buttons** — Facebook, Twitter/X, WhatsApp, and Telegram share on single posts (JS-injected)
- **Auto Author Widget** — Sidebar widget auto-detects post author name and displays avatar initial
- **3 Sidebar Types** — Homepage-only, Single Post-only, and All Pages sidebar sections (all visible in Layout editor)
- **Continuous Sidebar** — Sidebar runs seamlessly alongside all homepage content sections
- **Headlines Ticker** — Animated top bar news ticker
- **White Background** — Clean white background throughout (body, footer, comments)
- **Ad Ready** — Multiple ad widget slots (header, between categories, after latest updates, sidebar)
- **Editable Footer Copyright** — Edit copyright text from Layout editor
- **Back to Top Button** — Floating scroll-to-top button
- **SEO Friendly** — Clean markup, semantic HTML, proper heading hierarchy
- **Fast Loading** — Minimal external dependencies

## Fonts

- **Open Sans** — Body text, metadata, descriptions
- **Roboto** — Headings, titles, navigation
- **Montserrat** — Site logo/header

## External Libraries

- jQuery 3.7.1
- Slick Carousel 1.8.1
- SlickNav 1.0.10
- Font Awesome 6.5.1
- Google Fonts

## Installation

1. Go to your Blogger Dashboard
2. Navigate to **Theme** → **Customize** → **Edit HTML** (or **Backup/Restore**)
3. Upload `edutech_template.xml` or paste the XML content
4. Save the theme

## Layout Editor Sections

| Section | Description |
|---------|-------------|
| `top_social` | Top bar social media icons |
| `header` | Site logo/title |
| `header_ad` | Header banner ad (728x90) |
| `navmenu` | Main navigation menu |
| `featured_section` | Featured slider configuration |
| `cat_section_1` | Category 1 — Entertainment (label-based) |
| `cat_section_2` | Category 2 — Fun & Fashion (label-based, supports adding more widgets) |
| `ad_between_cats` | Ad block between category sections |
| `cat_section_3` | Category 3 — International slider (label-based) |
| `ad_after_latest` | Ad block after Latest Updates |
| **`home_sidebar`** | Sidebar widgets — **Homepage only** (blue label) |
| **`post_sidebar`** | Sidebar widgets — **Single Post only** (orange label) |
| **`sidebar_section`** | Sidebar widgets — **All pages except Home** (green label) |
| `footer_1` | Footer column 1 — About |
| `footer_2` | Footer column 2 — Labels |
| `footer_3` | Footer column 3 — Social |
| `footer_copyright` | Footer copyright text (editable) |

### Sidebar Architecture

The three sidebar sections are placed **outside** of any `<b:if>` conditional in the HTML body so they always appear in the Blogger Layout editor. Each section is wrapped in a `<div class="sidebar-inject-wrap">` that is hidden by default on the live site (`display: none`). On non-homepage views, JavaScript moves `post_sidebar` and `sidebar_section` into the `.content-layout` as an `<aside>` element for the two-column layout. Widget-level `<b:if>` conditions control which widgets render on which page type.

### Auto Author Widget

The `post_sidebar` includes an "About Author" widget that automatically detects the post author name from `showAuthor` metadata. It displays an avatar with the author's initial letter (blue circle) and the author name. No manual configuration needed.

## Customizing Categories

Each category section widget uses a **label name** as its content. To change which posts appear:

1. Go to **Layout**
2. Click **Edit** on the category widget (e.g., Entertainment)
3. Change the **Content** field to your desired Blogger label name
4. Change the **Title** to the display name
5. Save

### Adding More Labels to Fun & Fashion (cat_section_2)

`cat_section_2` supports adding new HTML gadgets. Each new widget is auto-initialized as a Fun & Fashion grid:

1. Go to **Layout** → find `cat_section_2`
2. Click **Add a Gadget** → choose **HTML/JavaScript**
3. Set **Title** to the display name (e.g., "Technology")
4. Set **Content** to the Blogger label name (e.g., "Tech")
5. Save — the new category grid will render automatically

## Color Customization

The primary color (`#2C91E1`) can be changed from **Theme** → **Customize** → **Advanced** → **Primary Color**.

## License

Designed by EduChainMagThemes. Free for personal and commercial use.
