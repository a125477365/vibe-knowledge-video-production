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

- Give every technical number a plain anchor the audience can feel — never drop a bare number or unit and assume everyone knows it (user 2026-11-21). Lead with the plain concept or term, then the number, then one familiar comparison that makes the magnitude concrete. Choose the comparison that fits that specific number and context — it is a judgement call each time, not a fixed sentence to reuse. Apply this awareness to every number in every episode, not just the one the user pointed at — when a new number appears, ask what a viewer who has never seen that unit would need to grasp it, and put that in the narration. Do not fix it by adding a definition upfront; the anchor belongs right where the number first appears.

- Before presenting any title or script for approval, do a dedicated re-read of every modifier and attributive (user 2026-11-21: 每次都要重新审定修饰语定语，通顺易懂). Read each one as a viewer who has never seen the term would: if it is technical, awkward, or hard to grasp, replace it with a plainer one. This is a fresh pass every time, for every title and every script, for any video — not just the first episode, and not just this series' episodes. Not a one-off fix.

- Synthesize narration in as few calls as you can while keeping each call reliable and keep one voice and one speed and add short crossfades between segments.

- Measure silence and flag any gap longer than 1.2 seconds and check that no segment is truncated and anchor every sound effect to its naming word and keep music under the voice at minus 14 LUFS.

## Check text and publish only after approval

- Put no black background behind on screen text and use no punctuation in subtitles unless the user asked for it and keep labels inset from the frame edge by at least 140 pixels.

- Send the finished video for user review and publish only after the user approves it and report only what you verified by measurement and what remains unverified.

- Douyin publish rules (user 2026-11-18/19): the title must not use 《》 book-title marks and must fit the 30-character limit; the cover must be manually chosen (Douyin's default cover is blank) and must carry text explanation — a plain picture frame is not acceptable, the cover needs the title/result text on it (make both a horizontal 4:3 and a vertical 3:4 text cover); topics must be selected via the # picker so they become linked topics in the description, not just typed as plain text. When editing a scheduled post, keep its identity and scheduled time unless the user asks to change them.

- Write every Douyin title topic first, then hook. Put the theme words that name what the video is about at the start of the title, then add the hook after them, inside the 30-character limit and without 《》. A hook-only title that states a surprising result without naming the topic fails this check. Before you send any title set, read each title alone and ask what topic it names; if a reader cannot tell the topic from the title itself, rewrite it before sending. For example, 远地点加速，远地点却一点不动 fails because it names no topic, while 宇宙速度 7.9 和 11.2，离开地面就变了 passes because 宇宙速度 names the topic first. This rule was added after the user corrected titles twice on 2026-11-21, first that they were not plain and attractive and then that they did not say what the video was expressing.

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

- Win-Hao/knowledge-video (Winhao学AI, the tutorial author behind this series), MIT: 6-step skill: sourced research article, scene copy of at most 20 characters per screen, first screen is the question, PD/CC0 images first or layered prompts, 3 looks as stills, beat-synced storyboard, review, render opening about 10 seconds first. Yes — method and tools. Hard rules: every fact sourced, every asset licensed, no AI-drawn faces of real people, deterministic frames. Publish checklist: sources and credits in the description, AI-generated label on.

- bobobo2026/explainer-video, MIT: word-level timeline.json spine; 13 reusable scenes hook to call to action; 9-dimension rubric, any dimension below 2 out of 5 does not ship; minus 14 LUFS; sound effects anchored to word k of sentence i. Yes — method. Render cost about 3.7 seconds wall per 1 second of video. Keep content inside platform safe areas (right button column, bottom caption zone).

- wchhywizd/vibe-knowledge-interactive, MIT (code) / CC BY 4.0 (docs): Canvas 2D plus Playwright plus ffmpeg; 100 real viral samples with play/like data; interactive counter-intuitive opening. Yes — method. Its BGM file is NOT licensed (someone else's upload) — never use it; replace any music before commercial use. Its samples are Bilibili, not Douyin — do not cross-compare absolute play counts.

- Vincentwei1021/video-talkcraft (2,331 stars) and anything2explainer (3,319 stars), PolyForm Noncommercial 1.0.0 — commercial use needs the author's prior authorisation: word-level sync (median 20–40 ms), 108 motion recipe cards, 7-layer anti-slideshow camera, segment-parallel rendering, contact-sheet QA. Ideas only — do NOT copy their code or templates into a commercial video. Videos made with them belong to the maker, but the tools themselves need authorisation for commercial use.

- ENCHIGO/explainer-video, TechNomadCode remotion-video, haidrrrry/claude-remotion-skill, MIT / open source: JSON storyboard batch rendering, Remotion skill packs. Yes, verify licence per repo before reuse.

- SpeedPainterOrg/explainer-video: sends content to a cloud service, installer runs code straight from GitHub, requires Google sign-in. Not adopted — do not install.

- Remotion itself: free for individuals, non-profits and companies with up to 3 employees; a company licence is needed beyond that. Remotion 5.0 changes the terms slightly — re-check the licence when upgrading. Official agent skills: npx skills add remotion-dev/skills; remotion-best-practices covers the rest.

- Trend notes (Nov 2026): Douyin #Vibe知识大赏 — 186k participants, 4.38B plays (Nov 12). Style that holds attention: black canvas, restrained music, graphics that move with the knowledge point, subtitles appearing line by line, ending on one screenshot-worthy line. 即梦动效工作室 (Motion Studio) launched 2026-11-10 — text-to-code motion visuals are now a platform feature, confirming the code-drawn direction.

## New practices adopted from this week's research

- **Opening: make the viewer bet first.** Before stating a counter-intuitive result, pose it as a two-way choice and leave a beat for the viewer to pick a side, then reveal. (From vibe-knowledge-interactive: 0.8 s to ask, 2 s countdown, then the reveal — the same fact holds attention far longer when the viewer has committed to an answer first.) Adapt to narrated video: ask the question out loud, hold the picture still for one beat, then reveal.

- **Length calibration for ~5-minute episodes.** A 3–5 minute Chinese explainer runs 1100–1400 characters of narration across 40–50 shots in 3–4 chapters of at least 60 s each (anything2explainer reference tier; their Chinese cut: 4′54″, 1490 characters). Target ~1400–1500 characters for a 5-minute episode. Sentences inside a paragraph are separated by ~10 frames, paragraph ends by ~30 frames, and the finished video runs 5–8% longer than the raw speech by design — budget the storyboard to the finished length, not the speech length.

- **First-shot-first, then parallel build.** Build the full skeleton with placeholders, render only the first shot group (a ~30 s pilot, or the ~10–15 s trial clip for this series) and get the user's approval on the look before building the rest. Fixing the style at the pilot costs one group; fixing it after the full render costs every group.

- **Segment-parallel rendering.** Render per shot and re-render only the changed shot plus its neighbours instead of re-rendering the whole film (video-talkcraft measured: a single-shot fix on a 201 s vertical took 53 s instead of a full re-render). Keep one shared dependency install per project (one node_modules, ~760 MB with headless browser) instead of one per episode.

- **Text-only shots must carry a line drawing.** A shot that is only text gets an icon + box + arrow schematic as a companion picture; text never sits bare on the canvas. Every sentence must produce at least one visible change on screen.

- **Camera movement is decided per video, not a default.** The slow push or pull was only for the solar system video (user 2026-11-19) — do not add a camera move to every scene. A static camera is the default and movement comes from the animated elements in the frame. A frame with no movement at all is a defect, not a style. Idle micro-motion, ambient breathing and pulsing are off by default.

- **Review in rounds, capped.** After the machine gates pass, do one independent review round, fix P0/P1, and deliver; further rounds only on request, capped at three total. Do not loop to perfection. (The GPU video 2026-11-19 used all three rounds: round 1 found 1×P0 + 6×P1, round 2 found 2×P1, round 3 found 2×P1 — budget for up to three rounds, and stop when the quota is used. Fix + re-render only the changed shots + reassemble + re-verify after each round. P2 minors do not block publish — record them honestly for the user's final call.)

- **Research discipline (Win-Hao).** Write the sourced article first with more candidate points than needed, then cut anything without a reliable source and report what was cut. Offer the user the choice of how many points to cover before writing copy.

- **Do not import a repo's sample numbers.** vibe-knowledge-interactive's own README warns its sample films contain demonstrative values and disputed concepts — verify every number before it goes on screen, same as any other source.

## 小事儿 formula — adopted 2026-11-19 (first used in the GPU video 《什么情况下，GPU 比 CPU 快？》)

Source: 小事儿's Douyin video "Redis是什么？MySQL给4个CPU还追不上它1个" (7709539666898226472, 343 s, 2026-11-18). Full study in ~/workspace/vibe-knowledge/xiaoshier-redis/STYLE-STUDY.md. Learn the method only — never copy the original video, footage, caption or script.

- **Hook = conclusion first.** A surprising number + an unfair same-condition comparison + a visible speed difference, all within 3 seconds, no definition upfront. (Redis: "9 倍" + same 1 CPU + rolling balls; GPU: "同一道数学题，CPU 算了 0.51 秒，GPU 只用了 0.016 秒，快了 32 倍。")

- **Hook-first applies to the video opening, not to the Douyin title.** The hook-first rule above governs the first seconds of the video. The Douyin title follows the topic-first rule in the Check text section: name the topic first, then the hook, so a viewer can tell what the video is about without opening it.

- **Question-first framing.** When the film itself shows the other side winning sometimes, frame the hook as the question, not the assertion — "什么情况下，GPU 比 CPU 快？" (user 2026-11-19) beats "GPU 为什么比 CPU 快" because the film shows CPU winning on serial loops and small matrices.

- **Chapters run guess → measure → explain.** One live experiment per chapter; live counters are the evidence. Define the thing in the middle, not at the start. Close each chapter with a summary graphic; end the film with "什么时候不该用" + an echo of the hook number.

- **Numbers are the animation.** Counters tick live; the diagram is a machine with balls rolling through it and the balls' speed IS the message. Time magnification / slow-motion is the core device (1 ns = 1 s in the Redis video).

- **Visual system.** Off-white / light-grey grid-paper background; black/white machines; red emphasis (key numbers/words); white balls = the requester side, red balls = the data side; huge black bold titles top-centre; bottom-centre white bold subtitles with shadow, one line per sentence, changing every ~1–3 s; monospace small text inside machines; flat micro-3D machines, black screens, glass cylinders, funnels, arched pipes; elements fade/pop in one by one inside a persistent scene; hard cuts mainly at chapter changes; watermark "个人观点，仅供参考" bottom-left throughout.

- **Voice.** The cloned 小事儿 voice (CosyVoice zero-shot from the Redis video's 2009-origin segment, voice-ref.wav, approved by the user's ear 2026-11-19) is the standing voice for tech videos. Synthesize in chunks whose length is close to the prompt length (~50–60 chars ≈ 13 s) — CosyVoice warns when a chunk is much shorter than the prompt.

- **Length and cadence (user 2026-11-19).** Keep videos short — target ~5–6 minutes. One video per week: generated on Sunday, published Friday 18:00. The GPU video ran 1265 chars → 236 s (3:56), under the target.

- **Measured numbers, not cited numbers.** Benchmark the claims on the same machine before writing them into the script, and replace every cited number with the measured value. (GPU video: 4096×4096 matmul CPU 0.51 s / GPU 0.016 s = 32×; 10,000-step serial loop CPU 466 ms / GPU 1446 ms = CPU 3× faster; 64×64 small matmul CPU 53 µs / GPU 220 µs = CPU 4× faster. The script's original 70× was replaced by the measured 32× everywhere.)

## Motion, counters, subtitles and assembly — lessons from the GPU video (2026-11-19)

- **Ball speed: never more than ~1 ball diameter per frame.** A ball moving faster strobes/teleports instead of rolling (GPU lane at 1900 px/s = 79 px/frame = 3 diameters per frame). Fix: slow the lane to ~600 px/s (25 px/frame, ≤1 diameter), spawn every 0.5 s, add a fading motion trail. A literal 32× pixel speed is unwatchable at 24 fps — the 32× lives in the counter and the narration only, not in the pixel speed.

- **Counters must reach their target and hold.** A counter that is still rolling when the shot cuts never shows its final value (Shot 3's 1370 never displayed). Roll the counter to the target by the end of the sentence and hold it ~0.6 s before the cut.

- **Anchor cues to the example, not the question.** Ball/counter cues anchored to the first mention (inside the hook question) start 2–3.5 s early. Anchor them to the second mention (the example sentence). A punchline badge pops only on the punchline word (e.g. "快了"), never from the shot's opening.

- **Subtitles: split per clause, and accept the slow-read residual.** Build subtitles from a per-clause split of each sentence (SUB_LINES: one line per spoken clause, 1–3 s per line) — a whole sentence as one subtitle line spoils the next clauses by up to 8.4 s. After three rounds of splitting, the GPU video's worst tail was still 1.94 s early and 32/128 lines were over 1 s — all because single sentences are read slowly (numbers read slowly, e.g. "一万六千三百八十四"), not cross-sentence spoilers. Pressing the whole film under 1 s would need karaoke-style per-word splits, which conflicts with the 小事儿 "one line per sentence" style. This is an ACCEPTED residual: do not chase it by changing the style unilaterally; report it honestly and leave it for the user to decide.

- **SENTENCES drives timing; SUB_LINES is display only.** Never edit SENTENCES when splitting subtitles — it drives the roll/cue timing. Edit only SUB_LINES, with context anchors so each split is unambiguous. (One accidental edit to SENTENCES was caught and restored on the spot; verify the table is intact afterwards.)

- **Whisper mis-hears words — anchor cues with the heard spelling.** Whisper normalizes numbers to digits and mis-hears words ("还得喂得饱" → "还得为的保", "四张卡" → "自征卡", "约 3×10²³ 次浮点运算" → "约3成10的23次方词辅典云算"). When a cue lookup fails, use the actual heard spelling from the transcript as the anchor, not the script text. Whisper also cannot prove a number was read correctly — only the user's ear can.

- **Font: no superscript glyphs in counters.** A mono font may lack superscript glyphs U+2074–U+2079, so an exponent renders as a tofu box. Draw exponents with regular digits scaled down and raised, never as superscript characters. (Shot 12's GPT-3 counter showed tofu for 10²³.)

- **Frozen shots: add micro-motion, never a push.** If a shot shows no pixel change over a long stretch (the GPU video had several 6–8 s frozen shots), add a continuous micro-effect to that shot — an orbiting dot, grid scaling, queue balls speeding up, a clock hand sweeping, LED blinking, matrix points pulsing, a progress line — and keep the camera static. Never fix a frozen shot with a camera push.

- **Assembly: never use `ffmpeg -shortest`.** It drops the last frame (5672/5673). Mux the full audio and video explicitly and verify the frame count afterwards.

- **Verification gates (all measured, all must pass).** Integrated loudness −16 LUFS, true peak ≤ −1 dBTP; no silence ≥0.5 s in the finished master (the GPU video measured 0.0 s; the narration-stage flag is the looser 1.2 s); every frame present (GPU video: 5673/5673); sample two frames 0.8 s apart in each shot — every shot must show pixel change and static corner/title regions must be exactly 0 (no shake); contact sheet from one frame near the end of each scene. Master: libx264 CRF 18 1080p + AAC, faststart. Preview: NVENC 720p, faststart, loudness re-measured (GPU video: master −16.19 LUFS / −1.44 dBTP, preview −16.20 LUFS).
