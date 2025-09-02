# Spring AI Redis Example

This project demonstrates integrating **Spring AI** with **Redis Stack** for vector storage and retrieval, using OpenAI embeddings.

## Features

- Uses **Spring Boot** for application framework.
- Integrates **Spring AI** with OpenAI's `text-embedding-ada-002` model for generating vector embeddings.
- Stores and queries embeddings in **Redis Stack** using RediSearch.
- REST API for interacting with the AI model and vector store.

## AI Model Details

- **Model:** `text-embedding-ada-002`
- **Provider:** OpenAI
- **Purpose:** Generates vector embeddings for text data, enabling semantic search and similarity queries.

## Dependencies

- Java 17+
- Spring Boot 3.3.0
- Spring AI 1.0.0-M2
- Redis Stack (with RediSearch)
- Maven

## Setup

1. **Clone the repository:**
 git clone <your-repo-url> cd spring-ai-redis
2. **Start Redis Stack:**
   docker run -d --name redis-stack -p 6379:6379 -p 8001:8001 redis/redis-stack:latest

4. **Configure OpenAI API Key:**
   - Set your OpenAI API key in `src/main/resources/application.properties`:
     ```
     spring.ai.openai.api-key=sk-...
     ```

5. **Build and run the application:**

## Configuration

Main properties in `application.properties`:
- `spring.ai.openai.api-key`: Your OpenAI API key.
- `spring.ai.openai.embedding.options.model`: AI model used (`text-embedding-ada-002`).
- `spring.redis.host` / `spring.redis.port`: Redis Stack connection.
- `spring.ai.vectorstore.redis.index-name`: Redis index for vector storage.

## Usage

- Access REST endpoints to store and query text embeddings.
- Redis Stack must be running with RediSearch enabled.
