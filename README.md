# ComfyUI-IxMxAMAR-Masterworks

Cross-pack masterwork workflow templates. **This pack ships zero Python nodes** — it is a workflow-only distribution combining nodes from multiple IxMxAMAR packs.

## Required Companion Packs

Install all of the following before using these workflows:

- [ComfyUI-NanoBanana2](https://github.com/IxMxAMAR/ComfyUI-NanoBanana2) — Google Gemini
- [ComfyUI-Kling-Direct](https://github.com/IxMxAMAR/ComfyUI-Kling-Direct) — Kling AI
- [ComfyUI-ElevenLabs-Pro](https://github.com/IxMxAMAR/ComfyUI-ElevenLabs-Pro) — ElevenLabs
- [ComfyUI-NanoBanana-FaceSwap](https://github.com/IxMxAMAR/ComfyUI-NanoBanana-FaceSwap) — Face swap (used by some masterworks)
- [ComfyUI-Utility-MegaPack](https://github.com/IxMxAMAR/ComfyUI-Utility-MegaPack) — Utility nodes (used by some masterworks)

## Workflows

Open `workflows/` in ComfyUI's template browser, or drag any `.json` onto the canvas.

| File | Title | Description |
|---|---|---|
| `01_short_film_production.json` | Short Film Production | End-to-end short film pipeline: Gemini writes a 4-scene script, each scene is illustrated with ImageGen, Kling animates each still into a 5-second clip, and ElevenLabs adds narration, cinematic SFX, and a score — all from a single creative prompt. |
| `02_dubbed_youtube_pipeline.json` | Dubbed YouTube Pipeline | Automated dubbing pipeline for existing video content: load a video and audio, transcribe with ElevenLabs STT, translate to French via Gemini, synthesise a new FR voice with ElevenLabs TTS, then apply Kling AdvancedLipSync to match lip movement to the dubbed audio. |
| `03_pdf_to_video_explainer.json` | PDF to Video Explainer | Transform any PDF document into a narrated explainer video: upload the PDF to Gemini Files, extract key points with VisionWithFile, refine into a spoken script with TextGen, synthesise narration with ElevenLabs TTS, then animate a presenter avatar with Kling AvatarGen. |
| `04_research_to_podcast.json` | Research to Podcast | Full AI podcast production: Gemini searches the web for a topic, a multi-turn session refines an episode outline, ElevenLabs Dialogue renders 3 distinct host voices, a music intro is generated, and everything is concatenated into a polished audio episode. |
| `05_brand_product_video.json` | Brand Product Video | Complete brand product video production: Imagen 4 generates a photorealistic hero shot, Gemini ImageEdit produces 4 brand variations (different lighting/angles), Kling animates each into a 5-second clip, and ElevenLabs layers a whoosh SFX and ambient background. |
| `06_character_consistency.json` | Character Consistency | Character identity locked across a 3-scene narrative: Gemini ImageGen creates the hero character portrait, NanoBananaWholeImageSwap transfers that identity into 3 distinct story scenes, and Kling animates each consistent scene into a 5-second clip. |
| `07_audiobook_to_animated.json` | Audiobook to Animated | Transform a long-form text into 4 animated audiobook chapters: ElevenLabs TTS narrates each chapter passage, Kling AvatarGen animates a narrator portrait lip-synced to each audio, and all 4 avatar videos are saved as individual chapter files. |
| `08_multilang_brand_launch.json` | Multilang Brand Launch | Global brand launch in 5 languages: Gemini writes the master script, 5 TextGen nodes translate to EN/ES/FR/DE/JA, ElevenLabs TTS synthesises each locale with a native-appropriate voice, and Kling animates a brand image into 5 language-specific video deliverables. |
| `09_music_video_full.json` | Music Video Full | Complete AI music video production: Lyria generates an original score, Imagen 4 creates the album art/cover image, Veo generates a cinematic video clip, and ElevenLabs layers cinematic impact SFX — all from a single creative concept. |
| `10_explainer_visual_essay.json` | Explainer Visual Essay | Visual essay production pipeline: Gemini Vision analyzes a source image, TextGen writes a narrated essay, Kling MultiShot generates 3 cinematic keyframes, ElevenLabs TTSTimestamps narrates with word-level timing, and SubtitleExport produces a broadcast-ready SRT file. |
| `11_face_swap_video_dub.json` | Face Swap Video Dub | Deep personalisation pipeline: load a source video, swap the on-screen face with a target identity using NanoBananaWholeImageSwap on a batch of frames, clone a new voice from a sample with ElevenLabs VoiceClone, synthesise dubbed audio with TTS, then apply Kling AdvancedLipSync for lip-matching. |
| `12_data_to_narrated_chart.json` | Data to Narrated Chart | Turn live data into a narrated audio summary: UtilMegaPack IOWorkflow fetches JSON data via HTTP GET, a Programming node extracts a summary string, Gemini TextGen writes a human insight paragraph, ElevenLabs TTS narrates it as a professional data report, and TTSTimestamps with SubtitleExport produces a broadcast-ready SRT for captioned playback. |

## Usage

Each workflow expects you to fill in API keys for the services it uses (Gemini, Kling, ElevenLabs). Visit the respective companion packs' README files for setup instructions.
