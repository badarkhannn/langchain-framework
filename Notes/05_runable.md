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

##### * Task Speific Runnables

✅ **Definition**: These are **core LangChain components** that have been converted into Runnables so they can be used in pipelines.

✅ **Purpose**: Perform **task-specific** operations like LLM calls, prompting, retrieval, etc.

✅ **Examples**:

- `ChatOpenAI` → Runs an LLM model.
- `PromptTemplate` → Formats prompts dynamically.
- `Retriever` → Retrieves relevant documents.

##### * Runable primitives

✅ **Definition**: These are **fundamental building blocks** for structuring execution logic in AI workflows.

✅ **Purpose**: They help **orchestrate execution** by defining how different Runnables interact (sequentially, in parallel, conditionally, etc.).

✅ **Examples**:

- `RunnableSequence` → Runs steps in **order** (`|` operator).
- `RunnableParallel` → Runs multiple steps **simultaneously**.
- `RunnableMap` → Maps the same input across multiple functions.
- `RunnableBranch` → Implements **conditional execution** (if-else logic).
- `RunnableLambda` → Wraps **custom Python functions** into Runnables.
- `RunnablePassthrough` → Just forwards input as output (acts as a placeholder).

#### RunableSequence

Runnable squence is a seuqnetial chain of the runable in langchain that execute each stp one after another passnig thoutput of one stp as the input to th text.

It is usefull when you need to ompose multiple runables together in a structured workflow.

#### RunableParalle

RunableParallel is a runable primitive that allows multiles runables to execute in parelel. Each runables the same input and process it indenpendenty producing a dictionary of output.

#### Runablepassthrough

Runablepassthrough is a special Runable primitive that simply return input as output without modifiying it.

#### Runableambda

RunableLambda is a runable primitive that alllow you to apply custom python functions within an AI pipeline. 

It acts as a middleware betweeb different AI component, enabling preprocessing transformation, API calls, filtering and post-processing ni a langchain workflow.

#### RunableBranch

RunableBranch is a control compoent in langchain that alllow you to conditionlally route input data to a different chain or runables based on custom logic.

It function like an if/elif/else bock for chain - where you define a set of condition functions each associated with a runable (e.g LLM call, prompt chain or tool). The first matching condition is executed if no conditio matches a default runable is used if provided.

#### LCEL

 | | | | | | | | you can use this pipe for the decare the runable sequence.
