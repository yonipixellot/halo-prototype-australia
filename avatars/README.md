# Player avatar photos

Drop player headshot files here. The prototype's `IdentityCircle` and roster renderers pick them up automatically.

## Filename convention

`<lastname>.png` when the lastname is unique across all rosters. For lastname collisions (two Parks, two Reyeses), use `<firstinitial>-<lastname>.png`.

Currently in place:
```
weiss.png   — Tal Weiss (#7, SG, Sesh Rigs)
kim.png     — Sarah Kim (#12, PG, Sesh Rigs)
torres.png  — Dylan Torres (#24, SF, Sesh Rigs)
```

## All wired slugs

Home (Sesh Rigs):
| Player | File |
|---|---|
| Tal Weiss | `weiss.png` ✓ |
| Sarah Kim | `kim.png` ✓ |
| Dylan Torres | `torres.png` ✓ |
| Jay Park | `j-park.png` |
| Marcus Lee | `lee.png` |
| Eli Cohen | `cohen.png` |
| Owen Brooks | `brooks.png` |
| Noah Patel | `patel.png` |
| Ryder Sun | `sun.png` |
| Alex Tan | `tan.png` |
| Marco Reyes | `marco-reyes.png` |
| Caleb Wong | `wong.png` |

Away (Medium Fundamentals):
| Player | File |
|---|---|
| C. Bell | `bell.png` |
| M. Reyes | `m-reyes.png` |
| D. Park | `d-park.png` |
| J. Howard | `howard.png` |
| A. Singh | `singh.png` |
| T. Olsen | `olsen.png` |
| R. Vance | `vance.png` |
| K. Mendez | `mendez.png` |
| B. Foster | `foster.png` |
| L. Diaz | `diaz.png` |
| S. Ito | `ito.png` |
| P. Khoury | `khoury.png` |

Followed (Home tab circles):
| Player | File |
|---|---|
| Elena Ruiz (Hustle HQ) | `ruiz.png` |

## Spec

- **Square**, recommended 256×256 or 512×512
- Centered head + shoulders, comfortable padding
- Any face-shape — the prototype crops to a circle
- White or any background works — the rendered circle has dark glass behind it

## Fallback behaviour

If a player's file is missing, the existing initials/silhouette/jersey-number fallback still renders behind a `<img onError>` handler — the broken-image icon never shows. Roll out one photo at a time.
