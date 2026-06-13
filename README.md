# ABC Fonts — Font Repository

This is the font library for the **ABC Fonts** app.  
Add font files into the correct category folder and the app will load them automatically.

---

## 📁 Folder Structure

```
abc-fonts-repo/
│
├── ancient/
│   ├── Cinzel-Regular.ttf
│   ├── Cinzel-Bold.ttf
│   ├── Marcellus-Regular.ttf
│   ├── UnifrakturMaguntia-Regular.ttf
│   └── ... (any ancient/historical fonts)
│
├── serif/
│   ├── Merriweather-Regular.ttf
│   ├── PlayfairDisplay-Regular.ttf
│   └── ...
│
├── sans-serif/
│   ├── Roboto-Regular.ttf
│   ├── OpenSans-Regular.ttf
│   └── ...
│
├── display/
│   ├── Lobster-Regular.ttf
│   └── ...
│
├── handwriting/
│   ├── DancingScript-Regular.ttf
│   └── ...
│
├── monospace/
│   ├── FiraCode-Regular.ttf
│   └── ...
│
└── fonts.json   ← the app reads this file!
```

---

## 📋 fonts.json — Font List File

The app reads `fonts.json` from the root of this repo.  
Every time you add a font file, add an entry here too.

### Format:

```json
[
  {
    "f": "Cinzel",
    "c": "ancient",
    "tags": ["Roman", "inscription"],
    "civ": "Ancient Rome",
    "civDesc": "Roman stone-carved capitals from 1st century AD.",
    "file": "ancient/Cinzel-Regular.ttf"
  },
  {
    "f": "Merriweather",
    "c": "serif",
    "tags": ["editorial", "readable"],
    "file": "serif/Merriweather-Regular.ttf"
  },
  {
    "f": "Roboto",
    "c": "sans-serif",
    "tags": ["clean", "popular"],
    "file": "sans-serif/Roboto-Regular.ttf"
  }
]
```

### Fields explained:

| Field | Required | Description |
|-------|----------|-------------|
| `f` | ✅ Yes | Font display name (shown in the app) |
| `c` | ✅ Yes | Category: `ancient`, `serif`, `sans-serif`, `display`, `handwriting`, `monospace` |
| `tags` | No | Keywords for searching |
| `civ` | No | Civilisation label (ancient fonts only) e.g. `Ancient Rome` |
| `civDesc` | No | Short description of the font's historical origin |
| `file` | ✅ Yes | Path to the font file in this repo e.g. `ancient/Cinzel-Regular.ttf` |

---

## 🚀 How to connect to ABC Fonts app

1. **Upload your font files** into the correct folders above
2. **Edit `fonts.json`** to add each font entry
3. **Enable GitHub Pages** on this repo:
   - Go to repo **Settings → Pages**
   - Set source to **main branch / root**
   - Click Save — you'll get a URL like `https://yourusername.github.io/abc-fonts-repo`
4. **Open ABC Fonts app**, go to **Admin** (add `#admin` to the URL)
5. Paste your GitHub Pages URL into the **GitHub Repo URL** field
6. Click **Load from GitHub** — all your fonts appear instantly!

---

## ✅ Supported font formats

- `.ttf` — TrueType (recommended)
- `.otf` — OpenType
- `.woff` — Web Open Font Format
- `.woff2` — Web Open Font Format 2 (smallest file size)

---

## 💡 Tips

- Font file names **cannot have spaces** — use dashes instead: `My-Font-Regular.ttf`
- You can have **multiple weights** of the same font: `Cinzel-Regular.ttf`, `Cinzel-Bold.ttf`
- Ancient fonts **should always have** `civ` and `civDesc` fields so the golden badge shows in the app
- After adding fonts, the app caches them — click **Reload from GitHub** to refresh

---

## 📦 Example fonts.json (ready to use)

```json
[
  {
    "f": "Cinzel",
    "c": "ancient",
    "tags": ["Roman", "inscription"],
    "civ": "Ancient Rome",
    "civDesc": "Roman stone-carved capitals — same letterforms as Trajan's Column (113 AD).",
    "file": "ancient/Cinzel-Regular.ttf"
  },
  {
    "f": "UnifrakturMaguntia",
    "c": "ancient",
    "tags": ["Gothic", "Blackletter"],
    "civ": "Medieval Europe 12th-15th Century",
    "civDesc": "Gothic Blackletter — script of illuminated manuscripts and the Gutenberg Bible.",
    "file": "ancient/UnifrakturMaguntia-Regular.ttf"
  },
  {
    "f": "Merriweather",
    "c": "serif",
    "tags": ["editorial", "readable"],
    "file": "serif/Merriweather-Regular.ttf"
  },
  {
    "f": "Roboto",
    "c": "sans-serif",
    "tags": ["clean", "popular"],
    "file": "sans-serif/Roboto-Regular.ttf"
  }
]
```
