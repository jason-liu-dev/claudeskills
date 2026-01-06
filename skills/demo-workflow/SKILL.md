---
name: demo-workflow
description: A multi-step workflow skill to demonstrate complex instruction following. It processes input, generates creative content, and saves the result to a file.
---

# Demo Workflow Skill

## Overview
This skill demonstrates a 3-step process to verify the model's ability to follow sequential instructions and use tools.

## Instructions
When the user provides a topic or a sentence and asks to "run the demo", "process this", or "test workflow":

### Step 1: Analysis & Extraction
1.  Analyze the user's input.
2.  Extract the **Main Topic**.
3.  Identify **3 Key Keywords** related to the topic.
4.  *Output*: Print the Main Topic and Keywords to the chat.

### Step 2: Creative Expansion
1.  Write a short, science-fiction themed micro-story (approx. 100 words) incorporating the Main Topic and all 3 Keywords.
2.  The story must feature a character named "Captain Glm".
3.  *Output*: Print the story to the chat.

### Step 3: Archival (File Creation)
1.  Create a Markdown file named `demo_result.md` in the `skills/demo-workflow/` directory.
2.  The file content MUST follow this format:
    ```markdown
    # Demo Workflow Result
    **Date**: [Current Date]
    **Input Topic**: [Main Topic]

    ## Keywords
    - [Keyword 1]
    - [Keyword 2]
    - [Keyword 3]

    ## The Story
    [The story generated in Step 2]
    ```
3.  Use the `write_file` tool to save this file.
4.  *Final Output*: Confirm to the user that the file has been created and provide the full path.

## Constraints
- You MUST perform all 3 steps in order.
- You MUST use the `write_file` tool for Step 3.
- Do not skip the file creation step.
