# Melo News and Radio backend

Public publisher-feed collection using Scrapling, independent native English/Arabic neural bulletins, and optional bounded EmbeddingGemma topic advice. News facts remain exact publisher headlines with original dates and attribution. No station deployment keys are needed.

Python 3.11. Build: `python -m zipfile -e melo-news-source.zip . && pip install -r melo_news/requirements.txt && python -m melo_news.bootstrap_models`

Start: `python -m melo_news.api --port $PORT`

Endpoints: `/health`, `/news.json?language=en|ar`, `/radio/status`, `/radio-program.json?language=en|ar`, `/radio/audio/<sha256>.mp3`.

Both native audio editions activate together only after full MP3 decoding. Reviewed entertainment ships with the source. Six joke breaks rotate at most every six hours; original fictional stories stay fixed until reviewed replacements. Publisher-only good/offbeat labels are preserved. Model downloads are pinned by revision and SHA256; model workers terminate before speech synthesis. LiquidAI failed the small quality evaluation and is not used; MiniCPM is too large for the selected free instance; Bonsai is deferred.

Free Render hosting sleeps after inactivity and has ephemeral generated caches. Requests wake it; the station keeps its dated published fallback while a cold host prepares fresh news and audio. This is not a promise of uninterrupted CPU execution.
