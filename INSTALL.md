# LangGraph Documentation Skill - Installation Guide

## Installation

### Method 1: Using Claude Code CLI

```bash
# Install the skill
claude skill install langgraph-docs.skill

# Verify installation
claude skill list
```

### Method 2: Manual Installation

1. Copy the `langgraph-docs.skill` file to your Claude skills directory:
   ```bash
   cp langgraph-docs.skill ~/.claude/skills/
   ```

2. Extract the skill (Claude Code does this automatically, but for manual setup):
   ```bash
   cd ~/.claude/skills
   unzip langgraph-docs.skill -d langgraph-docs
   ```

## Usage

Once installed, Claude will automatically use this skill when you ask LangGraph-related questions.

### Example Queries

**Basic concept questions:**
```
"What is a state graph in LangGraph?"
"How does checkpointing work in LangGraph?"
```

**Implementation questions:**
```
"How do I create a LangGraph agent with memory?"
"Show me how to implement human-in-the-loop with LangGraph"
```

**Advanced topics:**
```
"How do I deploy a LangGraph application?"
"What's the best way to handle errors in LangGraph workflows?"
```

## How It Works

When you ask a LangGraph question, the skill:

1. Fetches the LangGraph documentation index from https://docs.langchain.com/llms.txt
2. Selects the most relevant 2-4 documentation pages
3. Retrieves the full content from those pages
4. Provides accurate answers with code examples and references

## Updating

To update the skill to a newer version:

```bash
# Remove old version
claude skill remove langgraph-docs

# Install new version
claude skill install langgraph-docs.skill
```

## Troubleshooting

**Skill not triggering:**
- Ensure your question explicitly mentions "LangGraph"
- Try more specific questions like "How do I use LangGraph to..."

**Documentation not loading:**
- Verify internet connectivity
- Check that https://docs.langchain.com/ is accessible

## Uninstallation

```bash
claude skill remove langgraph-docs
```
