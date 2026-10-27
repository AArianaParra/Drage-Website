# Drage CPA website, restructure draft (v1)

A static HTML/CSS prototype of the restructured drage.com. It has no build step and no dependencies.

## Pages

| File | Page |
| --- | --- |
| `index.html` | Home: hero, Who We Help, services index, offices, testimonials, Insights teaser |
| `about.html` | About: Our Story, Leadership, Our Team grid (28 people, 5 groups), offices |
| `international-individuals-families.html` | Sample audience page (template for the other 4 "Who We Help" pages) |
| `contact.html` | Contact form + office cards (Coral Gables, India, Mexico) |
| `assets/css/styles.css` | Shared base styles |
| `assets/img/` | Drage logo (positive for light backgrounds, white-text version for dark) |

## Preview locally

Open `index.html` in a browser, or run:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Upload to GitHub

```bash
cd drage-website
git init
git add .
git commit -m "Drage website restructure draft v1"
git branch -M main
git remote add origin https://github.com/<your-org>/drage-website.git
git push -u origin main
```

Create the repository as **Private** first. The draft lists staff names and titles and contains unpublished placeholders.

## Before it goes live (open items)

- [ ] Replace initials avatars with headshots (square, 800×800 px min, `firstname-lastname.jpg`). Only add photos for people who have given consent.
- [ ] India office: street address, city, PIN, phone (footer of `index.html` and `contact.html`)
- [ ] Mexico office city, or "Remote team"
- [ ] Leadership bios and specialties, Our Story text, stats marked `[XX]`
- [ ] Testimonials pasted verbatim (only Arnaud Granville's is final)
- [ ] FAQ answers on the audience page
- [ ] Build the other 4 audience pages from `international-individuals-families.html`
- [ ] Wire the contact form to a secure form handler (HTTPS, spam protection). It currently has no backend. Do not collect SSNs, ITINs or account numbers. Documents go through the ShareFile client portal only.
- [ ] Spanish / Portuguese versions (the EN · ES · PT selector is a placeholder)

## Notes for Skyway Media

- The layout is written as inline styles exported from the design draft. Move them into the WordPress/Elementor theme or `styles.css` as you see fit.
- Brand: navy `#0B2154`, footer navy `#08183F`, accent gold `#C9A46A`, warm gray `#F4F2EC`. Fonts: Source Serif 4 (headings), Inter (body).
- The logo comes from the current drage.com site. The white-text footer version was derived from it, so swap in an official white logo if one exists.
