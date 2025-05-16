## Top few chains in langchain

| Chain Name                                             | Description                                                          |
| ------------------------------------------------------ | -------------------------------------------------------------------- |
| **LLMChain**                                     | Basic chain that calls an LLM with a prompt template.                |
| **SequentialChain**                              | Chains multiple LLM calls in a specific sequence.                    |
| **SimpleSequentialChain**                        | A simplified version of SequentialChain for easier use.              |
| **ConversationalRetrievalChain**                 | Handles conversational Q&A with memory and retrieval.                |
| **RetrievalQA**                                  | Fetches relevant documents and uses an LLM for question-answering.   |
| **RouterChain**                                  | Directs user queries to different chains based on intent.            |
| **MultiPromptChain**                             | Uses different prompts for different user intents dynamically.       |
| **HydeChain (Hypothetical Document Embeddings)** | Generates hypothetical answers to improve document retrieval.        |
| **AgentExecutorChain**                           | Orchestrates different tools and actions dynamically using an agent. |
| **SQLDatabaseChain**                             | Connects to SQL databases and answers natural language queries.      |

## Runable ?

It is the unit of the work (like you can give input and then it will give output, A common interface of the runable)
