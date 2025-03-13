1. Build Ollama and Microservice Containers
   ```bash
   docker compose up --build
   ```

2. Pull Model
   ```bash
   docker exec -it ollama_service /bin/bash
   ollama pull mistral
   exit
   ```

3. Run Command to send prompt
   ```bash
   curl -X POST http://127.0.0.1:5000/generate -H "Content-Type: application/json" -d '{"prompt": "Say 1 word"}'
   ```
4. Command to use model
   ```bash
   ollama run llama3.2 "How many days are there in a year?"
   ```
