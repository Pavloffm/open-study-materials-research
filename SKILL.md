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

1. 01_preliminary_knowledge.tex — Explain what the reader should already know, essential background, and notation or assumptions needed to follow the report.

2. 02_definitions.tex — Add precise, source-backed definitions of the key terms.

3. 03_core_explanations.tex — Explain the main ideas, mechanisms, reasoning, and limitations.

4. 04_examples_applications.tex — Provide worked examples and practical applications that connect to the definitions and explanations.

5. 05_gaps_next_steps.tex — Record important gaps in the reviewed material, related topics for further study, and unresolved questions.

6. 06_sources.tex — Add every inspected source as a bibliography entry. Use citation keys that match the \cite{...} references in the other sections.

After filling the section files, compile the LaTeX document to PDF and check that compilation succeeds.