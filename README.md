# Tactical Interactive Dashboard

[![Website](https://img.shields.io/badge/Website-GitHub%20Pages-222?logo=github&logoColor=white)](https://lucamonticone.github.io/tactical-interactive-dashboard/)
![Built with](https://img.shields.io/badge/Built%20with-HTML%20%2B%20JavaScript-3b6b70)
[![License](https://img.shields.io/badge/License-Noncommercial-79445b)](LICENSE.md)

I started this project after watching Torino–Como from the stands. From above, it was easier to see how Como kept moving the ball, how Torino's defensive block shifted, and how a player like Nico Paz tried to find space behind the midfield.

I wanted to explore those situations rather than simply describe them. This repository collects interactive tactical boards: pause the play, change a decision, and see which passing lanes become available.

## Case studies

### 01 — Torino vs Como | 2026/27

[**Open the interactive tactical board**](https://lucamonticone.github.io/tactical-interactive-dashboard/Torino-Como26-27/tactical_view.html) · [Website](https://lucamonticone.github.io/tactical-interactive-dashboard/)

A first-half tactical study focused on:

- Como's 4-2-3-1 build-up and Perrone's movement from midfield
- Torino's 5-3-2 defensive block
- Pressing angles and coordinated defensive shifts
- Nico Paz receiving between the lines
- Milla's movement and Bragança's defensive choices
- The passing options that appear after the first pass

The board lets you explore different responses to the same situation, rather than treating one decision as automatically right or wrong.

## Method

The match context and starting formations are based on publicly available information. The board uses positional geometry and interactive animations to illustrate alternative tactical decisions.

**These are tactical simulations, not player-tracking reconstructions.** A visible passing lane does not guarantee a successful pass: timing, body orientation, ball speed and defensive reactions matter. Simulated decisions are not claims that an individual player made those mistakes during the actual match.

Match reference: [Lega Serie A highlights](https://www.legaseriea.it/videos/serie-a-2026-2027-torino-como).

## Project structure

```text
tactical-interactive-dashboard/
├── README.md
├── LICENSE.md
├── index.html
├── assets/
└── Torino-Como26-27/
    └── tactical_view.html
```

To run locally, open `index.html` in a browser, or start a static server from the repository root:

```powershell
py -m http.server 8000
```

Then open `http://localhost:8000/`.

I'll add more match situations to this repository as I work on them.

## License

Code is available under the [PolyForm Noncommercial License 1.0.0](LICENSE.md). Non-commercial uses are permitted under its terms; commercial use requires separate authorization. The license is **not an OSI-approved open-source license**. Third-party trademarks, footage and other material remain the property of their respective owners.

Created by **Luca Monticone**. Independent project, not affiliated with Torino FC, Como 1907 or Lega Serie A.
