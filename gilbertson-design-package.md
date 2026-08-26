# Design Package: Gilbertson Fine Homes, "Built to be Inherited"

Tier 3 choreographed build. The single deliverable of the Creative Director's Loop. Every line of viewer-facing copy below ships verbatim. Band ranges and pacing numbers are labeled starting points, validated later by the flick test in `scrub-pipeline.md`.

Project folders:
- Deploy folder: `gilbertson/` (`index.html` + `assets/`), nothing else ships.
- Review folder: `gilbertson-review/` (raw generations, extracted frames, audit files). Never zipped, never deployed.

---

## 1. The brand premise

One word carries the whole site: **inheritance**. A production house is built for the market. A Gilbertson home is built for a family's name, to be lived in now and handed down later. Every section teaches and sells that one idea: the hero film shows a home being imagined, built, lived in, and sealed behind its own gate; the process section shows the discipline that makes a house worth inheriting; the islands section grounds it in a real place; the consultation is framed as the first conversation about a generational asset, not a lead form. If a section does not serve inheritance, it does not belong on the page.

Real-business facts the site may state as true (from the builder's own public materials): led by a hands-on Red Seal carpenter; serves Nanaimo, Ladysmith, and central Vancouver Island; builds on the Gulf Islands including Saltspring and Gabriola, including remote sites; trained in Built Green and Net Zero construction; handles permits and licensing; transparent pricing as a stated principle. Everything else (years in business, homes completed, awards, client names) is a clearly marked placeholder the owner fills in.

## 2. The palette as CSS tokens

Sampled from the storyboard's world: dusk over BC coastal mountains, mist, cedar, and amber interior light through glass. Exact values get finalized from the approved footage after the video gate; these are the direction.

```css
:root{
  --canvas:#10141a;        /* dusk charcoal-blue, tinted toward the mountain footage, never pure black */
  --panel:#1a212b;         /* raised surfaces, night-sky slate */
  --mist:#8fa3ad;          /* the island mist, cool secondary tone for rules and quiet labels */
  --accent:#c89a5e;        /* amber: interior light through glass at blue hour; the CTA and rare emphasis */
  --accent-hover:#dcae6f;
  --accent-muted:#5c4a30;  /* the accent at whisper level: borders, glows, particles */
  --text-secondary:#9aa7b2;
  --text-primary:#f2ede4;  /* warm ivory, never pure white */
}
```

## 3. The type trio

- Display: **Fraunces** (weights 300, 500; optical size high, "SOFT" axis low). A serif with warmth and craft, editorial without being a cliché luxury face.
- Body: **Newsreader** (400, 500). Quiet editorial serif, comfortable at length, reads like a well-set brochure for a firm that does not need to shout.
- Mono: **IBM Plex Mono** (400). Small labels only, styled as drawing-set annotations: section numbers read as architectural sheet numbers (A-101, S-201, L-301), coordinates, and spec labels. This is the construction-documents motif, and it is the only place the mono appears.

Loaded from Google Fonts, trimmed to exactly these weights, with preconnect.

## 4. The film: storyboard and segments

Three segments, 15 seconds each, generated on **kling-video-v3_0** (multi-shot on, no audio, 15 seconds, 16:9), each chained by extracting the previous segment's final frame as the next segment's start image. Joined with the single-encode concat into one 45-second scrub film. Three segments instead of two so every one of the brief's 14 beats gets its own window, none doubled up. Seam 1 lands inside the blueprint dissolve (a full texture refresh); seam 2 lands inside the golden-hour light shift as the pull-back begins, which motivates the texture refresh the seam law requires.

Generation path, decided with the owner: the owner generates each step in their own Kling web account from the exact prompt and settings handed to them, and returns the original downloaded file in chat. Claude extracts each chaining frame as a lossless PNG. Same engine, same prompts, so same quality; the standing rules are original files only (no re-compressed transfers) and a watermark check on the first output.

The generator never sees any text. The faint logo reveal in the clouds and every caption are HTML/SVG overlays on the page, crisp and brand-accurate, never baked into footage.

Law-driven adjustments to the brief, said out loud:
- All people are distant figures or warm silhouettes seen through glass (Law 5: anatomy at detail breaks; silhouettes at distance render beautifully). The dinner gathering reads as amber warmth and human shapes, not close faces.
- The two vehicles are dark, sculptural, and unbranded (no-logos guard; real marques are trademarks).
- The logo-in-clouds beat is a page overlay timed to band 1, not generated imagery (Law 12).
- Contingency, decided now: if the kids-and-vehicles beat fails inspection twice, the yard resolves as landscaping, fountain, and closing gate alone. The story survives; the anatomy risk does not have to.

### The world, locked (art direction from the owner's reference film)

Every prompt below describes the same place and the same house, so the film reads as one estate from clouds to gate:

- **The valley:** a British Columbia mountain valley beneath a sheer granite cliff face with vertical rock striations, dense dark fir forest climbing its base, a flat meadow floor in muted sage and straw, low mist lying in ribbons through the treetops. Documentary drone photography, not fantasy landscape.
- **The house:** a grand modern-barn estate: a long row of steep-pitched gables stepping across the clearing, the central gable a full two-storey wall of black-steel-framed glass with a cascading glass-orb chandelier visible inside, flanking wings in dark stained timber, heavy stone chimneys, charcoal standing-seam roofs, a broad stone terrace and a dark still reflecting pool across the front.
- **The grade:** cool Pacific Northwest light throughout: silver, diffuse, desaturated greens and slate blues, mist always alive in frame. Warmth enters only as interior amber through glass and the golden-hour/blue-hour close. Never oversaturated, never golden-fantasy.

### Segment 1, "The Vision" (0 to 15s)

| Time | Beat | Camera and world |
|---|---|---|
| 0-3s | Clouds | Inside a luminous drifting cloud layer, soft morning light, slow descent begins |
| 3-6s | The island | Cloud breaks: aerial view of BC coastal mountains, fir forest, inlets, morning mist in the valleys |
| 6-9s | The vision | Continued descent to a top-down view of a glass-roofed modern-classic home, glass catching the light, reading as a vision more than a finished thing |
| 9-12s | Raw land | Camera tilts and drops toward eye level: the land is actually raw and cleared, a single walking trail, survey stakes; the house hangs as a translucent apparition over the site |
| 12-15s | The blueprint | The apparition dissolves into glowing white blueprint line-art of itself, clean drawn lines standing over the raw land; ends at eye level, still drifting gently forward |

Final frame (becomes segment 2's start): eye-level view of the glowing white blueprint line-art house standing on the raw cleared land, mountains behind, late-morning light. Extracted as full-quality PNG.

### Segment 2, "The Build" (15 to 30s)

| Time | Beat | Camera and world |
|---|---|---|
| 0-3s | Foundation | The blueprint lines settle onto the ground and become real: timber formwork and a freshly poured concrete foundation, mid-day, crisp shadows |
| 3-7s | Night works | Daylight slides to dusk then night: work lights cut through blue dark, an excavator, a concrete pump mid-pour, steam and dust drifting through the beams, small distant crew figures in hard hats |
| 7-11s | The frame rises | Time-lapse: timber framing climbs out of the foundation, framers as small figures on the structure, first light returning |
| 11-15s | The house | The skeleton resolves into the finished home at golden hour: wood, stone, warm metal, stairs and finishes visible through the glass; rests a beat on the finished house |

Final frame (becomes segment 3's start): eye-level view of the finished house glowing at golden hour, mountains behind. Extracted as full-quality PNG.

### Segment 3, "The Life and the Legacy" (30 to 45s)

| Time | Beat | Camera and world |
|---|---|---|
| 0-3s | The life inside | Golden hour deepens toward blue hour; a slow pull back begins: amber interior glow, a couple and their friends gathered at a long dinner table seen through the tall glass as warm silhouettes, in a warmly classic interior: wood paneling, a marble floor, elegant traditional furniture, a grand staircase beyond |
| 3-6s | The door | The massive tall front door swings closed as the pull back continues |
| 6-9s | The yard | The landscaped front yard reveals itself: sculptural fountain centerpiece with moving water, two dark unbranded vehicles, small distant figures of children playing on the lawn |
| 9-12s | The retreat | The landscaping recedes into the periphery as the camera keeps drawing back down the driveway |
| 12-15s | The gate | A heavy estate gate closes across the frame and the shot rests on the sealed gate, home glowing beyond, blue hour |

Final frame (the page's settle): the closed gate centered with generous margin above and below, house warm behind it. Header-safe by design; verified with the header mocked over it before approval.

### The generation prompts (written now, submitted only after the gates)

**Start frame (image, 16:9, generated on the connector's strongest photoreal model — Nano Banana Pro / gemini-3-pro-image at high resolution — then animated by Kling video; generate multiple candidates, inspect, and show only the winner):**

> High-altitude aerial photograph looking down through a thin breaking layer of morning cloud over a British Columbia mountain valley. Through the widening break on the left of frame, far below: a sheer granite cliff face with vertical rock striations rising out of dense dark-green fir forest, a flat meadow valley floor in muted sage and straw tones, and ribbons of low mist lying through the treetops. The right side of frame stays a soft unbroken field of cool white-grey cloud. Overcast Pacific Northwest light: silver, diffuse, slightly cold, one faint warm touch of early sun on the cliff top. Shot from a drone on a full-frame cinema camera, deep depth of field, razor-sharp detail in rock striations and individual fir crowns, subtle natural film grain, graded like a moody architectural documentary: desaturated greens, slate blues, no oversaturation, no fantasy glow. 16:9. No text, no logos, no lettering anywhere.

**Segment 1 video prompt (image to video, kling-video-v3_0, start image = approved start frame):**

> One continuous shot, no cuts. A slow steady drone descent through a thin breaking morning cloud layer into a British Columbia mountain valley: a soft beat of mist crosses the lens, then the world sharpens below, a sheer granite cliff face with vertical striations above dense dark fir forest, a flat sage-and-straw meadow floor, ribbons of low mist through the treetops, cool silver overcast light. The camera keeps descending toward a single cleared homesite at the forest edge where a grand modern-barn estate appears seen from directly above: a long row of steep charcoal gable roofs, dark timber wings, stone chimneys, a dark reflecting pool tracing the front terrace, soft light glancing off a central glass roofline. As the camera keeps sinking and tilts toward eye level it reveals that the front land is actually raw and cleared, bare earth with one narrow walking trail and survey stakes, and the estate now reads as a translucent architectural vision hanging over the site, and the vision dissolves into glowing white blueprint line-art of the same gabled estate, clean drawn lines standing in the air over the raw land beneath the granite cliff. The scene stays alive throughout: drifting mist, moving cloud shadows, trembling fir tops. The shot ends at eye level, still drifting gently forward, the glowing white line-art house on the raw land, cliff and firs behind, cool late-morning light, desaturated documentary grade. No text or lettering anywhere.

**Segment 2 video prompt (image to video, kling-video-v3_0, start image = segment 1's extracted final frame):**

> One continuous shot, no cuts, continuing the same slow forward drift over the same homesite. The glowing white blueprint lines of the house settle down onto the ground and become real: timber formwork and a freshly poured concrete foundation in crisp mid-day light. Daylight then slides into dusk and night: work lights snap on and cut through the blue dark, an excavator and a concrete pump working over the foundation with small distant crew figures in hard hats, steam and dust drifting through the beams of light. Time flows forward in a smooth time-lapse: timber framing climbs up out of the foundation into a long row of steep gable trusses stepping across the site beneath the granite cliff, small figures of framers moving along the structure as first light returns, and the timber skeleton resolves into the grand finished modern-barn estate at golden hour: steep charcoal gable roofs, dark stained timber, stone chimneys, the central two-storey glass gable glowing, a cascading glass-orb chandelier and an elegant staircase visible through the black-steel-framed glass, the dark reflecting pool catching the light along the front terrace. The scene stays alive throughout: moving lights, drifting dust, a shifting sky. The shot ends resting a beat at eye level on the finished house glowing in golden-hour light, mountains behind. No text or lettering anywhere.

**Segment 3 video prompt (image to video, kling-video-v3_0, start image = segment 2's extracted final frame):**

> One continuous shot, no cuts, beginning on the same grand modern-barn estate at golden hour and easing into a slow steady pull back as golden hour deepens toward blue hour, the granite cliff dimming behind the gable roofline. Warm amber light fills the interior where a couple and their friends sit gathered at a long dinner table seen through the central two-storey glass gable beneath the cascading glass-orb chandelier, rendered as warm silhouettes in a warmly classic interior with rich wood paneling, a gleaming marble floor, elegant traditional furniture, and a grand staircase visible beyond them. As the camera pulls back, a massive tall front door swings closed. The pull back continues to reveal the landscaped front yard: a sculptural stone fountain centerpiece with moving water, two dark elegant unbranded luxury vehicles in the driveway, and small distant figures of children playing on the lawn in the evening light. The camera keeps drawing back down the driveway until a heavy estate gate closes across the frame. The shot ends at rest at blue hour: the closed gate centered in frame with generous sky above and driveway below, the finished home glowing warmly beyond it, everything settled and still except drifting mist and the fountain's water. No text or lettering anywhere.

## 5. The band map

45 seconds of joined footage carries a **2400vh** hero (starting point; the skill's proven density is about 400vh per 6s shot). Sticky full-viewport stage, scroll progress 0 to 1 drives video time through the Blob + lerp + gated-seek standard. Ranges are starting points for the flick test.

Text lives left-aligned in the left third of frame (the film's action reads center-right through most beats); bands 10 and 11 sit centered as the film symmetrizes on the door and gate.

| Band | Range | Footage moment | Copy (verbatim) | Entrance |
|---|---|---|---|---|
| 1 | 0.00-0.06 | Inside the clouds | GILBERTSON FINE HOMES (wordmark, faint, dissolving) | Blur-to-sharp at whisper opacity, one-time load ramp |
| 2 | 0.08-0.13 | Mountains revealed | "Some homes are built for the market." | Drift-down |
| 3 | 0.15-0.20 | Glass roof from above | "This one is built for your name." | Word-by-word rise |
| 4 | 0.22-0.27 | Raw land, trail, stakes | "It starts with land, and a promise." | Scatter, tight spread |
| 5 | 0.29-0.34 | Blueprint line-art | "We build sensational spaces." | Grid snap-align (drafting-table echo) |
| 6 | 0.36-0.42 | Foundation poured | "From concept," | Drift-down |
| 7 | 0.44-0.50 | Night works, pour | "to procurement," | Word-punch on "procurement" |
| 8 | 0.52-0.58 | Framing rises | "to building," | Weave (threads-crossing echo of framing) |
| 9 | 0.60-0.66 | Finished house, golden hour | "to finishes." | Blur-to-sharp |
| 10 | 0.69-0.79 | Amber gathering, door closes | "Then we hand you the keys to the rest of your life." | Word-by-word rise into staged settle |
| 11 | 0.84-1.00 | Gate closes, rest | "Built to be inherited." + CTA "Start the conversation" | Halves parting in reverse (converging as the gate closes), then staged settle: line, subline, CTA |

Bands 5 through 9 are one continuous sentence written across the scroll; their shared left rail and identical baseline make them read as one utterance, and the punctuation carries the continuation.

Band 11's plateau is the longest on the page (the final 16 percent of a 2400vh hero is about 380vh): "Built to be inherited" gets room to land, never clipped.

## 6. The static-hero copy block

For phones, portrait tablets, coarse-pointer landscape, short landscape, and reduced motion (the five gates): the settle frame (closed gate, glowing home) as a composed still with:

- Kicker (mono): `NANAIMO · LADYSMITH · THE GULF ISLANDS`
- Headline: "Built to be inherited."
- Subline: "Custom homes for Vancouver Island and the Gulf Islands, built by hand to carry your family's name."
- CTA: "Start the conversation"

## 7. The below-fold outline

Every section funnels to ONE call to action: the consultation form at `#conversation`. Sheet-number labels in mono give each section its construction-documents identity.

**A-101 · The quiet difference (philosophy).**
Kicker: `A-101 · THE BUILDER`
Headline: "A home your grandchildren will argue over."
Body (verbatim): "Gilbertson Fine Homes is led by a Red Seal carpenter who still swings a hammer on his own sites. We build a small number of homes each year on Vancouver Island and the Gulf Islands, and we build them to be argued over in fifty years, not flipped in five. Clear communication, transparent pricing, and a build you can watch happen. That is the whole trick."

**L-301 · The islands we build on (service area).**
Kicker: `L-301 · SITE PLAN`
Headline: "We build where the ferries go, and where they don't."
Body (verbatim): "Nanaimo. Ladysmith. Central Vancouver Island. And the outer islands most builders won't quote: Saltspring, Gabriola, and remote sites where every board arrives by barge. Island building is its own trade, and it is ours."
Treatment: a hand-drawn SVG coastline of the mid-island and Gulf Islands, contour lines drawing themselves on scroll, amber points marking the named places. No embedded map widget.

**S-201 · The process (echoes the film's four phases).**
Kicker: `S-201 · SEQUENCE OF WORK`
Headline: "Concept. Procurement. Building. Finishes."
Four phases, each one short verbatim block:
1. "Concept. We design around your land and your life, and we price honestly before anyone digs. Allowances are spelled out, not hidden."
2. "Procurement. We source every board, pane, and fixture ourselves, so quality and price never have to be a choice."
3. "Building. Permits handled. Schedule visible. A Red Seal carpenter on your site, not just a signature on your contract."
4. "Finishes. The stair rail your hand will know in the dark. Nice things cost. They don't need to cost twice."
The interactive moment lives here (section 8 below).

**A-401 · Selected work (portfolio).**
Kicker: `A-401 · SELECTED WORK`
Headline: "Homes we'd put our own name on. And did."
Six framed placeholder panels, each carrying a mono label: `[ YOUR PROJECT PHOTO · TITLE · ISLAND ]`. Styled as matted architectural presentation boards so the placeholders look intentional until real photography arrives. No stock imagery anywhere.

**I-501 · Inside the build (interiors and finishing).**
Kicker: `I-501 · INTERIORS`
Headline: "Finished means finished."
Body (verbatim): "Deep energy retrofits, Built Green and Net Zero training, and interiors finished to the last cabinet pull. If you want one contract from raw land to made beds, that is exactly what we do."

**T-601 · Trust (the receipts).**
Kicker: `T-601 · RECORD`
Four stat tiles, placeholders clearly marked, never fabricated:
- `[YEARS] years building on the island` → `[TO FILL: real number]`
- `[N] homes standing` → `[TO FILL: real number]`
- "Red Seal certified" (real, stays)
- "Built Green · Net Zero trained" (real, stays)
Two testimonial slots: `[TO FILL: real client words, with permission]`, styled as letterpress pull quotes.

**FAQ (folded into T-601's lower half).** The real objections, answered in the buyers' own language (verbatim):
- "Will we blow the budget?" → "The horror stories start with vague allowances. Ours are itemized before you sign, and change orders are priced before the work, not after."
- "How do you handle the cheapest bid?" → "We won't win a race to the lowest number, and we won't bill you for what a low bid left out. The cheapest quote is usually the most expensive home."
- "Can you actually build on the outer islands?" → "Yes. Barge schedules, remote crews, island permitting: we plan them from day one, and we've done it before."
- "Who handles the permits?" → "We do. All of them. You'll never stand in a municipal line."

**C-701 · The conversation (the one CTA).**
Kicker: `C-701 · FIRST MEETING`
Headline: "Tell us about your land. Or your idea of it."
Body: "One conversation. No obligation, no pressure, and no junior salesperson. You'll talk to the people who will actually build your home."
Form fields: Name, Email, "Where is (or where should be) your land?", "Tell us what you're imagining." Button: "Start the conversation."
Form handling, decided honestly: JS-only success state for this concept build ("Thank you. We read every one of these ourselves, and we'll reply within two business days."), with a clearly marked TODO to wire the owner's real intake email or a form service before this goes live as the business's actual site. The success message must stay truthful to whatever handling ships.

**Footer.** Wordmark, service areas, and the imagery line per the user's disclosure decision (placeholder until chosen): either "Concept imagery generated with AI; project photography arriving" or nothing if real photos will replace generated stills before launch. Plus: "This is a design concept for Gilbertson Fine Homes" if the site ships anywhere public before the business adopts it.

## 8. The one interactive moment

In S-201, phase 1's card carries it: **press and hold to pour the foundation.** A concrete-pour progress fill rises inside an outlined foundation form while the visitor holds; releasing early lets it ease back down; completing it lights the four phase cards in sequence, amber, left to right. Reduced motion gets the finished state instantly. It enacts the brand's premise: nothing about a Gilbertson home happens fast, and holding the pour is the point.

## 9. The vector layer plan

- **The signature element: the survey line.** One continuous hand-drawn SVG contour line that begins under the hero's settle, draws itself down the entire page along the left rail, ties every sheet-numbered section together, and terminates by closing into the outline of a gate above the footer. It is the property line of the whole page. Boldness budget spent here; everything else stays quiet.
- Sheet-number mono labels with short self-drawing underlines per section.
- The coastline SVG in L-301 with its amber location points.
- Whisper-level mist particles in the fixed background environment layer: a slow 90-second drift of two soft fog gradients behind everything, in the footage's blue-gray, so the page reads as one dusk environment.
- All of it honors reduced motion: lines shown drawn, particles stopped, finished states only.

## 10. The engineering list

The full standard, named so the build cannot half-remember it: streamed Blob fetch with the honest loading ring (45s of 720p footage will clear 8 MB), dt-normalized lerp that rests, gated seeks with the deadlock escape, delta-gated DOM writes, band pacing with the flick test, the four-layer legibility system with the worst-frame audit at 3.5:1, the five static-hero gates identical in CSS and JS and armed live, complete-without-video, `overflow-x: clip` on both roots, reduced motion honored live in both directions, and the quality floor, all per `scrub-pipeline.md`. Mobile decision, made now: the five gates serve the composed static settle frame; no mobile scrub (a 45-second chained film will not fit the under-8MB cover-crop bar).

Performance bar from the brief, adopted: page usable almost instantly, poster first, film streaming behind the ring; page weight excluding video in the tens of KB; measured receipts at deploy.

## 11. The copy gate line

Every viewer-facing line above ships verbatim. The built page must pass the Phase 9 grep gate (zero em dashes; zero hits on leverage, seamless, empower, unlock, robust, actionable, data-driven, solutions) plus the body-copy sweep for AI tells before anyone sees it. Deliberate brand devices in this package are craft and stay: the four-word phase march ("Concept. Procurement. Building. Finishes."), the market/name pair in bands 2 and 3, the staccato "Finished means finished." The sweep hunts only what drifts in uninvited.
