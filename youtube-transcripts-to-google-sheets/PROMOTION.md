# YouTube transcript workflow publication copy

Use the text below with the importable `workflow.json` and the setup guide in the [public repository](https://github.com/arjun-go-go/apify-workflow-examples). The repository is the current download destination; this workflow has not been submitted to or approved for the n8n template gallery.

## n8n template title

Save YouTube transcripts to Google Sheets with Apify

## Short description

Retrieve an existing YouTube caption track and save its full text, language, and video metadata to Google Sheets with Apify and n8n.

## Template description

![Workflow overview](https://raw.githubusercontent.com/arjun-go-go/apify-workflow-examples/main/youtube-transcripts-to-google-sheets/assets/workflow.png)

### Who is this for?

Researchers and content teams who want existing YouTube captions in a spreadsheet for review or later LLM workflows.

### What it does

Enter one video or Shorts URL. Apify retrieves one selected caption track. The workflow saves its full fetched text, title, URL, channel, language, automatic-caption flag, and extraction time in one Google Sheets row.

Missing captions and blocked requests follow a separate status branch, not blank transcript rows.

### Setup

1. Install the verified Apify node and import the workflow JSON.
2. Connect your own Apify and Google Sheets credentials.
3. Create a worksheet with the eight headers in the [setup guide](https://github.com/arjun-go-go/apify-workflow-examples/tree/main/youtube-transcripts-to-google-sheets).
4. Set `videoUrl`, `spreadsheetUrl`, and `sheetName` in **Workflow input**, then execute manually.

### Requirements and cost

Requires n8n with the Apify node, an Apify account, Google Sheets access, and a video with captions. Verified Apify nodes support n8n Cloud and self-hosted instances.

The template has no separate fee. Actor runs are paid; check [current pricing](https://apify.com/arjun_code/youtube-transcript-scraper). Other service charges may apply.

### Customization and limits

Change the Actor language settings if needed. This example requests text only, not SRT/VTT. Rerunning a successful URL appends another row. It does not transcribe, translate, summarize, or schedule runs. Source captions can contain errors or omit speech.

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

The tutorial link and an expanded integration guide are live in the Actor's Store README as of build 0.1.15 (October 16, 2026). Do not link the private n8n instance or personal spreadsheet.

## Submission route

Start from [n8n's official template documentation](https://docs.n8n.io/workflows/templates/) and follow its link to the Creator hub. Use the current creator and submission process shown there. The title and description above are prepared copy, not a claim that an application or template has been submitted or approved.

The Creator Portal uses a separate account from n8n Cloud. Register at https://creators.n8n.io/register or sign in at https://creators.n8n.io/login. Upload `workflow.json` and use the approximately 200-word Template description above. It includes a workflow image and setup instructions; the canvas note contains the same description text. This package contains no recording. Review any account or publication agreement yourself before acceptance.

The submission guidelines contain a general self-hosted-only warning for community nodes. This workflow uses Apify's verified node, which [Apify documents as supporting n8n Cloud and self-hosted instances](https://apify.com/integrations/n8n), and the example was verified on Cloud. Describe that dependency accurately rather than claiming that it is self-hosted only. Gallery acceptance is still subject to n8n review.
