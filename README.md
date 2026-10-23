# Azimuth

Azimuth is the corporate design language for established electronics manufacturers: companies with long product lifecycles, many sites and regulated customers. It is the corporate form of Meridian. It keeps Meridian's structure and token names, and changes the type, the color and the shape. It has a light and a dark theme, one brand color that each company sets, Source Sans 3 and Source Code Pro, and Lucide icons.

| System | For |
| --- | --- |
| Solaris | Dense management and collaboration apps |
| Meridian | Company sites for growing electronics companies |
| **Azimuth** | Corporate sites for established electronics manufacturers |
| Vesper | Developer and infrastructure tools |

Azimuth is a reference, not a component library. Each component is a definition (`README.md`) and a static HTML picture (`preview.html`). There is no JavaScript. Build the components in your own stack.

## Files

| Path | Content |
| --- | --- |
| `README.md` | This page. |
| `GUIDELINES.md` | Rules for principles, color, type, layout, content and accessibility. Read it before you build a page. |
| `tokens.json` | All tokens with a usage note for each token. |
| `tokens.css` | The same tokens as CSS custom properties and type classes. When you change a token, change both files. |
| `components/bundle.css` | Styles for the previews. It uses only the custom properties from `tokens.css`. |
| `components/<Name>/README.md` | The definition of one component: parts, states, content and when to use it. |
| `components/<Name>/preview.html` | A static HTML picture of one component. |

## Fonts and icons

The repository does not contain font or icon files. Get them from their own sources:

- **Fonts:** Source Sans 3 and Source Code Pro (Google Fonts). `components/bundle.css` loads them. Both cover Latin Extended, Greek and Cyrillic.
- **Icons:** Lucide (lucide.dev). Use the Lucide icon names.

## Theme

```html
<html data-theme="light" data-brand="navy"> <!-- brand: navy, petrol, crimson or graphite -->
```

With no `data-theme`, Azimuth follows the system setting. The brand sets `--brand`, `--brand-hover`, `--brand-pressed`, `--brand-subtle`, `--on-brand`, `--link` and `--focus` together. Do not set `--brand` alone. Component classes use the prefix `az-`.

## Components

AccessTag, BrandOptions, Breadcrumb, Button, Checkbox, ConsentBanner, ContactForm, ContactRail, Cover, DataTable, DownloadCenter, Footer, GlobalHeader, Icon, KeyFacts, Lifecycle, LocalNav, Logo, MasterData, MegaMenu, Notice, PageHeader, Pagination, PressList, ProductPage, RadioGroup, Select, StatusTag, Tabs, TextField, TextLink, ThemeToggle, TitleBlock
