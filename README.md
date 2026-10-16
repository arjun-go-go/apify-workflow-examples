# Apify workflow examples

Small, practical workflows for using Arjun AI's Apify Actors with other tools.

## YouTube transcripts to Google Sheets

Save an existing YouTube caption track to Google Sheets, with one video per row. The workflow uses [YouTube Transcript Scraper](https://apify.com/arjun_code/youtube-transcript-scraper) and does not download or transcribe audio.

- [Importable n8n workflow](youtube-transcripts-to-google-sheets/workflow.json)
- [Download workflow JSON](https://raw.githubusercontent.com/arjun-go-go/apify-workflow-examples/main/youtube-transcripts-to-google-sheets/workflow.json)
- [Setup instructions](youtube-transcripts-to-google-sheets/README.md)
- [Actor input example](youtube-transcripts-to-google-sheets/examples/input.json)
- [Real result examples](youtube-transcripts-to-google-sheets/examples/verified-results.json)
- [Publication copy and submission route](youtube-transcripts-to-google-sheets/PROMOTION.md)
- [Screenshot notes](youtube-transcripts-to-google-sheets/assets/README.md)

The workflow files contain no API tokens, connected accounts, or private Actor source. Each user connects their own Apify and Google accounts. Downloading a workflow does not make Actor runs or third-party services free.

The publication package contains written instructions and screenshots, not a video recording. Files under `local/` are private implementation notes and are not part of the shareable package.
