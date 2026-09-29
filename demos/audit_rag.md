---
layout: demo
title: Audit-aware RAG demo
permalink: /demos/audit-rag/
youtube_url: https://www.youtube.com/watch?v=ZOJNV82NxgE
repo: https://github.com/charleysanchez/aws-claude-rag
description: A retrieval-augmented generation pipeline on Amazon Bedrock with review gates and audit logs.
---

A retrieval-augmented generation pipeline on Amazon Bedrock, using Titan embeddings for retrieval and Claude for answers. Responses come back as strict JSON with their sources, can be held for human review before they're released, and every request is written to a JSONL audit log with a trace ID.
