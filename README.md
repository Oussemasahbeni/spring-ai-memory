# Chat Memory Application

This project is a Spring Boot application that demonstrates how to build a chat application with conversational memory using Spring AI.

## Building and Running

### Prerequisites

*   Java 21 or later.
*   You need to have an OpenAI API key. The application expects this key to be available as an environment variable named `SPRING_AI_OPENAI_API_KEY`. You can set it in your environment before running the application. For example:
    ```bash
    export SPRING_AI_OPENAI_API_KEY='your-api-key-here'
    ```

To build and run the project, you can use the following Maven command:

```bash
./mvnw spring-boot:run
```

You will need Java 21 or later.

## API Endpoint

The application exposes the following endpoint:

*   `GET /hello`
    *   **Parameter:** `message` (String) - The message from the user to the chat AI.
    *   **Returns:** (String) - The AI's response.

The endpoint uses a `ChatClient` to interact with an AI model and maintains a chat history of the last 10 messages.

## Technologies Used

*   Spring Boot
*   Spring AI (with OpenAI)
*   Maven

## Conversational Memory

This application implements conversational memory using Spring AI's `MessageWindowChatMemory`. It keeps track of the last 10 messages exchanged between the user and the AI to provide context for ongoing conversations.
