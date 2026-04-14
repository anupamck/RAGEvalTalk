# RAG evals: A Live Demo

_Anupam Krishnamurthy_

A rag model is built using the RAG tutorial from Langchain: https://python.langchain.com/docs/tutorials/rag/. Here, I have connected the [basecamp handbook ](https://basecamp.com/handbook) as the custom datasource, and used [Ragas](https://github.com/explodinggradients/ragas/tree/main/docs) for evaluating the RAG model's responses. 

This repo is linked to this [research task](https://github.com/BeyondQuality/beyondquality/blob/main/research/rag-evaluation.md) from the BeyondQuality community. 

To access a more in-depth workshop version of this talk, head to https://github.com/anupamck/tad26Workshop. 

## Setup
### Configure APIs
1. Get an account at LangSmith: https://smith.langchain.com/ and create a project (Choose `US` as the region)
2. To get the value of `OPENAI_API_KEY`, head over to this [document](https://www.protectedtext.com/tad2026workshop) and use the password `tad2026`. Update the value of the `OPENAI_API_KEY` in your `.env` file.
3. Add your API keys and project name from LangSmith to your `.env` file
   
### Quickstart (via Docker)
#### Prerequisites
 - Docker desktop installed on local machine. 

1. Start Docker desktop.
   
2. In a new terminal or command prompt window, run the following command to build and start Jupyter Lab:
   ```bash
   docker compose up --build
   ```
3. Open your browser at `http://localhost:8888` (no token/password required).

Your current folder is mounted into the container at `/workspace`, so changes you make to notebooks and files are saved on your host.

To stop the server, press Ctrl+C in the terminal or run:
```bash
docker compose down
```

### Start without Docker
#### Prerequisites 
- Python 3.10 or newer

1. Install all dependencies in requirements.txt, preferably in a python virtual environment
2. Open jupyter lab via `jupyter lab`

## Run the handbook 
1. Open http://localhost:8888/lab on your browser. 
2. Open the basecampHandbookRagWithRagas.ipynb in the Jupyter lab UI.
3. Explore the handbook by running each block using the UI. 
4. View the LangSmith traces of the LLM calls in the LangSmith UI.
