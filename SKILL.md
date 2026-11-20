---
name: open-study-materials-research
description: TODO
compatibility: TODO
metadata:
  version: "0.0.1"
  language: "en"
  reply_language: "user"
---

# Language

**Always reply in the user's language.**

# Skill Updates

At the beginning of the research, check the [canonical repository](TODO) once for new changes. If an update is available, notify the user and ask: “A skill update is available. Would you like to update?” The user's agent will perform the update using its standard available methods after obtaining consent. While awaiting a response, or if the user declines, continue the research using the current version without repeatedly offering the update in every cycle.

# **Autonomous Research**

By default, conduct research independently in a prolonged, multi-hour cycle if necessary. Do not end work after each stage with the question “continue?”

1\. Ask clarifying questions once, in a single message or through a non-blocking tool, without entering a state of waiting for a response. Immediately work with known facts; mark unknowns as unknown and assumptions as hypotheses. The absence of a response does not block research.

2\. Repeat the cycle: select the next verification from the queue → find and read the source → save the artifact and its provenance → update the claims and log → select the next useful step. Do not repeat completed searches without new grounds.

# **Workflow**

This is a reference route: return to the necessary steps as findings emerge, rather than waiting for the previous stage to be fully completed. Scripts help manage the work; if a tool is unavailable, perform the available part of the work using the agent's capabilities.

## **Step 1. Define the task and permissible scope**

1\. Formulate the working objective from the request. For a broad task, start with the most reliably known branch and expand the search based on findings.
