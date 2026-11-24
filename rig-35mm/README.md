# 35 mm rig

Film transport test rig for 35 mm (135) film. A standard cassette supplies the
film, a printed spool takes it up, and after the last frame the film is rewound
into the cassette.

Design: `rig-35mm.sc` (SolidCraft). Renders: `rig-35mm.png`, `top-section.png`
(section at film height), `gear-section.png` (section through the gears).

## How it works

- **Two sprockets, geared together.** One sits on each side of the throat (8
  teeth, one turn = 38 mm of film). A middle gear couples them, so both move
  exactly the same length of film: the supply sprocket pushes film into the
  drum while the take-up sprocket pulls the same amount out. The loop never
  gets tighter or looser.
- **No edge rings.** 35 mm film is stiff enough to press itself outward against
  the drum wall. It runs in a shallow groove (film radius 20 mm): a ledge under
  the bottom edge and a 0.5 mm lip over the top edge keep it at the right
  height. Neither can shade the film, so the whole 35 mm width is exposed,
  perforations included.
- **Driving:** the take-up knob turns the take-up spool. The film turns the
  take-up sprocket, and the gears make the supply sprocket push the same amount.
- **Loading wheel:** the small wheel under the floor turns the middle gear. When
  loading, it makes the supply sprocket push the leader round the drum on its
  own.
- **Rewind:** the supply knob ends in a fork that grips the cassette spool's
  cross bar. A felt washer under it acts as a light brake while advancing; turn
  it backwards to rewind. The take-up spool freewheels.
- **Emulsion faces the pinhole:** the film wraps each sprocket on its far side
  (S-bend), so the emulsion side ends up facing inward.
- About 126 mm of film per 360° frame, so roughly 10–11 frames from a 36-exposure roll.

## Printed parts

| Part | File | Qty | Print orientation |
|---|---|---|---|
| Body | `stl/Body.stl` | 1 | floor on the bed |
| Top cap | `stl/TopCap.stl` | 1 | top face on the bed |
| Sprocket | `stl/Sprocket_x2.stl` | 2 | gear end on the bed |
| Middle gear | `stl/IdlerGear.stl` | 1 | gear face on the bed, stem up |
| Loading wheel | `stl/LoadWheel.stl` | 1 | closed face on the bed |
| Rewind shaft (fork) | `stl/RewindShaft.stl` | 1 | fork up |
| Take-up shaft | `stl/TakeupShaft.stl` | 1 | stem down |
| Take-up spool | `stl/TakeupSpool.stl` | 1 | flange on the bed |
| Take-up spool top flange | `stl/TakeupSpoolFlange.stl` | 1 | flat, press onto the spool core |
| Pinhole clamp | `stl/PinholeClamp.stl` | 1 | flat |
| Lens cap | `stl/LensCap.stl` | 1 | top face on the bed |
| Knob | `../transport-rig/stl/Knob_x2.stl` | 2 | as before |
| Thumb knob | `../cartridge-rig/stl/ThumbKnob_x2.stl` | 2 | pocket up |
| GoPro mount plate | `../transport-rig/stl/MountPlate.stl` | 1 | prongs up |

No supports needed. All parts in PLA.

## Hardware

| Item | Qty | Where |
|---|---|---|
| 623 bearing | 2 | top of each sprocket |
| M3 × 10 cap screw + washer | 2 | sprocket axles, from below through the floor |
| M3 × 10 cap screw + washer | 2 | through the cap into the top sprocket bearings |
| M3 × 12 cap screw | 2 | thumbscrews, cap into body |
| M3 × 6 cap screw + washer | 5 | mount plate (3), pinhole clamp (2) |
| Magnet 5 × 1 mm | 8 | 2 per pocket: cap top (2), lens cap (2) |
| Felt washer, ~20 mm OD, 6 mm hole | 1 | rewind brake, between rewind knob and floor |
| Can aluminium foil, max. 12 mm wide | 1 | pinhole |
| Cord, ~2.5 mm | 1 | lens cap to the GoPro mount |
| 135 cassette | 1 | supply |

Washers: 9 in total. All M3 screws self-tap into 2.5 mm holes.

## Assembly notes

- Press a 623 bearing into the top of each sprocket.
- **Gear timing:** before fixing the cap, set the two sprockets so their teeth
  sit in the same perforation phase relative to the film. The gears allow
  steps of 1/12 turn (3.2 mm of film); the groove has about ±2 mm of radial
  play to take up what is left.
- Press the top flange onto the take-up spool core.
- The cassette goes in spool end down, mouth pointing toward the supply
  sprocket. The mouth slot in the body stops it from turning.

## Loading

1. Cap off. Drop the cassette in, mouth into its slot.
2. Pull out a little leader and hook its perforations onto the supply sprocket.
3. Turn the loading wheel. The sprocket pushes the film round the groove until
   the leader comes out at the take-up sprocket.
4. Tuck the leader into the slit of the take-up spool and turn the take-up knob
   a little.
5. Cap on, tighten the thumbscrews. In daylight the first frame is fogged.

## Unverified assumptions

- Cassette measurements: Ø25 mm, 43.5 mm shell, 4 mm spool end (Ø11/9.4 mm,
  2.5 mm cross bar), mouth about 8 mm long and 3 mm thick.
- Perforation rows assumed 3.6 mm from each film edge, pitch 4.75 mm.
- The throat layout (mouth slot, film lanes, body outline) is drawn for these
  numbers and does not follow parameter changes; heights and the film groove
  do.
