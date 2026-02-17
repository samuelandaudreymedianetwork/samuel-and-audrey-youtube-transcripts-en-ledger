# Data Dictionary — Samuel & Audrey — YouTube Transcripts (EN) Corpus (2012–2026)

| Field | JSON types observed | Description |
|---|---|---|
| id | string | Stable transcript identifier. |
| content_hash | string | Field preserved from source metadata. |
| video_id | string | YouTube video identifier. |
| url | string | Canonical YouTube watch URL. |
| published_at | string | Publish timestamp (UTC ISO-8601). |
| video_date | string | Date derived from original subtitle filename (YYYY-MM-DD). |
| title | string | Transcript filename title. |
| youtube_title | string | YouTube title from channel export. |
| lang | string | ISO language code. |
| channel | string | Channel name. |
| domain | string | Source domain. |
| source | string | Field preserved from source metadata. |
| caption_source | string | Field preserved from source metadata. |
| caption_track_kind | string | Field preserved from source metadata. |
| view_count | integer | Views at export time (from channel list export). |
| tags | string | Comma-separated tags string. |
| tags_list | array | Tags parsed into a list. |
| text | string | Plain transcript (space-joined cues). |
| text_with_breaks | string | Transcript with cue-level line breaks preserved. |
| srt | string | Original SRT contents (timestamps + cues). |
| original_filename | string | Original subtitle filename. |
