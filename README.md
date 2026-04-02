# Shopify Section Schema Builder

**A free, visual tool for generating valid Shopify section schema JSON — instantly.**

No coding required. No sign-up. No AI. Works completely offline.

<br>

[![Live Tool](https://img.shields.io/badge/Open%20Live%20Tool-%E2%86%92-96bf48?style=for-the-badge&logo=shopify&logoColor=white)](https://hussnain926.github.io/shopify-schema-builder/)
&nbsp;
[![Price](https://img.shields.io/badge/Price-Free-0f9d58?style=for-the-badge)](https://hussnain926.github.io/shopify-schema-builder/)
&nbsp;
[![No Signup](https://img.shields.io/badge/Signup-Not%20Required-3b82f6?style=for-the-badge)](https://hussnain926.github.io/shopify-schema-builder/)
&nbsp;
[![Offline](https://img.shields.io/badge/Works-Offline-f59e0b?style=for-the-badge)](https://hussnain926.github.io/shopify-schema-builder/)

<br>

---

## Live Demo

**[https://hussnain926.github.io/shopify-schema-builder/](https://hussnain926.github.io/shopify-schema-builder/)**

---

## The Problem This Solves

Every Shopify section requires a `{% schema %}` block. Writing it by hand is slow, error-prone, and tedious — especially for complex sections with multiple settings, select options, range sliders, and blocks.

This tool lets you build the entire schema visually in seconds:

- Click a field type from the left panel — it is added instantly
- Expand the field card to configure label, ID, default value, options, and info text
- Watch the valid JSON update live on the right as you type
- Click **Copy JSON** or **Copy .liquid** and paste it directly into your theme file

No wasted time. No syntax errors. No searching through Shopify documentation.

---

## Features

| Feature | Description |
|---|---|
| **22 field types** | Complete Shopify field type support — full list below |
| **Blocks support** | Add repeatable blocks with their own settings and `max_blocks` control |
| **Live JSON preview** | Syntax-highlighted output that updates in real time as you configure |
| **Copy as JSON** | Clean JSON ready to paste directly into your schema |
| **Copy as .liquid** | Output wrapped in `{% schema %}...{% endschema %}` tags |
| **Auto-generated IDs** | Field IDs generated automatically from the label — manually overridable |
| **Reorder fields** | Move any field up or down with a single click |
| **Presets toggle** | Include or exclude the presets block with one toggle |
| **Works offline** | Pure HTML and JavaScript — no server, no internet connection required |
| **Zero dependencies** | No frameworks, no npm, no build step, no configuration |

---

## Supported Field Types

### Text
`text` &nbsp;&nbsp; `textarea` &nbsp;&nbsp; `richtext` &nbsp;&nbsp; `inline_richtext` &nbsp;&nbsp; `html` &nbsp;&nbsp; `number` &nbsp;&nbsp; `liquid`

### Controls
`select` &nbsp;&nbsp; `radio` &nbsp;&nbsp; `checkbox` &nbsp;&nbsp; `range`

### Media
`image_picker` &nbsp;&nbsp; `video_url` &nbsp;&nbsp; `color` &nbsp;&nbsp; `color_background` &nbsp;&nbsp; `font_picker`

### Links
`url` &nbsp;&nbsp; `collection` &nbsp;&nbsp; `product` &nbsp;&nbsp; `blog` &nbsp;&nbsp; `page`

### Layout
`header` &nbsp;&nbsp; `paragraph`

---

## How to Use

**1.** Open the [live tool](https://hussnain926.github.io/shopify-schema-builder/)

**2.** Enter your section name in the top input bar

**3.** Click any field type in the left panel — it is added to the list instantly

**4.** Click the field card to expand it and configure:
   - Label and ID
   - Default value and placeholder text
   - Options with label and value pairs (for `select` and `radio`)
   - Min, max, step, and unit (for `range`)
   - Accept platforms (for `video_url`)
   - Default color (for `color` fields)

**5.** Switch to the **Blocks** tab to add repeatable blocks such as slides, cards, or tabs

**6.** Click **Copy JSON** or **{% %} .liquid** in the top right corner

**7.** Paste into your Shopify theme `.liquid` section file

---

## Example Output

```json
{
  "name": "Hero Banner",
  "settings": [
    {
      "type": "image_picker",
      "id": "image",
      "label": "Background Image"
    },
    {
      "type": "text",
      "id": "heading",
      "label": "Heading",
      "default": "Welcome to our store"
    },
    {
      "type": "range",
      "id": "heading_size",
      "label": "Heading Size",
      "min": 20,
      "max": 80,
      "step": 2,
      "unit": "px",
      "default": 48
    },
    {
      "type": "select",
      "id": "text_align",
      "label": "Text Alignment",
      "options": [
        { "label": "Left", "value": "left" },
        { "label": "Center", "value": "center" },
        { "label": "Right", "value": "right" }
      ],
      "default": "center"
    },
    {
      "type": "color",
      "id": "text_color",
      "label": "Text Color",
      "default": "#ffffff"
    },
    {
      "type": "checkbox",
      "id": "show_button",
      "label": "Show Button",
      "default": true
    }
  ],
  "presets": [
    {
      "name": "Hero Banner"
    }
  ]
}
```

---

## Pasting into Your Theme

Paste the `.liquid` output at the bottom of your section file:

```liquid
{% schema %}
{
  "name": "Hero Banner",
  "settings": [ ... ],
  "presets": [ { "name": "Hero Banner" } ]
}
{% endschema %}
```

---

## Run Locally

No installation required. Download and open directly in any browser:

```bash
git clone https://github.com/hussnain926/shopify-schema-builder.git
cd shopify-schema-builder
open index.html
```

Or [download the ZIP](https://github.com/hussnain926/shopify-schema-builder/archive/refs/heads/main.zip) and open `index.html` directly.

---

## Tech Stack

A single self-contained HTML file with no external runtime dependencies.

- **Vanilla JavaScript** — all state management and schema generation logic
- **CSS custom properties** — dark theme with live syntax highlighting
- **Google Fonts** — JetBrains Mono and DM Sans (loaded remotely, works offline with system fonts as fallback)
- **No frameworks. No npm. No build step.**

The entire tool is one file. Open `index.html` in any text editor to read and modify it.

---

## About the Developer

<br>

<table>
  <tr>
    <td>

Built and maintained by **Hussnain**, a Shopify and WordPress developer available for freelance projects worldwide.

If this tool saved you time, feel free to reach out. I am available for custom Shopify section development, full theme builds, WordPress projects, and ongoing store maintenance.

  </td>
  </tr>
</table>

<br>

[![Portfolio](https://img.shields.io/badge/Portfolio-hussnain926.github.io-96bf48?style=for-the-badge&logo=github-pages&logoColor=white)](https://hussnain926.github.io/)
&nbsp;
[![WhatsApp](https://img.shields.io/badge/WhatsApp-Message%20Me-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/923055498557?text=Hi%20Hussnain%2C%20I%20found%20your%20Shopify%20Schema%20Builder%20and%20need%20help%20with%20my%20project.)
&nbsp;
[![Phone](https://img.shields.io/badge/Phone-0305--5498557-0078D4?style=for-the-badge&logo=phone&logoColor=white)](tel:+923055498557)

---

## License

Free to use for personal and commercial projects.
Do not republish or redistribute this tool as your own work.

---

![GitHub Stars](https://img.shields.io/github/stars/hussnain926/shopify-schema-builder?style=social)
&nbsp;&nbsp;
**If this tool helped you, a star on the repository helps other developers find it.**
