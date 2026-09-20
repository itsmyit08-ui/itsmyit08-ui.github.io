# itsmyit.in — digital visiting cards

Interactive 3D digital visiting cards for **ItsMyIT** — IT Infrastructure &
Security Solutions. One public page per person, hosted free on GitHub Pages.

| Page | Who |
| --- | --- |
| [`/`](https://itsmyit08-ui.github.io/) | Besto Thomas, Founder |
| [`/justin.html`](https://itsmyit08-ui.github.io/justin.html) | Justin Sebastian, Co-Founder |
| [`/akhil.html`](https://itsmyit08-ui.github.io/akhil.html) | Akhil Thomas, Co-Founder |

Every contact detail is a live link: WhatsApp, phone, email, Instagram,
LinkedIn, Facebook and the website. The card flips to a back face with the
services and the main actions. **Save Contact** downloads a vCard (or offers a
QR code another phone can scan), and **Share My Card** uses the phone's own
share sheet, falling back to copying the link.

## Files

| File | What it is |
| --- | --- |
| `index.html`, `justin.html`, `akhil.html` | The three cards — one self-contained page each |
| `*.vcf` | Each contact as a vCard, also generated in-page |
| `og.png`, `justin-og.png`, `akhil-og.png` | Link preview images for WhatsApp, LinkedIn and messaging apps |
| `favicon.png` | Browser tab icon |
| `.nojekyll` | Publish the files as they are, with no Jekyll pass |

No framework, no build step at serve time, no dependencies. Fonts come from
Google Fonts; everything else — logo, icons, both QR codes, the vCard — is
embedded in the page. All of the 3D is CSS transforms, and it respects
`prefers-reduced-motion`.

## Editing it

The three pages are **generated from one template**, so they stay identical
apart from name, title and email. Editing a page by hand works, but the next
regeneration overwrites it — change the template instead.

Two things are generated and need regenerating if they change:

- The **Scan to Connect** QR encodes that page's own address. If a card moves
  to a different domain, regenerate it.
- The **Save Contact** QR encodes the vCard. If a phone number, email or title
  changes, update the matching `.vcf` and regenerate that QR.
