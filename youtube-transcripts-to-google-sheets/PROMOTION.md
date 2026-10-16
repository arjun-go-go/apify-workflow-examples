# YouTube transcript workflow publication copy

Use the text below with the importable `workflow.json` and the setup guide in the [public repository](https://github.com/arjun-go-go/apify-workflow-examples). The repository is the current download destination; this workflow has not been submitted to or approved for the n8n template gallery.

## n8n template title

Save YouTube transcripts to Google Sheets with Apify

## Short description

Retrieve an existing YouTube caption track and save its full text, language, and video metadata to Google Sheets with Apify and n8n.

## Template description

Collect existing YouTube captions in a spreadsheet for research notes, content review, and later LLM workflows. Enter one video or Shorts URL, connect your own Apify and Google Sheets credentials, and run the workflow manually.

### How it works

The workflow starts YouTube Transcript Scraper, waits for the Actor to finish, and reads that run's Dataset. A successful caption track adds one row with the video ID, title, URL, channel, returned language, automatic-caption flag, complete fetched text, and extraction time.

Caption statuses such as `noTranscript`, `languageUnavailable`, and `requestBlocked` follow a separate branch. They are not written as empty transcripts. Failed Actor runs can still provide their saved status records; a completed n8n execution does not itself guarantee a transcript was found.

### Setup

1. Install the official `@apify/n8n-nodes-apify` node and import `workflow.json`.
2. Create a worksheet named `Transcripts` with the eight headers from the setup guide.
3. Select the same Apify credential on both Apify nodes and connect Google Sheets.
4. Set `videoUrl`, `spreadsheetUrl`, and `sheetName` in **Workflow input**.
5. Execute manually and inspect the successful row or caption-status branch.

### Costs and scope

The workflow has no separate fee. As checked on October 16, 2026, the Actor charges $0.002 per successfully saved transcript plus $0.00005 per start at this workflow's 512 MB setting. n8n and Google services may have their own charges. Review the Actor's current Store pricing before running.

This retrieves existing captions. It does not transcribe audio, translate, or summarize. Source captions can contain mistakes or omit speech. This example requests text only, not SRT/VTT files. It is single-video, manual, and append-only; rerunning a successful URL adds another row.

[YouTube Transcript Scraper](https://apify.com/arjun_code/youtube-transcript-scraper) by Arjun AI. Independent tool, not affiliated with YouTube or Google.

## Suggested search phrases

YouTube transcript to Google Sheets; YouTube captions n8n workflow; Apify YouTube transcript scraper; save video captions for research.

These describe the use case, not a list to repeat in every paragraph. Select matching categories offered by the submission form rather than treating these phrases as official category names.

## LinkedIn or community post

I built a small n8n workflow for a practical research task: save existing YouTube captions to Google Sheets.

One video URL becomes one row with its title, channel, caption language, and full fetched text. There is also a separate status branch for missing captions or blocked requests, so failures are not saved as blank transcripts.

In one verified example, the workflow saved 7,038 characters of English captions and the spreadsheet text matched the Actor's returned text exactly. That run took 21.191 seconds; timing and availability vary.

It uses YouTube Transcript Scraper on Apify. It reads available captions rather than transcribing audio. The Actor is paid, and you connect your own Apify and Google Sheets accounts.

Useful for research notes and preparing text for a later LLM workflow.

Workflow JSON and setup guide: https://github.com/arjun-go-go/apify-workflow-examples

Actor: https://apify.com/arjun_code/youtube-transcript-scraper

Attach `assets/workflow.png` and `assets/sheets-output.png` when publishing. Use the public repository link above; add an n8n template gallery link only after a template has been accepted and its public URL is known.

## Short social post

YouTube URL → existing captions → Google Sheets. This n8n workflow saves full caption text and video metadata, with a separate status branch. Paid Actor; no audio transcription. Workflow and guide: https://github.com/arjun-go-go/apify-workflow-examples

## Actor README integration paragraph

Save existing captions to Google Sheets with n8n. This manual workflow writes one selected caption track per video and routes caption-status records separately. Connect your own Apify and Google Sheets accounts. It does not transcribe audio or generate summaries.

[Import the workflow and follow the setup guide](https://github.com/arjun-go-go/apify-workflow-examples/tree/main/youtube-transcripts-to-google-sheets).

This paragraph is prepared for the Actor's integrations section; it has not been applied to the Store README. Do not link the private n8n instance or personal spreadsheet.

## Submission route

Start from [n8n's official template documentation](https://docs.n8n.io/workflows/templates/) and follow its link to the Creator hub. Use the current creator and submission process shown there. The title and description above are prepared copy, not a claim that an application or template has been submitted or approved.

Upload `workflow.json`, use the setup guide for the long description, and attach supported screenshot files if the form offers image uploads. This package contains no recording. Review any account or publication agreement yourself before acceptance.
