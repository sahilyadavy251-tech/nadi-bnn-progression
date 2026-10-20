# Nadi (BNN) + Slow-Planet Progression

A **single-file, offline** Vedic astrology tool for two things that are hard to find in one place:

1. **Bhrigu Nandi Nadi (BNN)** &mdash; planetary **bonds** (yuti) and trine circuits
2. **Slow-Planet Progression** &mdash; Jupiter, Saturn and Rahu/Ketu sign changes by age

No build step. No npm. No server. No internet. Open `index.html` and it works.

---

## What it does

### Nadi (BNN)
BNN reads **relationships between planets**, not houses.

- Two planets in the **same sign** form a **yuti** (bond)
- The planet with the **lower degree leads** the bond
- Each pair gets a relation from a classical friend/enemy table: **Friendly**, **Inimical** or **Neutral**
- Every planet is placed in a **trine circuit** &mdash; Dharma (1,5,9), Artha (2,6,10), Kama (3,7,11) or Moksha (4,8,12)
- Hero planets: **Venus** (male chart) / **Mars** (female chart) for marriage, **Jupiter** for children, **Saturn** for karma

### Slow-Planet Progression
A planet changes sign at a fixed rate. The tool shows the **age range** for each sign the planet occupies across the life.

| Planet | Major cycle | Minor |
| --- | --- | --- |
| Jupiter | 12 years | 1.0 |
| Saturn | 30 years | 2.5 |
| Rahu / Ketu | 18 years | 1.5 |

A **retrograde** planet is progressed **backwards** through the signs.

---

## Use it

### In a browser
Open `index.html`. Enter birth date, time, place (or latitude/longitude) and a timezone offset. Press the button.

### Embed it in your own page
```html
<iframe src="index.html" style="width:100%;height:900px;border:0"></iframe>
```

### Call it from your own code
```js
// rebuild with the current form values
window.__nadiBuild();

// or drive the engine directly
KV.computeChart({ date: new Date(), lat: 28.6139, lon: 77.2090 });
KV.nadiChart(chart);
KV.planetProgression(chart, 'Jupiter', 30);
```

The `KV` object also exports `computeAll`, `vimshottari`, `shadbala`, `ashtakavarga`, `charaKarakas`, `kpChart`, `panchang`, `yogasDoshas`, `chalit`, `careerRules` and `numerology`.

---

## Accuracy

- **Sidereal** zodiac with the **Lahiri** ayanamsa
- **Whole-sign** houses
- Ephemeris: [Astronomy Engine](https://github.com/cosinekitty/astronomy), inlined and unmodified
- Timezone is a **fixed UTC offset** entered by the user &mdash; this tool does not carry a timezone database, so enter the correct offset for the birth date

Astrology is a traditional system of guidance. This tool does not predict events and is not a substitute for medical, legal or financial advice.

---

## Part of Advanced Occult Astrology

This tool is extracted from **[Advanced Occult Astrology](https://advanced-occult-astrology.pages.dev)** &mdash; a free Vedic astrology app with 20 divisional charts (D1 to D60), Vimshottari dasha to four levels, Shadbala, Ashtakavarga, Jaimini Chara Karakas, KP system, Golden Time and daily horoscope.

- **Website:** https://advanced-occult-astrology.pages.dev
- **Free D9 (Navamsa) calculator:** https://advanced-occult-astrology.pages.dev/d9-navamsa-chart.html
- **Free D10 (Dashamsa) calculator:** https://advanced-occult-astrology.pages.dev/d10-dashamsa-chart.html
- **Daily horoscope:** https://advanced-occult-astrology.pages.dev/horoscope.html
- **Author:** Sahil Rao &mdash; Hansi, District Hisar, Haryana, India
- **Contact:** sahilyadavy251@gmail.com

---

## Licence

MIT. Use it, fork it, embed it, ship it in your own app.
