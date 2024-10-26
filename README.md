## Anime Recommender RAG based LLM

## Project Purpose

There are several sources for getting anime recommendations such as MyAnimeList, Reddit and so on. However, the scores could be biased and sometimes anime fans like myself go down a rabbit hole digging through subreddits and so on to find the perfect anime to watch. This project aims to solve this problem by providing a chatbot interface where users can ask for anime recommendations based on their preferences. The chatbot uses the LLM model to generate responses and provide recommendations.

## Instructions

#### Setup

1. Download [llava-v1.5-7b-q4.llamafile](https://huggingface.co/Mozilla/llava-v1.5-7b-llamafile/resolve/main/llava-v1.5-7b-q4.llamafile?download=true) (4.29 GB).

2. Open your computer's terminal.

3. If you're using macOS, Linux, or BSD, you'll need to grant permission
   for your computer to execute this new file. (You only need to do this
   once.)

```sh
chmod +x llava-v1.5-7b-q4.llamafile
```

4. If you're on Windows, rename the file by adding ".exe" on the end.

5. Run the llamafile. e.g.:

```sh
./llava-v1.5-7b-q4.llamafile
```

6. Your browser should open automatically and display a chat interface.
   (If it doesn't, just open your browser and point it at http://localhost:8080)

7. When you're done chatting, return to your terminal and hit
   `Control-C` to shut down llamafile.

8. Clone the repository

9. Change directory to the cloned repository

```sh
cd anime-recommendation-rag
```

10. Install the dependencies

```sh
pip install -r requirements.txt
```

#### Running the application

1. Start the FastAPI server

```sh
PYTHONPATH=. fastapi dev backend/server.py
(or run using the Docker image)
docker run --platform linux/x86_64 -e MODEL_URL=http://127.0.0.1:8080/v1/chat/completions -p 8000:8000 --network="host" ketankeshava/anime-recommendation-backend
```

2. Start the streamlit frontend application

```sh
streamlit run frontend/ui.py
```

