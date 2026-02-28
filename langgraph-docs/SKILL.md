---
name: langgraph-docs
description: Access up-to-date LangGraph Python documentation to provide accurate implementation guidance. Use when requests involve LangGraph concepts, APIs, or implementation questions including (1) building agents with LangGraph, (2) creating state graphs and workflows, (3) using LangGraph checkpointing and persistence, (4) implementing human-in-the-loop patterns, (5) deploying LangGraph applications, or (6) any LangGraph-specific questions requiring current documentation.
---

# LangGraph Documentation

## Overview

This skill provides access to the official LangGraph Python documentation to answer questions and guide implementation with accurate, up-to-date information.

## Workflow

### 1. Fetch the Documentation Index

Use the WebFetch tool to read the documentation index:

```
WebFetch with url="https://docs.langchain.com/llms.txt" and prompt="Extract the full list of documentation URLs with their descriptions"
```

This index provides a structured list of all available LangGraph documentation with descriptions.

### 2. Select Relevant Documentation

Based on the user's question, identify 2-4 most relevant documentation URLs from the index. Prioritize:

- **How-to guides** for implementation questions (e.g., "How do I create a checkpointer?")
- **Concept pages** for understanding questions (e.g., "What is a state graph?")
- **Tutorials** for end-to-end examples (e.g., "Build a chatbot with LangGraph")
- **API reference** for detailed API information (e.g., "StateGraph parameters")

### 3. Fetch Selected Documentation

Use the WebFetch tool to read each selected documentation URL:

```
WebFetch with url="[selected-doc-url]" and prompt="Extract all content including code examples, explanations, and API details"
```

Read 2-4 documentation pages to gather comprehensive context.

### 4. Provide Accurate Guidance

After reading the documentation:

- Answer the user's question with information directly from the documentation
- Include code examples from the documentation when relevant
- Cite specific documentation URLs for reference
- Recommend additional documentation pages if the user needs more context

## Tips

- **Multiple topics**: If the question spans multiple topics (e.g., "agents with persistence"), fetch documentation for each topic
- **Code examples**: Always include working code examples from the documentation
- **Version compatibility**: Check if the documentation mentions version-specific behavior
- **Related concepts**: Suggest related documentation that might be helpful for the user's broader goals
