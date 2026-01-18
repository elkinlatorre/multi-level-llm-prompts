# AI Prompt Templates – Multi-Level Architecture

## Overview

This repository contains a curated set of reusable prompt templates designed for working with Large Language Models in production and experimental environments.

The prompts are classified into three levels based on:
- Control
- Robustness
- Token cost
- System complexity

The objective is to provide clear trade-offs between **cost and control**, allowing developers and architects to select the appropriate prompt for each use case.

---

## Repository Structure

/prompts
├── prompt_lowLevel.md
├── prompt_midLevel.md
└── prompt_highLevel.md

Each file contains a complete, standalone prompt template that can be used in chat-based workflows or injected directly into API calls.

---

## Prompt Levels

### 1. Low-Level Prompt

**File:** `prompt_lowLevel.md`

**Purpose**
Optimized for minimal cost and fast execution.

**Characteristics**
- Minimal structure
- Generic role definition
- No explicit reasoning control
- Lightweight validation

**Best Suited For**
- Simple Q&A
- Text transformations
- High-volume API requests
- Non-critical tasks

**Advantages**
- Very low token usage
- Fast responses
- Easy to adapt

**Trade-offs**
- Lower determinism
- Higher variability
- Not suitable for complex reasoning

---

### 2. Mid-Level Prompt

**File:** `prompt_midLevel.md`

**Purpose**
Balanced approach between robustness and cost.

**Characteristics**
- Explicit objective and context
- Internal structured reasoning
- Deterministic output expectations
- Basic validation

**Best Suited For**
- Code generation
- Moderate analysis
- Backend LLM services
- Standard production use cases

**Advantages**
- Good consistency
- Reasonable token usage
- Suitable for most real-world systems

**Trade-offs**
- Less control than high-level prompts
- Not ideal for agent orchestration

---

### 3. High-Level Prompt

**File:** `prompt_highLevel.md`

**Purpose**
Maximum control, clarity, and robustness.

**Characteristics**
- Fully structured prompt architecture
- Explicit reasoning configuration
- Clear input/output contracts
- Built-in validation and error handling

**Best Suited For**
- Agent-based systems
- Prompt orchestration
- Complex reasoning workflows
- Critical or auditable systems

**Advantages**
- High determinism
- Strong hallucination mitigation
- Easy integration with orchestration frameworks (e.g. LangChain)

**Trade-offs**
- Higher token usage
- Increased cost per request
- More verbose configuration

---

## How to Use

1. Select the prompt level based on task complexity and cost constraints.
2. Replace placeholders with task-specific values.
3. Use directly in chat or via API calls.
4. Version prompts as part of your system architecture.

---

## Design Philosophy

These prompts are designed as:
- **Contracts**, not conversations
- **Configurable artifacts**, not ad-hoc instructions
- **Scalable building blocks** for AI-powered systems

They intentionally minimize ambiguity and discourage implicit assumptions.

