## How to deliver this session

🥇 Thanks for delivering this session!

Prior to delivering the workshop please:

1.  Read this document and all included resources included in their entirety.
2.  Watch the video presentation
3.  Ask questions of the content leads! We're here to help!

## Presentation

### Powerpoint

Download the [English version of the Powerpoint presentation](https://microsoft.sharepoint.com/:p:/t/EventSessionUploads/EfGaf8bHX0FEkJRrBmQcD08Bwniycmt4yt3VWDB_i_l1oQ?e=EJ4bBH).
Speaker notes are available for each slide.

### Video recording

[Watch the recording](https://aka.ms/AArzook)

### Timing

| Segment             | Time  |
|---------------------|-------|
| Segment Name        | 10:00 |

## Demos

There are six demos in the presentation, from three different samples:

* **[Zava products database](https://github.com/microsoft/ai-tour-26-zava-diy-dataset-plus-mcp)**: Python scripts that demonstrate different search strategies on a PostgreSQL database.
* **[Agentic Shop](https://github.com/Azure-Samples/postgres-agentic-shop)**: An E2E full-stack app powered by Azure Database for PostgreSQL, showcasing graph query retrieval.
* **[RAG on AI Search](https://github.com/Azure-Samples/azure-search-openai-demo/)**: An E2E full-stack app powered by Azure AI Search, showcasing agentic retrieval.

### Setup

To be able to show the demos yourself, you will need to set up the three codebases.

#### Zava products database

1. Clone [the repo](https://github.com/microsoft/ai-tour-26-zava-diy-dataset-plus-mcp) OR navigate into the `src` folder, where the repo is checked in as a submodule.

    ```bash
    cd ai-tour-26-zava-diy-dataset-plus-mcp
    ```

2. Deploy the necessary infrastructure:

    ```bash
    cd infra && deploy.sh
    ```

3. Initialize the database with seed product data:

    ```bash
    ./scripts/init-db.sh
    ```

4. Setup the Python environment and install dependencies:

    ```bash
    python -m venv .venv
    source .venv/bin/activate
    pip install -r requirements.txt
    ```

5. Configure the Azure AI extensions for Azure Database for PostgreSQL:

    ```
    python ./scripts/setup_azure_ai.py
    ```

6. Test that each script runs successfully:

    ```bash
    python ./scripts/keyword_search.py
    python ./scripts/vector_search.py
    python ./scripts/hybrid_rrf_search.py
    python ./scripts/hybrid_ranker_search.py
    ```

7. Install the PostgreSQL extension for VS Code and create a new server connection for the provisioned Azure database. Navigate to zava database, open the retail schema, and use the context menu to visualize the schema.

#### Agentic Shop

1. Clone [the repo](https://github.com/Azure-Samples/postgres-agentic-shop) OR navigate into the `src` folder, where the repo is checked in as a submodule.

    ```bash
    cd postgres-agentic-shop
    ```

2. Create a new azd environment:

    ```bash
    azd env new
    ```

2. Provision the Azure resources and deploy the app:

    ```bash
    azd up
    ```

3. Navigate to the deployed frontend endpoint and confirm that the application is running. Test the search for "headphones with good reviews about noise cancellation" works.

#### RAG on AI Search

1. Clone [the repo](https://github.com/Azure-Samples/azure-search-openai-demo) OR navigate into the `src` folder, where the repo is checked in as a submodule.

    ```bash
    cd azure-search-openai-demo
    ```

2. Create a new azd environment:

    ```bash
    azd env new
    ```

3. Enable agentic retreival:

    ```bash
    azd env set USE_AGENTIC_RETRIEVAL true
    ```

4. Provision the Azure resources and deploy the app:

    ```bash
    azd up
    ```

5. Navigate to the deployed endpoint and confirm the app is working. Test the question "How do expectations differ for Manager of Product Management vs Senior Manager of PM?"

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
