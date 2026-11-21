# Promotional Poster · Image-Generation Prompts (Hede Language · v2.1)

> Usage: produce the image in "two steps" — **Step 1** use the prompt to generate a text-free base image, **Step 2** overlay the copy list.
> Why two steps: having AI image generators render Chinese text directly tends to produce broken or wrong characters (based on real-world testing); base image + text overlay is the reliable approach.
> Any text-overlay tool works: Jimeng / Canva / Gaoding / PPT / PS are all fine — just lay out the text from the copy list.
> Recommended size: **3:4 portrait** (export at 1080×1440 or 1242×1660 for clarity in WeChat groups).

---

## Step 1 · Base-image prompt (copy into MiniMax image generation)

### Chinese version (preferred)

```
Vertical tech-style poster background, 3:4 ratio. Background is a gradient from deep blue to dark purple (deep-sea blue to starry-night purple),
with a glowing translucent crystal-textured brain in the center, blue data light streams and particles flowing inside.
Four floating glowing small icons arranged in an arc around the brain, each with a soft halo: a golden pushpin,
a cyan magnifying glass, an open blue book, a bright yellow lightning bolt.
Tiny stars and light spots scattered around; the bottom third is left as a clean, deep gradient blank area
(reserved for later text overlay), with a clean and simple blank area at the top.
Overall style: premium, high-end tech feel, clean and translucent, with breathing room, visually focused on the center.
No text, letters, numbers, watermarks, or logos anywhere in the image.
```

### English version (backup; some models understand English more reliably)

```
Vertical tech-style poster background, 3:4 ratio. Deep navy-to-dark-purple
gradient background. In the center, a glowing translucent crystal brain with
blue data streams and particles flowing inside. Four floating glowing icons
arranged in an arc around the brain, each with soft halo: a golden pushpin,
a cyan magnifying glass, an open blue book, a bright yellow lightning bolt.
Tiny stars and light spots scattered around. The bottom third is a clean,
dark gradient area (reserved for text overlay). Top area minimal and clean.
Style: premium, futuristic, clean, focused. No text, no letters, no numbers,
no watermark, no logo.
```

---

## Step 2 · Text-overlay copy list (lay out as-is; do not change the wording)

| Level | Copy | Layout suggestion |
|---|---|---|
| Main title | **Hede Language** | Centered at the very top, extra-bold sans-serif, white; may include a small English subline "HEDE LANGUAGE" (the formal language name; the skill identifier hede-thinking does not need to appear on the poster) |
| Subtitle | Teach your AI to think logically · close with a plain-language version | Below the main title, medium size, light blue-white |
| Four-tag line | 📌 Every assertion must carry an anchor　🔍 Every to-verify must be closed | Can be laid out in two lines: |
| | 📚 Every new insight must be memorized　⚡ Every action must be backfilled | Pair each emoji with a short phrase, evenly distributed |
| Selling point (choose one) | A: One prompt, drop it into any AI | Lower middle, small size |
| | B: Make every "I verified it" traceable to the end | Same as above; choose one of the two |
| Call to action | Reply "**Hede Language**" in the WeChat group to get the skill | Bottom, accent color (bright yellow / cyan) |
| Version footnote | Hede Thinking skill v2.1 · New /eli5 plain-language version | Very bottom, small text, semi-transparent white |

### Layout tips

1. Keep the main title and four-tag line **clear of** the central brain in the base image; place them in the top blank area and the bottom dark area;
2. For the four-tag line, consider giving each emoji a semi-transparent rounded card background (white at 10% opacity) for better readability;
3. The call to action is the key to conversion — give it the strongest visual contrast (bright color + bold).

---

## Alternative · One-step direct output (version with text; try your luck)

> Risk note: Direct output of large blocks of Chinese text will most likely produce broken characters; only try this if you can't be bothered to overlay text. If wrong characters appear, fall back to the two-step approach.

```
Vertical 3:4 tech poster, deep blue-purple gradient background, glowing crystal brain in the center, four glowing icons around it:
golden pushpin, cyan magnifying glass, blue book, yellow lightning bolt. Large headline at the top of the poster "Hede Language",
with a line of small text below it "Teach your AI to think logically", and a line of bright yellow small text at the bottom "Copy the prompt, drop it into your AI".
Text in Simplified Chinese, clear with no wrong characters, no other text anywhere.
```

---

## Delivery and archiving

- Suggested names for the generated base image and final image: `poster-base.png` (base image) / `poster.png` (final image)
- Website deployment: put `poster.png` in this directory and replace the "poster placeholder" at the end of `hede-bench.html` with this image.
