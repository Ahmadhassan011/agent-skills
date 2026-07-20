---
name: user-manual-generator
description: Authors task-based user manuals, setup guides, and technical procedures following Microsoft and Google style standards. Use when creating step-by-step product documentation, quick-start guides, or troubleshooting procedures.
---

# User Manual Generator Skill

## Triggers & Use Cases
Activate this skill when the user asks to "write a user manual," "create a setup guide," "document an application," or "draft a procedural guide" for hardware, software, or systems.

## Process Workflow

### 1. Discovery & Architecture
Before generating text, prompt the user for missing context or silently infer the following variables:
* **Product Type:** (e.g., SaaS platform, physical hardware, CLI tool, API).
* **Target Audience:** (e.g., non-technical end-users, system administrators, developers).
* **Documentation Type:** (e.g., Quick Start Guide, Comprehensive Manual, Troubleshooting Guide).

### 2. Standard Document Structure
Generate the document using this widely adopted technical writing structure. Omit irrelevant sections based on the product type (e.g., skip physical parts for SaaS apps).

* **Header Block:** Product Name, Document Version/Date.
* **1. Introduction & Scope:** A concise overview of what the product does and the goal of this specific manual.
* **2. Prerequisites & Requirements:** System requirements, account permissions, or physical components required before starting.
* **3. Getting Started / Quick Start (Optional):** The absolute fastest path to initial operational success (the "Hello World" flow).
* **4. Task-Based Procedures:** The core operational instructions. Group them logically by the task the user is trying to accomplish (e.g., "Configuring the Network").
* **5. Troubleshooting:** A symptom-cause-resolution matrix for common issues.
* **6. Support:** Contact information, links to knowledge bases, or community forums.

### 3. Procedural Writing Rules (Industry Standards)
Adhere strictly to the guidelines established by the Microsoft Manual of Style and Google Developer Documentation Style Guide:

* **Goal-First Phrasing:** State the purpose of the action before the action itself. 
  * *Correct:* "To save the document, click **File**."
  * *Incorrect:* "Click **File** to save the document."
* **Conditions First:** If a step is conditional, put the condition at the beginning of the sentence.
  * *Correct:* "If prompted for a password, enter your admin credentials."
* **Imperative Verbs:** Start every numbered action step with a clear command verb (e.g., "Click", "Enter", "Select", "Connect").
* **Atomic Steps & Menu Sequencing:** Describe exactly one action per step. Combine small UI navigation steps using angle brackets.
  * *Correct:* "Select **Settings** > **Network** > **Wi-Fi**."
* **UI Highlighting:** Bold all user interface elements, buttons, menus, and exact text inputs.
* **Front-Loaded Warnings:** Place all safety callouts (`> [!WARNING]`, `> [!CAUTION]`, or `> [!NOTE]`) immediately *before* the step they apply to. Never put a warning after the user has taken the action.
* **Parallelism:** Ensure all items in a bulleted or numbered list use the same grammatical structure (e.g., all starting with verbs, or all noun phrases).

## Anti-Patterns to Avoid
* **The "Do-Everything" Chunk:** Combining setup, usage, and teardown into a single, massive 20-step list. Chunk tasks logically with their own subheadings.
* **Partial Sentence Introductions:** Never introduce a numbered list with a fragmented sentence.
  * *Incorrect:* "To configure the router:" (followed by steps).
  * *Correct:* "To configure the router, follow these steps:"
* **Directional Language:** Avoid using words like "above," "below," or "on the left" to describe UI elements, as interfaces shift based on screen size, updates, or accessibility tools.

## Verification Checklist
Before outputting the manual, ensure:
- [ ] Are headings task-oriented (e.g., "Creating a User Account") rather than feature-oriented (e.g., "The User Screen")?
- [ ] Do all numbered steps start with an imperative verb?
- [ ] Are all warnings and prerequisites placed *before* the relevant action?
- [ ] Are UI elements bolded and navigation paths joined with `>`?