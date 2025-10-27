# Africa Travel Biz - Landing Page

A bilingual (English/Japanese) website for Africa Travel Biz - Your Concierge for Business and Research in Africa.

## 🎯 Site Purpose

Convey trust, professionalism, and reliability for business travel and research support in Africa through a trusted local network and Japanese-quality coordination.

## ✨ Key Features

### Hero Section
- **Main Copy**: アフリカ出張・視察を、安心・安全・スムーズに
- **Sub Copy**: 現地ネットワーク × 日本品質で、貴社のアフリカビジネスを支援します
- **CTA**: とりあえず気軽に無料相談
- **Background**: Needs professional image of African business cities/airports/local landscapes

### Sections Implemented
1. ✅ Hero Section - First impression with trust & professionalism
2. ✅ Problem Section - Customer pain points
3. ✅ Solution Section - The only concierge directly connected with Africa
4. ✅ Our Role - Not a travel agency, but a business concierge
5. ✅ Services - 5 service categories
6. ✅ Strengths - Why choose us (5 advantages)
7. ✅ Case Studies - Real client examples (Kenya, Tanzania, Ethiopia)
8. ✅ Flow - 5-step process
9. ✅ Final CTA - Free consultation

## 🚀 Getting Started

```bash
npm start
```

Visit: `http://localhost:3000`

## 📝 To Add Background Image

1. Find a professional image of African business settings (cities, airports, landscapes)
2. Place the image in the root directory as `hero-bg.jpg`
3. Add to `index.html` in the hero section:

```html
<section class="hero" style="background-image: url('hero-bg.jpg'); background-size: cover; background-position: center;">
```

Or add to `styles.css`:

```css
.hero {
    background-image: url('hero-bg.jpg');
    background-size: cover;
    background-position: center;
}
```

## 🌐 Bilingual Support

- **Language Toggle**: Top right navigation
- **Auto-detect**: Remembers user preference
- **Full Translations**: EN/JP for all content

## 📁 File Structure

```
├── index.html          # Main HTML structure
├── styles.css          # CSS styling (reused from existing)
├── script.js           # JavaScript functionality (reused)
├── translations.js     # Bilingual translations
└── package.json        # Project metadata
```

## 🎨 Site Name

**Africa Travel Biz** (without brackets in the UI)

## 📞 Contact Information

- **Email**: info@africatravelbiz.com
- **Office**: Tokyo, Japan

---

Built with HTML, CSS, and JavaScript.
