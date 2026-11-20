---
name: open-study-materials-research
description: Find reliable, accessible study materials. TODO
compatibility: Requires web search for finding and checking sources. Works as a skill for Codex and Claude Code.
metadata:
  version: "0.0.1"
  language: "en"
  reply_language: "user"
---

# Language

**Always reply in the user's language.**

# Skill Updates

At the beginning of the research, check the [canonical repository](https://github.com/Pavloffm/open-study-materials-research) once for new changes. If an update is available, notify the user and ask: “A skill update is available. Would you like to update?” The user's agent will perform the update using its standard available methods after obtaining consent. While awaiting a response, or if the user declines, continue the research using the current version without repeatedly offering the update in every cycle.

# Autonomous Research

By default, conduct research independently in a prolonged, multi-hour cycle if necessary. Do not end work after each stage with the question “continue?”

1. Ask clarifying questions once, in a single message or through a non-blocking tool, without entering a state of waiting for a response. Immediately work with known facts; mark unknowns as unknown and assumptions as hypotheses. The absence of a response does not block research.

2. Repeat the cycle: select the next verification from the queue → find and read the source → save the artifact and its provenance → update the claims and log → select the next useful step. Do not repeat completed searches without new grounds.

# Workflow

This is a reference route: return to the necessary steps as findings emerge, rather than waiting for the previous stage to be fully completed. Scripts help manage the work; if a tool is unavailable, perform the available part of the work using the agent's capabilities.

## Step 1. Understand the user's goal

1. Formulate the working objective from the request. For a broad task, start with the most reliably known branch and expand the search based on findings.

2. Establish current level, relevant prerequisites, preferred depth, and intended application.

3. Ask up to three essential questions in a single message if needed, but proceed from known information. Label any assumptions.

4. Make a small **topic map**: main concept → subtopics → prerequisite concepts.

## Step 2. Collect materials

1. Search relevant **university courses and lecture notes**, **open textbooks**, **official documentation**, and **problem sets**. Use the [sources index](references/sources/index.md) for discovery guidance.

## Step 3. Generate the report
Fill the existing files in assets/latex/sections/ with the findings, keeping each kind of content in its assigned section:

### `01_content.tex`. Learning content
Write the complete educational content needed to help the reader
understand the topic, not merely a summary of the sources.

1. **Build understanding from the reader's starting point.**
   Identify the prerequisite knowledge and explain unfamiliar
   concepts before using them. Do not assume the reader already
   understands the topic.

2. **Develop intuition before introducing formalism.**
   Explain what the topic is about, why it matters, what problems
   it solves, and the underlying ideas. Use simple explanations
   or analogies where helpful.

3. **Explain concepts progressively.**
   Organize the material into a logical learning sequence, moving
   from foundational ideas to more complex ones. Introduce
   terminology, notation, formulas, and definitions when needed.

4. **Explain both how and why.**
   Do not merely describe procedures or state facts. Explain the
   reasoning behind important steps, relationships, mechanisms,
   and results.

5. **Use examples to develop understanding.**
   Include relevant examples, worked solutions, visualizations,
   comparisons, or practical applications when they improve
   comprehension. Explain intermediate steps rather than skipping
   directly to the result.

6. **Support independent learning.**
   Where appropriate, include exercises, questions, solutions,
   common mistakes, methods for checking answers, and connections
   to related concepts.

7. **Preserve accuracy and source traceability.**
   Base factual and technical claims on reliable inspected sources.
   Cite them with `\cite{...}`. Verify calculations and worked
   examples. Clearly distinguish sourced information from original
   explanatory examples or interpretations.

8. **Adapt the structure to the topic.**
   Choose sections and subsections based on what is necessary to
   teach the subject effectively. Do not force every topic into
   identical headings or include irrelevant material.

The final content should form a coherent learning path that allows
the reader to understand the main concepts, follow the reasoning,
and apply the knowledge at the intended level without constantly
consulting external resources.

### `02_sources.tex`. Sources
Add every inspected source as a bibliography entry. Use citation keys that match the \cite{...} references in the other sections.

After filling the section files, compile the LaTeX document to PDF and check that compilation succeeds.