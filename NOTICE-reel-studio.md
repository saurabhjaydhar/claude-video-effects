# claude-video-effects inside Reel Studio

Source for updates: https://github.com/saurabhjaydhar/claude-video-effects (Saurabh's fork, 2026-11-01).
Original upstream: https://github.com/Vibha-Ramprakash/claude-video-effects — "45 starter video effects" by Vibha Ramprakash
(@vibha.in.progress), MIT licence (LICENSE in this folder). Fonts: SIL OFL / Apache-2.0 (fonts/*.txt). Models: YuNet (MIT),
MediaPipe Selfie Segmenter (Apache-2.0) — models/NOTICE.md.

Vendored 2026-10-30 from the main branch. Changes for Reel Studio:
- scripts/fx.py: the optional `fx_private.py` exec loader is disabled (no code outside this folder is ever executed).
- setup.sh / words.py / assets/ not included (Reel Studio has its own environment check and word timings).
- Called only through `tools/vfx.py`, which writes the plan, applies the channel's colours and adds SFX.
