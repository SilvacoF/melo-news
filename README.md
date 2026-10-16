# Melo News and Radio backend

Public publisher-feed collection using Scrapling, independent native English/Arabic neural bulletins, and optional bounded EmbeddingGemma topic advice. Up to20 news items per language use exact publisher headlines or brief source-provided reporting details, with original dates and attribution preserved in metadata. Spoken breaks omit date/link/reference footers. No station deployment keys are needed.

New speech includes the exact headline plus one short complete publisher detail where available, retaining qualifications and source evidence. Missing or unsafe details remain headline-only; the model never invents them.

Python 3.11. Build: `python -m zipfile -e melo-news-source.zip . && pip install -r melo_news/requirements.txt && python -m melo_news.bootstrap_models`

Start: `python -m melo_news.api --port $PORT`

Endpoints: `/health`, `/news.json?language=en|ar`, `/radio/status`, `/radio-program.json?language=en|ar`, `/radio/podcasts.json?language=en|ar`, `/radio/audio/<sha256>.mp3`.

Short bilingual podcasts are curated about every ten minutes while awake from four native publisher reports and optional advisory topic tags. Exact reporting and reviewed host lines are narrated with free native voices; no model writes facts. Each episode is scheduled initially and twice more at +60 and +150 minutes, with a three-hour expiry. Both hashed recordings activate together. Sleep and ephemeral restarts can delay creation or lose episodes; missed intervals are not backfilled.

Both native audio editions activate together only after full MP3 decoding. Reviewed entertainment ships with the source. Six joke breaks rotate at most every six hours; original fictional stories stay fixed until reviewed replacements. Publisher-only good/offbeat labels are preserved. Model downloads are pinned by revision and SHA256; model workers terminate before speech synthesis. LiquidAI failed the small quality evaluation and is not used; MiniCPM is too large for the selected free instance; Bonsai is deferred.

Free Render hosting sleeps after inactivity and has ephemeral generated caches. Requests wake it; the station keeps its dated published fallback while a cold host prepares fresh news and audio. This is not a promise of uninterrupted CPU execution.
