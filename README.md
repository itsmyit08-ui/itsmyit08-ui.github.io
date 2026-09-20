# itsmyit.in — digital visiting card

A single-page digital visiting card for **Besto Thomas**, Founder of
[itsmyit.in](https://itsmyit.in) — IT Infrastructure & Security Solutions.

Every contact detail is a live link: WhatsApp, phone, email, Instagram,
LinkedIn, Facebook and the website. "Save Contact" downloads a vCard or
offers a QR code another phone can scan to add the contact.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole card — no build step, no dependencies |
| `besto-thomas.vcf` | The contact as a vCard, also generated in-page |
| `og.png` | Link preview image for WhatsApp, LinkedIn and messaging apps |
| `favicon.png` | Browser tab icon |

Fonts come from Google Fonts; everything else (logo, icons, both QR codes)
is embedded in `index.html`.

## Editing it

Contact details, service tiles and copy are plain HTML in `index.html`.
Two things are generated and need regenerating if they change:

- The **Scan to Connect** QR encodes this site's own address. If the site
  moves to a different domain, regenerate it.
- The **Save Contact** QR encodes the vCard. If a phone number, email or
  title changes, update `besto-thomas.vcf` and regenerate that QR to match.
