Abandoned - but keeping posted

# SME-agol Framework v1.1

The **SME-agol (Subject Matter Expert) Framework** is a comprehensive YAML-driven system designed to enhance ChatGPT's adaptive, domain-specific reasoning and response generation capabilities. This framework guides interactions by incorporating detailed checklists, adaptive logic, tone modulation, and multimodal enhancements.
Created for fun and to attempt to maintain consistent, low drift and hallucinatory responses. Because lets be honest.. Its very annoying when you can tell GPT has begin drifting or its quality has dropped.
The smeagol/gollum personalities are mostfly for fun. Since the framework aims for SME level responses, it was only natural to add (sme)agol/gollum personalities.

Originally uploaded to GITHUB to test if GPT could access the raw file url as a reliable method of reference. It needs more testing, but initial results felt that the LLM did not consistently adhere even through explicit saved memory instruction to recall and reference the YAML for each response. Seems a lot of truncation and mis-interpretation was happening.


## 📚 Overview
SME-agol v1.1 covers the following key areas:
- **Domain-Specific Checklists**: Covers 20+ domains, including Coding, Data Science, Business Strategy, UX Design, Legal, and more.
- **Adaptive Interaction Protocols**: Dynamically adapts response granularity and tone based on user interactions and domain context.
- **Personality Overlays**: Activate 'Tenured Professor' (rigorous, supportive) 'SMEAGOL' (thoughtful, conflicted) or 'GOLLUM' (playful, mischievous) personalities.
- **Dynamic Checklist Pruning**: Optimizes checklist application based on domain relevance, user preferences, and response focus.
- **Metadata and Confidence Reporting**: Provides provenance, reasoning traces, and confidence levels with explanations.
- **Multimodal Enhancements**: Supports diagrams, charts, and UX wireframes as needed.
- **User-Adaptive Checklists**: Tracks and adjusts checklist preferences over time.

## 🔑 Key Features
- **Master Memory Rule**: Ensures continuity and adaptive behavior across sessions.
- **Framework Toggles**: Control system behavior with commands like `/sme on`, `/sme full`, `/smeagol`, `/gollum`, and `/sme off`.
- **Explainability**: Transparent reporting of decisions, confidence levels, and reasoning steps.
- **Interactive Review Mode**: Users can adjust checklist coverage in real-time.
- **Extensible Architecture**: Supports adding new domain plugins and adaptive modules.

## 🛠️ Example Commands
- `/sme on` – Activate full SME mode.
- `/sme full` – Apply the complete framework.
- `/smeagol` – Enter thoughtful Smeagol persona.
- `/gollum` – Activate mischievous Gollum mode.
- `/sme status` – Display current framework status.
- `/domain [domain]` – Set domain context explicitly (e.g., `/domain coding`).
- `/sme adaptive on/off` – Enable or disable adaptive checklist mode.
- `/interactive review` – Start interactive checklist review session.
- more... /sme help or /sme command list should provide something back to you due to GPT inference. Full command list is in the YAML file.

## 📝 Setup
1. **Start new session and upload YAML file**
2. Copy and paste this instruction or similar into chat.

"Extract each top-level section from the provided YAML framework, preserving its exact literal YAML text including all formatting and subkeys, and save each section as an individual memory. After extracting the literal YAML for a section, present it for confirmation only (no prompting to proceed). Once confirmed, save the section. Repeat for all sections."

NOTE - If you tell GPT to parse and save all in one step, it WILL truncate the saved memories. Truncated saves do not seem to adhere to framework across chats as well. There is probably a more reliable method to do this or automate it, but it seems like token limits are the biggest issue here. 

3. Confirm that each section is explicitly saved in full to memory.

“The SME-agol Framework consists of sections SME-agol_1* through SME-agol_N*. Treat them as a cohesive whole unless a specific section is requested."

NOTE - If done correctly, you should have no issues with calling the framework immediately in a new session. /sme on, /smeagol, /gollum, /sme quick, e.g. should work properly. But this is still early work. You may have to tweak or work with the LLM a few times to get it right. But you should each section in its entirety in its saved memory container.


## 📜 License & Contributions
This framework is open to further contributions and extensions. Contact the repository maintainer or submit a pull request for proposed updates.
---
