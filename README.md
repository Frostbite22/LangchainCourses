# Langchain Courses on Deeplearning.AI
These courses are available in deeplearningAI platform freely. 

[Courses can be found here](https://www.deeplearning.ai/courses/?dev_courses_date_desc%5BrefinementList%5D%5Bpartnership%5D%5B0%5D=LangChain)

## Course 1 : LangChain for LLM Application Development
[Link to the course](https://www.deeplearning.ai/short-courses/langchain-for-llm-application-development/)

## Course 2 : Langchain Chat With your Data
[Link to the course](https://learn.deeplearning.ai/courses/langchain-chat-with-your-data)

## Course 3 : Functions, Tools and Agents with LangChain
[Link to course](https://learn.deeplearning.ai/courses/functions-tools-agents-langchain/)

## Instructions
Set OPENAI_API_KEY environment variable as well as GITHUB_TOKEN
You can use a ```.env``` file for that

### Requirements 
Install it with uv package management or with pip
```
uv pip install python-dotenv openai langchain-community langchain-core langchain-openai docarray
```

## Note 
The github models marketplace has changed 
```
import os
from openai import OpenAI

token = os.environ["GITHUB_TOKEN"]
endpoint = "https://models.github.ai/inference"
model_name = "openai/o3-mini"

client = OpenAI(
    base_url=endpoint,
    api_key=token,
)

response = client.chat.completions.create(
    messages=[
        {
            "role": "developer",
            "content": "You are a helpful assistant.",
        },
        {
            "role": "user",
            "content": "What is the capital of France?",
        }
    ],
    model=model_name
)

print(response.choices[0].message.content)

```