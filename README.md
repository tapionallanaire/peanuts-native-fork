# Xenoblade on Android: test evidence (2026-11-25)

Device: AYN Thor (Snapdragon 8 Gen 2, Adreno 740), Turnip v27.0.0-R1, 117.84 Hz panel (8.485 ms refresh).
Screenshots are from the device (`screencap`), with the in-game performance overlay on.
`*-surfaceflinger-presents.tsv` are the game surface's present times from `dumpsys SurfaceFlinger --latency`.
Thirty fps means four refreshes per frame.

| Game | Files | What it shows |
|---|---|---|
| Xenoblade Chronicles 2 2.1.0 (`0100E95004038000`) | `xc2-1..4` | Title → King Crustip targeted → Rex fighting (HP 280 → 238) → event after the win. Profile unchanged. |
| | `xc2-surfaceflinger-presents.tsv` | 2 min of the fight: 30.09 fps, no frame over 42.4 ms. |
| Xenoblade Chronicles 3 2.2.1 EU (`010074F013262000`) | `xc3-1..4` | Title → first battle tutorial → first battle → party in Everblight Plain after the win (phone set to en-US). |
| | `xc3-surfaceflinger-presents.tsv` | 63 s of the battle after first-run pipelines: 30.10 fps, max 50.9 ms. |
| Xenoblade Chronicles: Definitive Edition 1.1.2 (`0100FF500E34A000`) | `xcde-roads-before` / `xcde-roads-after` | Colony 9 road with the uint view but UBWC on (blocks) / with the view made uncompressed. |
| | `xcde-colony9-*` | Commercial District at day, evening and night. |
| | `xcde-surfaceflinger-presents.tsv` | 5 min of Colony 9: 9,026 of 9,026 frames at exactly four refreshes. |
