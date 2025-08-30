## How to deliver this session

🥇 Thanks for delivering this session!

Prior to delivering the workshop please:

1.  Read this document and all included resources included in their entirety.
2.  Watch the video presentation
3.  Ask questions of the content leads! We're here to help!

## Presentation

### Powerpoint

Download the English version of the Powerpoint Presentation from [aka.ms/AArxlgn](https://aka.ms/AArxlgn).
Speaker notes are available on each slide.

### Video recording

[Watch the recording](https://aka.ms/AArzook)

### Timing

| Segment             | Time |
|---------------------|------|
| Segment Name        | 10:00 |


## Demos

These are the demos that you may choose to do in the presentation. You may leave some out depending on time constraints. 

### Setup

To be able to show the demos yourself, setup these two repositories:

* **RAG on AI Search**: Follow deployment instructions in [azure-search-openai-demo](https://github.com/Azure-Samples/azure-search-openai-demo), making sure to enable [the optional vision feature](https://github.com/Azure-Samples/azure-search-openai-demo/blob/main/docs/gpt4v.md)
* **RAG on PostgreSQL**: Follow instructions in [rag-postgres-openai-python](https://github.com/Azure-Samples/rag-postgres-openai-python) - Not a part of the current slide, but was in the original version.
* **Dave's repo**: https://github.com/microsoft/ai-tour-26-zava-diy-dataset-plus-mcp

cd infra && deploy.sh

./scripts/init-db.sh

python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python ./scripts/setup_azure_ai.py

Make sure each script can run successfully:

python ./scripts/keyword_search.py
python ./scripts/vector_search.py
python ./scripts/hybrid_rrf_search.py


### Video recordings

If you'd like, there are videos available for each demo. These videos have audio, which you can choose to mute and talk over.


| Demo 	                  | Duration | Video - Audio  |
--------------------------|----------|----------------|
|  1 - Keyword Search     | 3:35     | [Recording](https://assetsmanagement952e.blob.core.windows.net/assets/BRK444%20Advanced%20retrieval%20for%20your%20AI%20Apps%20and%20Agents%20on%20Azure/Demo1_KeywordSearch_V1.0.mov) |
|  2 - Vector Search      | 3:21     | [Recording](https://assetsmanagement952e.blob.core.windows.net/assets/BRK444%20Advanced%20retrieval%20for%20your%20AI%20Apps%20and%20Agents%20on%20Azure/Demo2_VectorSearch_V1.0.mov) |
|  3 - RRF Search         | 1:31     | [Recording](https://assetsmanagement952e.blob.core.windows.net/assets/BRK444%20Advanced%20retrieval%20for%20your%20AI%20Apps%20and%20Agents%20on%20Azure/Demo3_HybridRRFSearch_V1.0.mov) |
|  4 - Ranker Search      | 1:49     | [Recording](https://assetsmanagement952e.blob.core.windows.net/assets/BRK444%20Advanced%20retrieval%20for%20your%20AI%20Apps%20and%20Agents%20on%20Azure/Demo4_HybridRankerSearch_V1.0.mov) |
|  5 - Postgres Shop      | 2:04     | [Recording](https://assetsmanagement952e.blob.core.windows.net/assets/BRK444%20Advanced%20retrieval%20for%20your%20AI%20Apps%20and%20Agents%20on%20Azure/Demo5_AgenticShop_V1.0.mov) |
|  6 - Agentic AI Search  | 1:52     | [Recording](https://assetsmanagement952e.blob.core.windows.net/assets/BRK444%20Advanced%20retrieval%20for%20your%20AI%20Apps%20and%20Agents%20on%20Azure/Demo6_AISearchRAG_V1.0.mov) |
