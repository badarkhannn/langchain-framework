# Structured Output

In langchain structured output refer to the pratice of having langiage model return responses in a well defined data format (for example, JSON) rather than free-form format make the model output easir to parso work with programmaticall.

***i.e* **

JSON format

## Why do we need structured Data

* Data Extraction
* API Building
* Agents

**with_structured_output -** are the function to get the ouput in the structured

**output_parsiers** - same as above - but it's used when model don't have a model for the structured output

### Type of output

* Typedir
* Pydantic
* Json_schema

### Typedict

Typedict is a way to define a dictonary in python where you specifity what keys and values should exist. It help ensuse that your dictonary follow a spacfic structure

### Pydantic

Pydantic is a data validation and data parsing libraary for python, it ensure that the data you work with is correct structured and type-safe.

**i.e** It's mostly used in the API

When to use what?

✅ **Use `TypedDict` if:**

- You **only need type hints** (basic structure enforcement).
- You **don’t need validation** (e.g., checking numbers are positive).
- You **trust the LLM** to return correct data.

---

✅ **Use `Pydantic` if:**

- You need **data validation** (e.g., sentiment must be `"positive"`, `"neutral"`, or `"negative"`).
- You need **default values** if the LLM **misses fields**.
- You want **automatic type conversion** (e.g., `"100"` → `100`).

---

✅ **Use `JSON Schema` if:**

- You **don’t want to import extra Python libraries** (Pydantic).
- You need **validation but don’t need Python objects**.
- You want to define structure **in a standard JSON format**.
- 

| Feature                      | TypedDict ✅ | Pydantic ✏️ | JSON Schema 🌐 |
| ---------------------------- | ------------ | ------------- | -------------- |
| Basic structure              | ✅           | ✅            | ✅             |
| Type enforcement             | ✅           | ✅            | ✅             |
| Data validation              | ❌           | ✅            | ✅             |
| Default values               | ❌           | ✅            | ❌             |
| Automatic conversion         | ❌           | ✅            | ❌             |
| Cross-language compatibility | ❌           | ❌            | ✅             |

## Output parsers

Output parsers in Langchain help convert raw LLM responses into structured format like JSON,CSV, Pydantic models, and more. They ensure conistency, Validation and ease of use in appliation.

* str output parser
* JSON output parser
* pydantic parser

### Str output parser

The stroutput parser is the simplest output parser in langchain. It is used to parse the output of a language Model (LLM) and return it as a plain string.

### Strutured Output parser

Structuredoutput parser is an output in langchani that helps extract JSON data from the LLM responses based on predefined field schemas.

It workds by definig a list of field (responseScheme) that the model shoudl retuen, ensurig the output follow a structured format.

## What is `PydanticOutputParser` in LangChain?

`PydanticOutputParser` is a **structured output parser** in LangChain that uses **Pydantic models** to enforce **schema validation** when processing LLM responses.

## ❓ Why Use `PydanticOutputParser`?

- ✅ **Strict Schema Enforcement** — Ensures that LLM responses follow a well-defined structure.
- ✅ **Type Safety** — Automatically converts LLM outputs into Python objects.
- ✅ **Easy Validation** — Uses Pydantic's built-in validation to catch incorrect or missing data.
- ✅ **Seamless Integration** — Works well with other LangChain components.
