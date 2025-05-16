# Langchain

Langchain is an open soure Frame work for developing applicaton powered by large language mdel.

# Langchain component

* Models
* Prompts
* Chains
* Memory
* Indexes
* Agents

## Model

In  langchain model are the core interface through which you interats wth AI models

## Prompts

Input provide to the LLM

* Dynamic & Reuseable prompt
* Role-Based Prompts
* Few Short prompting

## Chains

To build a pipeline (one outpput can be transfer to another chain), you can create a parallel chain as well as.

## Indexes

Indexes connect your application to external knowledge - such as PDF(doc loader, text splilter, vector space,Retrievel)

## Memory

LLM API calls are stateless

* Conversation BUfferMemory - Send all previous messages to API
* ConversationBufferWindowMomory - last 100/10 interacts store - send previous
* Summarizer-Based Memory - Send summary of chat
* Custom Memory  - User preference or key facts in the memory

## Agents

Autonomous action  (Reason capablility & Tool access)
