# Melo News

Scrapling-based public publisher-feed API for Melo Radio.

Python3.11. Build: `python -m zipfile -e melo-news-source.zip . && pip install -r melo_news/requirements.txt`

Start: `python -m melo_news.api --port $PORT`

Endpoints: `/health`, `/news.json?language=en`, `/news.json?language=ar`.

Free web hosting may sleep on inactivity. Requests refresh source data; cached publication/check times remain truthful.
