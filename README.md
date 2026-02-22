# 🎥 Samuel & Audrey — YouTube Transcripts (EN) Corpus (2012–2026)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18665704.svg)](https://zenodo.org/records/18665704)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0006--3748--9630-A6CE39.svg)](https://orcid.org/0009-0006-3748-9630)
[![Hugging Face](https://img.shields.io/badge/🤗_Hugging_Face-Download_Dataset-FFD21E.svg)](https://huggingface.co/datasets/samuelandaudreymedianetwork/samuel-and-audrey-youtube-transcripts-en)
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

## 📌 Context & Provenance
This repository contains the canonical English transcript archive from the **“Samuel and Audrey - Travel and Food Videos”** YouTube channel. 

Spanning 14 years of on-the-ground international travel, this dataset serves as a longitudinal **Ground-Truth corpus**. Unlike polished articles, these transcripts capture unedited human decision-making, conversational pacing, logistics, pricing mentions, food reactions, and real-world constraints—making it an ideal resource for building travel assistants that sound human, not brochure-y.

---

## 📊 Counts Snapshot
A massive repository of spoken-word travel intelligence anchored by high-signal **E-E-A-T** (Experience, Expertise, Authoritativeness, and Trustworthiness).

| Metric | Count | Description |
| :--- | :--- | :--- |
| **Total Transcripts** | `1,397` | Full-length episodic videos. |
| **Total Words** | `2,288,859` | Spoken conversational tokens. |
| **Cue-Level Segments** | `1.54 Million` | High-precision segmented rows for RAG indexing. |
| **Time Span** | `14 Years` | 2012-09-16 to 2026-02-03. |

---

## 🚀 Why Use This Dataset?
* **Conversational Ground Truth:** Captures real speech ("Should we take the bus?", "How much is this?") and uncertainty that structured writing edits out.
* **Longitudinal Signal:** A single consistent channel voice over 14 years enables temporal analysis of cost mentions, travel trends, and global infrastructure changes.
* **Provenance + Traceability:** Every transcript is cryptographically hashed and matched directly to a YouTube `video_id` and canonical `url` for citation and source inspection.

---

## 📂 Canonical Files & Architecture
*(Note: Due to GitHub's file size limits, the primary `.gz` data files are hosted on our Hugging Face and Zenodo repositories. See badges above for direct links).*

This release includes files optimized for LLM context windows, streaming, and RAG ingestion:
* `samuel-and-audrey-youtube-transcripts-en.jsonl.gz` **(Recommended for Full Transcripts)**
* `samuel-and-audrey-youtube-transcripts-en.jsonl`
* `samuel-and-audrey-youtube-transcripts-en.csv`
* `samuel-and-audrey-youtube-transcripts-en_segments.jsonl.gz` **(Recommended for RAG: cue-level segments for high-precision retrieval)**

### Data Schema Overview
For a complete structural breakdown, please refer to the [`DATA_DICTIONARY.md`](DATA_DICTIONARY.md) file in this repository. 

**Full Transcripts Core Fields:**
* `id` / `content_hash`: Identifiers and cryptographic deduplication
* `video_id` / `url`: Canonical YouTube identifiers
* `published_at` / `video_date`: Temporal metadata
* `tags_list`: Array of semantic tags
* `text` / `text_with_breaks` / `srt`: The transcript payload in various unrolled formats

---

## 🎯 Intended Use
This dataset is specifically engineered for:
* Travel-domain **Retrieval-Augmented Generation (RAG)** grounded in real speech.
* Fine-tuning **conversational travel assistants** and **voice agents**.
* Long-form summarization and dialogue-style compression.
* Temporal analysis of price/cost mentions and macro travel trends.
* Evaluation of grounding and hallucination resistance in LLMs.

---

## 🔍 Data Preview
<details>
<summary>Click to view a sample raw transcript block</summary>

```text
index: 1
transcript_id: 79bc53819f2f1ff2
content_hash: 8dae51261291157676fa604d14fdec2181eaf747
video_id: g7-wj8jaF0Q
url: [https://www.youtube.com/watch?v=g7-wj8jaF0Q](https://www.youtube.com/watch?v=g7-wj8jaF0Q)
published_at: 2012-09-16T00:31:08Z
video_date: 2012-09-16
title: Exploring Sindorim, Guro & Gocheok Dong in Seoul, Korea
view_count: 11215

text: Today we are doing the Seoul subway challenge, so we've been assigned line two and the idea is to explore as many stops as possible. We're going back to an area that used to be a part of my old stomping grounds - Sindorim...
