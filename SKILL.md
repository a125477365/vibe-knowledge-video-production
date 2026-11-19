# Vibe Knowledge Video Production

## Learn the method before you build

- Verify every named tutorial or reference source before you render anything longer than a trial and list what you took from each source.

- Build only a short trial of about 10 seconds first when the method is new and show it to the user before you render the full video and mark any early render as a draft.

- Build a word level timeline from the finished narration and derive every subtitle, graphic, arc, circle and sound cue from those word timestamps instead of hand typed seconds.

- Write a shotbook and one theme object before you build and list unfinished or uncollected footage so a shot with no real footage must justify itself in writing.

- Render one complete sample shot with audio and build the rest only after the user confirms that sample and check the licence of any community method before commercial use.

## Approve the script and storyboard first

- Draft the narration and the map storyboard and send them for user approval before you render the full video.

- Cover a systematic topic per video, such as mechanics, and cover all of its knowledge; keep each video around 5 minutes. When one topic holds too much for one video, split it into several episodes, but each episode must be complete on its own: never split one piece of content across two episodes.

- Keep narration in Chinese when the user asked for Chinese narration and keep one voice through the whole video unless the user approved a change and set length by story completeness.

- Keep narration to verifiable time, place, parties, movements and outcomes and leave out political evaluation.

- Give each shot one idea and one concrete visual metaphor and keep at most three subject groups on screen and rotate compositions so consecutive shots do not repeat the same framing.

## Check the map across the whole film

- Clip every front line and arrow to the landmass it describes and keep fronts and arrows out of neighbouring countries and out of the sea.

- Check border lines against a reference for every segment and do not draw a straight line where the real line bends and check that the timeline moves forward through the whole film.

- Check for omitted campaigns or turning points and ask the user whether to add them and zoom out far enough that the whole theatre stays visible.

- When the user points out one map error, self check every analogous segment across the whole film to the same standard before you report the fix.

## Measure the audio instead of claiming to hear it

- Never claim you heard the audio when you only checked files or waveforms and do not treat pitch, waveform or recognition as proof of correct tone.

- Before full synthesis, list every polyphonic or tone critical word and synthesize each one alone and send each isolated sample to the user for ear approval.

- Do not use a spelling trick inside a word to fix a tone and keep the approved voice and tone sample as the reference for the full narration.

- Write every number and decimal in the narration out in Chinese characters (for example 零点五一秒 and 三十二倍, not 0.51 秒 or 32 倍) — the TTS misreads digits and decimals (user 2026-11-19: 0.51 was read as 零五十一). On-screen text stays as digits for readability; only the TTS input uses Chinese characters.

- Synthesize narration in as few calls as you can while keeping each call reliable and keep one voice and one speed and add short crossfades between segments.

- Measure silence and flag any gap longer than 1.2 seconds and check that no segment is truncated and anchor every sound effect to its naming word and keep music under the voice at minus 14 LUFS.

## Check text and publish only after approval

- Put no black background behind on screen text and use no punctuation in subtitles unless the user asked for it and keep labels inset from the frame edge by at least 140 pixels.

- Send the finished video for user review and publish only after the user approves it and report only what you verified by measurement and what remains unverified.

- Sample two frames 0.8 seconds apart in each shot and fix any shot with no pixel change. Do not add a camera push or pull to every shot — the slow push was only for the solar system video (user 2026-11-19); a static camera is the default and movement comes from the animated elements in the frame.

- Give every shot a carrying image from its opening to its first cue and move any cue that would land inside the last 0.7 seconds of a shot.

- Show each graphic element on its naming word 0.1 to 0.2 seconds early and keep it fully invisible before that word and ease entrances with a spring and stagger them by 3 to 6 frames and make exits faster than entrances.

- Use real footage or a real photo for every real object and use code only for exact annotation such as subtitle, magnifier ring, leader line, chalk arc, map circle, counter and title card.

- Score each chapter on the explainer video quality rubric and do not ship any chapter with a score below 2 out of 5 in any dimension and build a contact sheet from one frame near the end of each scene and look at it beside the reference.

- Send frame by frame quality control to a fresh context reviewer who did not build the film and fix every top priority defect before delivery and do not describe your own review process as part of the delivery.

- After any visual scheme change, recheck every narration line against the rendered frame at its timestamp and do not pass quality control by checking the script against the script or the source document alone.

- Check that every named object, place and reference in a narration line is visible in the frame at its timestamp and that every unnamed pronoun has a named referent visible on screen at that moment.

## Where the work runs

- Execution location (user 2026-11-18): non-GPU work goes local first — cutting, editing, rendering and libx264 encoding run on the local VM by default; use the Windows server only when local resources are not enough. GPU work still goes to the server. The local VM has 1.5 CPU / 6GB memory, so a large render may still need the server, but the default for CPU-only work is local. This replaces the earlier "prefer the server for all video work" rule.
- GPU vs CPU split (user 2026-11-19, replaces the 2026-11-17 "GPU only for lip sync and face restoration" rule): use the GPU wherever a task can use it. GPU is the Windows server's RTX 3070 Laptop 8GB (driver 546.01, CUDA 12.3, verified 2026-11-19). GPU: CosyVoice narration (cosyvoice env was torch 2.3.1+cpu — CPU synthesis ran at ~18x real time, about 1 hour for 5 minutes of narration; switched to GPU 2026-11-19: torch 2.5.1+cu121, RTF ~2.25, ~8x faster than CPU, whole 23-chunk batch ~9 minutes; note the Tsinghua PyTorch mirror silently serves a CPU build — install GPU torch from the official index with an explicit torch==2.5.1+cu121 and verify torch.cuda.is_available()), ffmpeg encoding (NVENC h264_nvenc, verified available on the server ffmpeg 2026-11-19 — measured 2026-11-19: 10 s 1080p re-encode NVENC 0.75 s vs libx264 1.79 s, ~2.4x faster; use it for re-encodes such as the preview; note CPU libx264 still gives better quality per bit, so use NVENC for speed, libx264 when quality matters most), faster-whisper transcription (server base env, faster-whisper 1.2.1 + ctranslate2 4.9.0, device="cuda", float16 — measured 2026-11-19: 60 s clip in ~4.6 s, ~13x real-time, ~6x faster than CPU int8 ~27 s; first run in a fresh process pays ~50 s CUDA init; needs the pip nvidia libs on PATH plus KMP_DUPLICATE_LIB_OK=TRUE, and feed a numpy array — file loading is broken with PyAV 19), XTTS (torch 2.5.1+cu121, CUDA True, verified 2026-11-19), LatentSync lip sync and GFPGAN/CodeFormer face restoration where used. GPU jobs queue one at a time; confirm with the user first when someone else is using the GPU. CPU, no GPU path: PIL frame drawing (blackboard chalk style — PIL has no GPU path; moving it to the GPU would mean replacing the whole renderer, not flipping a switch), ffmpeg audio work (loudnorm, mixing, sidechain ducking), and stream-copy assembly (just moving bytes, nothing to accelerate). Those stay CPU and, per the 2026-11-18 local-first rule, run on the local VM first. Cloud, not local GPU: image/video generation (Muse's models in the cloud). The 2026-11-18 CPU-only constraint recorded in the relativity shotbook is superseded by this rule.
- Model work: image and video generation run in the cloud (Muse's models); CosyVoice, XTTS, LatentSync, Wav2Lip and faster-whisper run on the Windows server, where they are installed — the earlier "narration synthesis always stays local" rule is superseded.
- If server work is needed (GPU work, or CPU work that local resources cannot handle) and the server connection fails, report it instead of silently falling back to local.

## Available connectors

- Use muse.connector_search to find other connectors and muse.skill_search to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with Custom Connectors and MCPs, or build a custom connector.

## Alternatives for better results

- Ask the user to confirm whether omitted campaigns belong in this video or in a follow up before you render the full version.

- Reuse an approved voice, map style and text style across videos in a series and change only the story, the dates and the fronts. Series narration voice: already-published videos keep their own voice (MAI_01 for Korean War, vd3_vd2_brittle_fan for water, MAI_03 speed 95 for the relativity twin-paradox video). For future videos (user decided 2026-11-19): the cloned 小事儿 voice (CosyVoice zero-shot from the Redis video reference, approved by the user's ear 2026-11-19) — one voice through the whole series. The earlier MAI_03 series-voice decision (2026-11-10) is superseded for future videos.

## Community research — 2026-11-15 (Sunday prep, week 1)

Sources checked this week, with licences verified on the repo pages themselves:

| Source | Licence | What it is | Usable for us? |
|---|---|---|---|
| Win-Hao/knowledge-video (Winhao学AI, the tutorial author behind this series) | MIT | 6-step skill: sourced research article → scene copy ≤20 chars/screen, first screen is the question → PD/CC0 images first or layered prompts → 3 looks as stills, beat-synced storyboard → review → render opening ~10 s first | Yes — method and tools. Hard rules: every fact sourced, every asset licensed, no AI-drawn faces of real people, deterministic frames. Publish checklist: sources + credits in the description, AI-generated label on. |
| bobobo2026/explainer-video | MIT | Word-level `timeline.json` spine; 13 reusable scenes hook→cta; 9-dimension rubric, any dimension <2/5 does not ship; −14 LUFS; SFX anchored to "word k of sentence i" | Yes — method. Render cost ≈3.7 s wall per 1 s of video. Keep content inside platform safe areas (right button column, bottom caption zone). |
| wchhywizd/vibe-knowledge-interactive | MIT (code) / CC BY 4.0 (docs) | Canvas 2D + Playwright + ffmpeg; 100 real viral samples with play/like data; interactive counter-intuitive opening | Yes — method. Its BGM file is NOT licensed (someone else's upload) — never use it; replace any music before commercial use. Its samples are Bilibili, not Douyin — do not cross-compare absolute play counts. |
| Vincentwei1021/video-talkcraft (2,331★) and anything2explainer (3,319★) | PolyForm Noncommercial 1.0.0 — commercial use needs the author's prior authorisation | Word-level sync (median 20–40 ms), 108 motion recipe cards, 7-layer anti-slideshow camera, segment-parallel rendering, contact-sheet QA | Ideas only — do NOT copy their code or templates into a commercial video. Videos made with them belong to the maker, but the tools themselves need authorisation for commercial use. |
| ENCHIGO/explainer-video, TechNomadCode remotion-video, haidrrrry/claude-remotion-skill | MIT / open source | JSON storyboard batch rendering, Remotion skill packs | Yes, verify licence per repo before reuse. |
| SpeedPainterOrg/explainer-video | — | Sends content to a cloud service, installer runs code straight from GitHub, requires Google sign-in | Not adopted — do not install. |

- Remotion itself: free for individuals, non-profits and companies with up to 3 employees; a company licence is needed beyond that. Remotion 5.0 changes the terms slightly — re-check the licence when upgrading. Official agent skills: `npx skills add remotion-dev/skills`; `remotion-best-practices` covers the rest.
- Trend notes (Nov 2026): Douyin #Vibe知识大赏 — 186k participants, 4.38B plays (Nov 12). Style that holds attention: black canvas, restrained music, graphics that move with the knowledge point, subtitles appearing line by line, ending on one screenshot-worthy line. 即梦动效工作室 (Motion Studio) launched 2026-11-10 — text-to-code motion visuals are now a platform feature, confirming the code-drawn direction.

## New practices adopted from this week's research

- **Opening: make the viewer bet first.** Before stating a counter-intuitive result, pose it as a two-way choice and leave a beat for the viewer to pick a side, then reveal. (From vibe-knowledge-interactive: 0.8 s to ask, 2 s countdown, then the reveal — the same fact holds attention far longer when the viewer has committed to an answer first.) Adapt to narrated video: ask the question out loud, hold the picture still for one beat, then reveal.
- **Length calibration for ~5-minute episodes.** A 3–5 minute Chinese explainer runs 1100–1400 characters of narration across 40–50 shots in 3–4 chapters of at least 60 s each (anything2explainer reference tier; their Chinese cut: 4′54″, 1490 characters). Target ~1400–1500 characters for a 5-minute episode. Sentences inside a paragraph are separated by ~10 frames, paragraph ends by ~30 frames, and the finished video runs 5–8% longer than the raw speech by design — budget the storyboard to the finished length, not the speech length.
- **First-shot-first, then parallel build.** Build the full skeleton with placeholders, render only the first shot group (a ~30 s pilot, or the ~10–15 s trial clip for this series) and get the user's approval on the look before building the rest. Fixing the style at the pilot costs one group; fixing it after the full render costs every group.
- **Segment-parallel rendering.** Render per shot and re-render only the changed shot plus its neighbours instead of re-rendering the whole film (video-talkcraft measured: a single-shot fix on a 201 s vertical took 53 s instead of a full re-render). Keep one shared dependency install per project (one `node_modules`, ~760 MB with headless browser) instead of one per episode.
- **Text-only shots must carry a line drawing.** A shot that is only text gets an icon + box + arrow schematic as a companion picture; text never sits bare on the canvas. Every sentence must produce at least one visible change on screen.
- **Camera movement is decided per video, not a default.** The slow push or pull was only for the solar system video (user 2026-11-19) — do not add a camera move to every scene. A static camera is the default and movement comes from the animated elements in the frame. A frame with no movement at all is a defect, not a style. Idle micro-motion, ambient breathing and pulsing are off by default.
- **Review in rounds, capped.** After the machine gates pass, do one independent review round, fix P0/P1, and deliver; further rounds only on request, capped at three total. Do not loop to perfection.
- **Research discipline (Win-Hao).** Write the sourced article first with more candidate points than needed, then cut anything without a reliable source and report what was cut. Offer the user the choice of how many points to cover before writing copy.
- **Do not import a repo's sample numbers.** vibe-knowledge-interactive's own README warns its sample films contain demonstrative values and disputed concepts — verify every number before it goes on screen, same as any other source.
