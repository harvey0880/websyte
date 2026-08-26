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

## 4. The film: one master take, eight hard cuts

One 15-second generation on **kling-video-v3_0** (multi-shot ON, prompt written as an explicit hard-cut shot list, no audio, 1080p, 16:9), driven by the approved start frame. Hard cuts and timelapse replace continuous camera travel: each shot is a held composition doing exactly one job, and the scrub gives each its own band, so no screen time is spent flying over empty ground. One take means no chaining, no frame extraction between segments, no seams.

Generation path, decided with the owner: generated from this session through the Kling connector; the owner reviews and downloads each output from the returned no-watermark URL (the session's own network policy blocks the CDN, so the owner's download is the archival copy). Standing rules: original files only, and a watermark check on the first output.

The generator never sees any text. The faint logo reveal in the clouds and every caption are HTML/SVG overlays on the page, crisp and brand-accurate, never baked into footage.

Law-driven adjustments to the brief, said out loud:
- All people are small, distant, fast-moving crew figures (Law 5: anatomy at detail breaks; silhouettes at distance render beautifully). The dinner-party and children beats from the earlier plan are cut by the owner's revised brief.
- The two vehicles are dark, sculptural, and unbranded (no-logos guard; real marques are trademarks).
- The logo-in-clouds beat is a page overlay timed to band 1, not generated imagery (Law 12).
- Contingency, decided now: if the driveway-and-cars beat fails inspection twice, the close resolves as gate and mist alone. The story survives; the risk does not have to.

### The world, locked (art direction from the owner's reference film)

Every prompt below describes the same place and the same house, so the film reads as one estate from clouds to gate:

- **The valley:** a British Columbia mountain valley beneath a sheer granite cliff face with vertical rock striations, dense dark fir forest climbing its base, a flat meadow floor in muted sage and straw, low mist lying in ribbons through the treetops. Documentary drone photography, not fantasy landscape.
- **The house:** a grand modern-barn estate: a long row of steep-pitched gables stepping across the clearing, the central gable a full two-storey wall of black-steel-framed glass with a cascading glass-orb chandelier visible inside, flanking wings in dark stained timber, heavy stone chimneys, charcoal standing-seam roofs, a broad stone terrace and a dark still reflecting pool across the front.
- **The grade:** cool Pacific Northwest light throughout: silver, diffuse, desaturated greens and slate blues, mist always alive in frame. Warmth enters only as interior amber through glass and the golden-hour/blue-hour close. Never oversaturated, never golden-fantasy.

### The cut (owner's second-by-second brief, mapped to footage time)

| Shot | Footage window | Beat |
|---|---|---|
| 1 | 0.0-2.0s | Straight down through thinning cloud, the estate's charcoal gable roofs dead-centre far below, growing fast as the camera drops |
| 2 | 2.0-4.0s | Directly over the central glass gable roof: through the glass, a gorgeous warm interior, chandelier, staircase, marble floor |
| 3 | 4.0-5.5s | HARD CUT to eye level across the reflecting pool, the finished estate front-on beneath the cliff |
| 4 | 5.5-7.5s | The house turns to glowing white architectural line-art; day snaps to night in timelapse and the outline fades, leaving bare excavated earth and an open foundation |
| 5 | 7.5-9.5s | Night works timelapse: excavators and a concrete pump over the foundation, work lights, small crew figures in fast motion |
| 6 | 9.5-11.5s | Dawn timelapse: the timber frame stands, steep gable trusses stepping across the site, framers moving fast along it |
| 7 | 11.5-13.0s | The frame skins over into the finished house; through the glass, rich woodwork and marble floors catching warm light |
| 8 | 13.0-15.0s | Eye-level pull back: paved driveway with two dark luxury cars in the foreground, a heavy estate gate closes across frame, mist rolls in, house glowing beyond; rest on the closed gate |

Final frame (the page's settle, the poster, the static hero): the closed gate in mist, house warm behind it. Header-safe by design; verified with the header mocked over it before approval.

### The generation prompts (written now, submitted only after the gates)

**Start frame (image, 16:9, generated on the connector's strongest photoreal model — Nano Banana Pro / gemini-3-pro-image at high resolution — then animated by Kling video; generate multiple candidates, inspect, and show only the winner):**

> High-altitude aerial photograph looking down through a thin breaking layer of morning cloud over a British Columbia mountain valley. Through the widening break on the left of frame, far below: a sheer granite cliff face with vertical rock striations rising out of dense dark-green fir forest, a flat meadow valley floor in muted sage and straw tones, and ribbons of low mist lying through the treetops. The right side of frame stays a soft unbroken field of cool white-grey cloud. Overcast Pacific Northwest light: silver, diffuse, slightly cold, one faint warm touch of early sun on the cliff top. Shot from a drone on a full-frame cinema camera, deep depth of field, razor-sharp detail in rock striations and individual fir crowns, subtle natural film grain, graded like a moody architectural documentary: desaturated greens, slate blues, no oversaturation, no fantasy glow. 16:9. No text, no logos, no lettering anywhere.

**Master film prompt (image to video, kling-video-v3_0, 15s, multi-shot on, no audio, 1080p, start image = approved start frame):**

> A cinematic architectural film cut as a rapid sequence of distinct shots with hard cuts and timelapse, not one continuous camera move. Shot 1: looking straight down through a thinning morning cloud layer, a grand modern-barn estate directly below, a long row of steep charcoal gable roofs, stone chimneys and a dark reflecting pool, growing closer as the camera drops fast through the mist. Shot 2: directly above the central glass gable roof, looking through the glass into a gorgeous warm interior: a cascading glass-orb chandelier, a grand staircase, gleaming marble floor, amber light. Hard cut, Shot 3: eye level across the dark reflecting pool, the finished estate front-on, dark timber and black-steel glass beneath a sheer granite cliff, cool silver light. Shot 4: the whole house turns into glowing white architectural blueprint line-art; day snaps to night in fast timelapse and the line-art fades away, leaving bare excavated earth and an open foundation on the same site. Shot 5: night construction timelapse, excavators and a concrete pump truck working fast over the foundation under blazing work lights, small crew figures in hard hats moving in fast motion, steam and dust drifting through the beams. Shot 6: dawn timelapse, a timber frame rises, steep gable roof trusses stepping across the site, framers moving fast along the structure. Shot 7: the timber skeleton skins over into the finished estate, and through the tall glass rich warm woodwork and marble floors catch golden light. Shot 8: eye-level pull back at blue hour, a paved stone driveway with two dark elegant unbranded luxury cars in the foreground, a heavy iron estate gate swings closed across the frame, low mist rolls in, the house glowing warm beyond the gate; the film ends at rest on the closed gate in the mist. The same house, the same valley, the same granite cliff in every shot. Cool desaturated documentary grade throughout, warmth only from interior light and the blue-hour close. No text or lettering anywhere.

## 5. The band map

15 seconds of hard-cut footage carries a **1100vh** hero (starting point; the skill's proven density is about 400vh per 6s shot). Sticky full-viewport stage, scroll progress 0 to 1 drives video time through the Blob + lerp + gated-seek standard. Ranges are starting points for the flick test; the cut boundaries in the footage are the band boundaries, so every scroll lands inside one held composition.

Text lives left-aligned in the left third of frame; band 8 sits centered as the film symmetrizes on the gate.

| Band | Range | Footage moment | Copy (verbatim) | Entrance |
|---|---|---|---|---|
| 1 | 0.00-0.10 | Falling through cloud to the roofs | GILBERTSON FINE HOMES (wordmark, faint, dissolving) | Blur-to-sharp at whisper opacity, one-time load ramp |
| 2 | 0.13-0.24 | The interior through the glass roof | "Some homes are built for the market." | Drift-down |
| 3 | 0.27-0.35 | Eye level across the pool | "This one is built for your name." | Word-by-word rise |
| 4 | 0.37-0.48 | Line-art, night falls, site goes bare | "We build sensational spaces." | Grid snap-align (drafting-table echo) |
| 5 | 0.50-0.61 | Night works over the foundation | "From concept, to procurement," | Word-punch on "procurement" |
| 6 | 0.63-0.74 | The frame rises at dawn | "to building," | Weave (threads-crossing echo of framing) |
| 7 | 0.76-0.84 | Finished: woodwork and marble | "to finishes." | Blur-to-sharp |
| 8 | 0.87-1.00 | Cars, the gate closes, mist | "We build to inherit." + CTA "Start the conversation" | Halves converging as the gate closes, then staged settle: line, subline, CTA |

Bands 5 through 7 read as one continued sentence across the scroll; the shared left rail and identical baseline carry it. Band 8's plateau is the longest on the page (the final 13 percent of an 1100vh hero): "We build to inherit." gets room to land, never clipped.

## 6. The static-hero copy block

For phones, portrait tablets, coarse-pointer landscape, short landscape, and reduced motion (the five gates): the settle frame (closed gate, glowing home) as a composed still with:

- Kicker (mono): `NANAIMO · LADYSMITH · THE GULF ISLANDS`
- Headline: "We build to inherit."
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

The full standard, named so the build cannot half-remember it: streamed Blob fetch with the honest loading ring (a 15-second film encoded at 720p lands well under 8 MB), dt-normalized lerp that rests, gated seeks with the deadlock escape, delta-gated DOM writes, band pacing with the flick test, the four-layer legibility system with the worst-frame audit at 3.5:1, the five static-hero gates identical in CSS and JS and armed live, complete-without-video, `overflow-x: clip` on both roots, reduced motion honored live in both directions, and the quality floor, all per `scrub-pipeline.md`. Mobile decision, made now: the five gates serve the composed static settle frame; mobile scrub revisited at build now that the film is 15 seconds; the under-8MB cover-crop bar decides it.

Performance bar from the brief, adopted: page usable almost instantly, poster first, film streaming behind the ring; page weight excluding video in the tens of KB; measured receipts at deploy.

## 11. The copy gate line

Every viewer-facing line above ships verbatim. The built page must pass the Phase 9 grep gate (zero em dashes; zero hits on leverage, seamless, empower, unlock, robust, actionable, data-driven, solutions) plus the body-copy sweep for AI tells before anyone sees it. Deliberate brand devices in this package are craft and stay: the four-word phase march ("Concept. Procurement. Building. Finishes."), the market/name pair in bands 2 and 3, the staccato "Finished means finished.", the owner's gate line "We build to inherit." The sweep hunts only what drifts in uninvited.
