# Surveillance Capitalism theme design

## Identity

The desktop is the view from inside the system. Somewhere a machine is watching an
ordinary person, classifying them, predicting them and selling the prediction. The
theme never shows the watcher. It shows only what the watcher draws: a thin box
around a subject, a small label, a red light far away in the dark.

Two sources meet here. *Person of Interest* gives the visual grammar: classification
boxes, camera timestamps, the steel-blue night of its title sequence, and the cold
Samaritan interface. Shoshana Zuboff's *The Age of Surveillance Capitalism* gives
the subject matter: behavioral surplus, prediction products, the loss of sanctuary
and the right to an unpredicted future.

**Should feel:** quiet, cold, patient, watched, nocturnal, precise, slightly sad.

**Should not feel:** hacker-green, cyberpunk neon, gamer RGB, Matrix rain, Guy Fawkes
or any other mask, cosy, warm amber, glossy sci-fi dashboard, rainy-street AI art.

## Visual thesis

- **Ground:** the night sky of the show's title card, a steel-blue slate where
  every detail of the city has been lost. All surfaces share this hue family.
- **Text:** the ice-white lettering of the same title card, a little softened so
  that long reading does not glare (about 11:1 on the background).
- **The box:** the AI's classification frame. It is the only lead accent: ice white,
  thin, solid. It is never decorated with a gradient.
- **Four words:** the system only speaks in its classifications. Every colour slot
  is red threat, yellow admin, blue government or white irrelevant, or a shade of
  one of them. A successful command is not green: it is irrelevant. This deliberate
  poverty is the theme's strangeness; there is no rainbow to hide in.

## Palette source and role mapping

| Role | Hex | Source |
|---|---|---|
| background | `#131e28` | title-card sky, L .23 h246 |
| darker / dark | `#050c13` / `#0b151d` | title-card shadow band |
| lighter / selection | `#1e2a35` / `#2b3d4c` | title-card mid sky |
| muted | `#626d78` | title-card haze |
| foreground | `#c8d3da` | title-card lettering, softened |
| accent / active border | `#ccdae3` | title-card lettering: the AI's box |
| red | `#e24945` | threat box and the recording light |
| yellow | `#d8c740` | admin box |
| blue | `#5492ec` | government / operational box |
| green | `#b2c0c9` | irrelevant: success is just another white box |
| cyan | `#92bbea` | pale government blue |
| magenta | `#a83636` | dark threat red |
| orange | `#c39800` | deep admin yellow |
| brown | `#7d6627` | dimmed admin yellow |

Each signal sits at the chroma it reaches in the source images, not above it.
Colour-blind separation still holds: the closest pair (green/cyan) is about dE 6. The
ground is deliberately tinted rather than neutral: the steel blue *is* the identity,
and the signals are rare enough to stay legible against it. The Base24 palette in
`surveillance-capitalism-base24.yaml` uses the same values.

## Surfaces

- **Active window:** a solid ice-white border, the AI's box around the one subject it
  is currently looking at. Inactive windows fade almost into the ground: irrelevant.
- **Bar:** the same ground as the windows, so the screen reads as one dark field.
- **Menu and launcher:** an opaque dark card with a quiet steel frame. The selected
  row is drawn as a full classification box: an ice-white frame with no fill.
- **Notifications:** the countdown is the recording light, the only red that appears
  without an error.
- **Errors:** red, and only red, everywhere (polkit, lock screen, terminal).

## Wallpapers

Twelve drawn originals. Most come in pairs: a title card, then the same sentence
taken literally, with one subject in the centre.

1. *Surveillance Capitalism* — the title card.
2. *Observation: continuous.*
3. The subject made only of the data collected about him.
4. *You are the raw material.* → 5. his body breaking up into extracted data.
6. *You are being predicted.* → 7. a woman's next three steps, leading to a sponsored shop.
8. *Nothing to hide.* → 9. a see-through man, everything tracked marked where it really is.
10. *Sanctuary: not found.* → 11. someone at home, every device in the room reporting out.
12. *Status: irrelevant — for now.*

Rules: one subject or one line of text per image, always centred or on the card's
left third, faces never shown, huge negative space for windows. The subjects are
different ordinary people: the system watches everyone, not one man. Everything is drawn in the palette at full resolution; nothing is a
photograph. See `backgrounds/SOURCES.md`.

## Companion files

`gtk.css`, `zen.css`, `zed.json`, `cava_theme` and `vencord.theme.css` carry the same
roles: ice white for focus and accent, red for errors, yellow for warnings. Cava
rises from steel blue to ice white and touches red only at its peaks. `icons.theme`
selects Yaru blue. `btop.theme` follows cava: graphs rise from steel to ice white and turn red only at their peaks. In Zed, code reads mostly in ice and white, with deep-yellow strings and pale blue constants; bright yellow is kept for warnings.

## Guardrails

- Keep red rare. If red appears on every screen, the threat stops meaning anything.
- Do not add a second lead accent; yellow and blue are words, not decoration.
- Do not give the AI a face, a mask, or an eye. It is only ever the box.
- New wallpapers follow the story rules above and go through the same palette map.
