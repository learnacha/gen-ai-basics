# Creating Multiple LLM Functionalities in a Generative AI Application

## Overview
This lesson demonstrates how to create a single application that incorporates multiple Large Language Model (LLM) functionalities. The example application is a text summarizer that provides different types of summaries using the same underlying LLM model.

## Key Concepts

### 1. Modular Function Design
- The application uses a single LLM model (Groq's llama3-70b-8192) to perform multiple types of text summarization
- Each functionality is implemented as a separate function that can be called independently
- The `summarize_text()` function takes two parameters:
  - `text`: The input text to summarize
  - `summary_type`: The type of summary to generate

### 2. Multiple Functionalities
The application provides four different types of summaries:
1. **Normal Summary**: A standard summary of the text
2. **Short Summary**: A concise summary limited to 10 words
3. **Simple Summary**: A summary written in layman's terms
4. **Bullet Point Summary**: A summary presented in 3 bullet points

### 3. Dynamic Prompt Engineering
- Each summary type uses a different prompt template
- The prompts are designed to guide the LLM to produce the desired output format
- Example prompts:
  - Normal: "Summarize the text: {text}"
  - Short: "Summarize the text in 10 words: {text}"
  - Simple: "Summarize the text in layman terms: {text}"
  - Bullet Points: "Summarize the text in 3 bullet points: {text}"

### 4. User Interface Integration
- The application uses Streamlit to create an interactive web interface
- Each functionality has its own dedicated button
- The interface provides immediate feedback and handles error cases (e.g., empty input)

## Technical Implementation
- Uses the `llama_index` library to interface with the LLM
- Implements environment variable management for API keys
- Creates a clean, user-friendly interface with Streamlit
- Handles multiple input/output scenarios gracefully

## Best Practices Demonstrated
1. **Separation of Concerns**: Each summary type is handled independently
2. **Code Reusability**: The same LLM model is used for all functionalities
3. **User Experience**: Clear interface with distinct options for different needs
4. **Error Handling**: Proper validation of user input
5. **Security**: Secure handling of API keys through environment variables

## Applications
This approach can be extended to create various types of applications:
- Multi-functional chatbots
- Content generation tools with different styles
- Document processing applications
- Educational tools with different learning modes 