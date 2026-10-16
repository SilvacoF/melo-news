# Melo News and Radio backend

Public publisher-feed collection using Scrapling, independent native English/Arabic neural bulletins, and optional bounded EmbeddingGemma topic advice. Up to20 news items per language use exact publisher headlines or brief source-provided reporting details, with original dates and attribution preserved in metadata. Spoken breaks omit date/link/reference footers. No station deployment keys are needed.

New speech includes the exact headline plus one short complete publisher detail where available, retaining qualifications and source evidence. Missing or unsafe details remain headline-only; the model never invents them.

Python 3.11. Build: `python -m zipfile -e melo-news-source.zip . && pip install -r melo_news/requirements.txt && python -m melo_news.bootstrap_models`

Start: `python -m melo_news.api --port $PORT`

Endpoints: `/health`, `/news.json?language=en|ar`, `/radio/status`, `/radio-program.json?language=en|ar`, `/radio/podcasts.json?language=en|ar`, `/radio/audio/<sha256>.mp3`.

Bilingual discussions target a new pair every three minutes while awake.
One female and one male AI presenter debate the same available topic in each
language, with exact native publisher reporting separated from reviewed
contrasting opinions. Each composed episode exceeds two listening minutes,
including Arabic at 1.3× speed. Seventeen alternating turns use four pinned
native voices. Reusable reviewed speech ships as hashed, fully decoded audio;
only fresh source reporting and composition run on the free host.

Each episode has initial/+60/+150-minute airing opportunities with three-hour
expiry. Music is never interrupted; missed opportunities expire. Generation
cadence is not a guarantee of hearing every episode and repeat. Both language
recordings activate together. Sleep or restarts may delay work or lose the
queue. No model generates facts or arguments; EmbeddingGemma stays advisory.

Both native audio editions activate together only after full MP3 decoding. Reviewed entertainment ships with the source. Six joke breaks rotate at most every six hours; original fictional stories stay fixed until reviewed replacements. Publisher-only good/offbeat labels are preserved. Model downloads are pinned by revision and SHA256; model workers terminate before speech synthesis. LiquidAI failed the small quality evaluation and is not used; MiniCPM is too large for the selected free instance; Bonsai is deferred.

Free Render hosting sleeps after inactivity and has ephemeral generated caches. Requests wake it; the station keeps its dated published fallback while a cold host prepares fresh news and audio. This is not a promise of uninterrupted CPU execution.

Spoken news refreshes on a ten-minute start cadence while awake. Cold starts activate a complete eight-report native bilingual pair before expanding to twenty; failures retain the playable pair. The existing station keeps a hash-verified native audio reserve during free-host sleep.
