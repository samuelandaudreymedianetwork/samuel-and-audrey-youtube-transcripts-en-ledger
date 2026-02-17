---
license: cc-by-nc-4.0
language:
- en
task_categories:
- text-generation
- question-answering
- summarization
- text-classification
tags:
- youtube
- youtube-transcripts
- travel
- food
- tourism
- vlogs
- long-form
- conversational
- voice-assistants
- rag
- eeat
- temporal
---

# 🎥 Samuel & Audrey — YouTube Transcripts (EN) Corpus (2012–2026)

## Dataset Summary

This dataset contains the complete English transcript archive from the **“Samuel and Audrey - Travel and Food Videos”** YouTube channel.

It includes **1,397 transcripts** totaling **2,288,859 words**, spanning **2012-09-16 to 2026-02-03**. Unlike polished articles, these transcripts capture real conversational pacing, on-the-ground logistics, pricing mentions, food reactions, navigation decisions, and real-time cultural observations—useful for building travel assistants that sound human, not brochure-y.

---

## Why This Dataset

**Conversational Travel Ground Truth**  
Spoken language captures decision-making (“Should we take the bus?”), uncertainty, humor, and real-world constraints that structured writing often edits out.

**Longitudinal Signal**  
A single consistent channel voice over 14 years enables temporal analysis (cost mentions, travel trends, and how destinations are discussed over time).

**Provenance + Traceability**  
Each transcript is matched to a YouTube `video_id` and canonical `url` for citation and source inspection.

---

## Dataset Structure

This release includes:

- `samuel-and-audrey-youtube-transcripts-en_hf.jsonl`  
- `samuel-and-audrey-youtube-transcripts-en_hf.jsonl.gz` (recommended)  
- `samuel-and-audrey-youtube-transcripts-en_hf.csv`  
- `samuel-and-audrey-youtube-transcripts-en_segments_hf.jsonl.gz` (optional cue-level segments for high-precision retrieval)

### Data Fields (Full Transcripts)

Each record contains:

- `id` (string): Stable transcript identifier  
- `content_hash` (string): SHA-1 hash of transcript `text` for deduplication/auditing  
- `video_id` (string): YouTube video id  
- `url` (string): Canonical watch URL  
- `published_at` (string): Publish timestamp (UTC ISO-8601)  
- `video_date` (string): Date derived from the transcript filename (YYYY-MM-DD)  
- `title` (string): Transcript filename title  
- `youtube_title` (string): YouTube title from channel export  
- `lang` (string): ISO language code (`en`)  
- `channel` (string): Channel name  
- `domain` (string): `youtube.com`  
- `source` (string): dataset source label  
- `caption_source` (string): `srt_archive`  
- `caption_track_kind` (string): `unknown` (can be refined later: auto vs uploaded captions)  
- `view_count` (int): Views at export time (channel list export)  
- `tags` (string): Comma-separated tag string (channel export)  
- `tags_list` (array): Tags parsed into a list  
- `text` (string): Plain transcript (space-joined cues)  
- `text_with_breaks` (string): Transcript with cue-level line breaks preserved  
- `srt` (string): Original SRT contents (including timestamps)  
- `original_filename` (string): Original subtitle filename

### Data Fields (Segments)

`samuel-and-audrey-youtube-transcripts-en_segments_hf.jsonl.gz` contains cue-level segments, one per subtitle cue:

- `segment_id` (string): Stable hash id for the segment  
- `transcript_id` (string): Parent transcript id  
- `video_id`, `url`, `published_at`, `video_date`, `title`, `lang`, `channel`, `domain`  
- `start_ms` (int), `end_ms` (int): Cue timestamps in milliseconds  
- `text` (string): Cue text

---

## Intended Use

This dataset is suitable for:

- Travel-domain **Retrieval-Augmented Generation (RAG)** grounded in real speech  
- Fine-tuning **conversational travel assistants** and **voice agents**  
- Long-form summarization and dialogue-style compression  
- Temporal analysis of price/cost mentions and travel trends  
- Entity extraction (places, transport, food, attractions)  
- Evaluation of grounding and hallucination resistance

---

## Provenance

All content originates from the channel:

Samuel and Audrey - Travel and Food Videos  
Platform: https://www.youtube.com  

Transcripts originate from SRT subtitle files provided by the channel owners and are enriched with YouTube metadata (`video_id`, `published_at`, `tags`, `view_count`) from a channel video list export.

---

## License and Commercial Use

License: **Creative Commons Attribution-NonCommercial 4.0 (CC BY-NC 4.0)**

Free for academic research, open-source experimentation, and non-commercial projects.

For commercial model training, enterprise deployment, or data licensing inquiries:

**nomadicsamuel@gmail.com**

---

## Citation / Attribution

If you use this dataset in a project, paper, demo, or product, please cite/credit:

**Samuel & Audrey Media Network — samuel-and-audrey-youtube-transcripts-en (Hugging Face Datasets)**

Suggested BibTeX (optional):

```bibtex
@dataset{samuel_audrey_youtube_transcripts_en,
  title={Samuel & Audrey — YouTube Transcripts (EN) Corpus (2012–2026)},
  author={Samuel & Audrey Media Network},
  year={2026},
  url={https://huggingface.co/datasets/samuelandaudreymedianetwork/samuel-and-audrey-youtube-transcripts-en},
  note={License: CC BY-NC 4.0}
}
```
