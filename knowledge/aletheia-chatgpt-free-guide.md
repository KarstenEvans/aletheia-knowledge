---
title: ChatGPT Free without the faff
collection: Aletheia Secret Windows
section: AI / BEGINNER GUIDES
status: current-guidance
last_checked: 2026-09-23
resource_url: https://karstenevans.github.io/aletheia-knowledge/resources/aletheia-chatgpt-free-guide.htm
---

# ChatGPT Free without the faff
## A practical guide to cleaning, customising and actually using your free AI

ChatGPT Free is useful without paying for a subscription. The trick is to choose the right mode, give it clear instructions and keep your own copy of anything important. This guide works on a Windows PC as well as supported mobile devices. Exact controls can change; check the official links at the end if a menu has moved.

## 1. What you can do for free

- Chat normally, request summaries, ask follow-up questions and create or revise writing.
- Search the live web and request source links when information may have changed.
- Upload some files or images, analyse data and generate images, subject to separate usage limits.
- Use limited Voice, Custom Instructions, Memory and Projects. Free Projects currently hold up to five files each; uploads and some other tools have separate limits.
- Try Think for a difficult question on supported mobile apps, or on the web if the control has reached your account.
- Use existing GPTs, but personal Free accounts cannot currently create or publish new GPTs.
- Keep reference files in Library (currently 500 MB on Free). An item in Library is not automatically loaded into every chat or Project.

Free offers generally unlimited everyday text chat, subject to abuse safeguards, while uploads, data analysis, images and Voice have separate quotas. The current Free model is GPT-5.6 Luna. Free does not mean that every tool is unlimited or available in every region. A convincing answer is not proof that the AI searched the web or read the file you had in mind.

## 2. Use the right microphone: Voice versus Dictation

**Voice:** Choose a live spoken conversation for company, brainstorming, language practice and discussing ideas. ChatGPT's Live mode can search the web and use memory where available, but uses a different conversation-oriented model (GPT-Live-1 mini on Free). A spoken answer and its transcript may be less convenient when you need exact quotations, tables, sources or a reusable document. Live can accept text and images in the same chat when enabled, but cannot currently retrieve files directly from your ChatGPT Library.

**Voice options:** Under Settings > Voice, your account may offer Live (natural interruption/back-and-forth), Standard (transcribes each turn before answering) or Advanced (older real-time experience with mobile video/screen sharing for eligible subscribers). Available options, limits and controls depend on your account; Live does not support video or screen sharing.

**Dictation:** For research, troubleshooting, calculations, comparisons and longer jobs, tap the microphone that converts your speech into editable text in the ordinary message composer. Read the transcription, correct errors and send it. You can still speak your question without staying in live Voice.

**Listen afterwards:** Where your app offers Read Aloud or a speaker action on a finished answer, use it to listen to the written result. You keep the table and citations on the screen.

This is a workflow recommendation, not a claim that Voice cannot research. For important questions, a written answer is usually easier to examine and verify. Voice transcripts are not verbatim records; check any quoted speech, names or figures.

**Audio privacy difference:** Live and Advanced conversation clips are generally retained for 30 days. Dictation audio is retained with the chat while it remains in your history; after deleting the chat, associated audio is generally removed within 30 days, subject to stated exceptions. Review the separate audio/video sharing toggles in Data controls.

## 3. Clean up incorrect assumptions

- Ask: 'What do you currently remember about my preferences for this subject? Label any guesses.'
- Open Settings > Personalization > Memory. Review the Memory summary and its Manage controls if they are available for your account; the summary is not necessarily a full inventory.
- If Sources appear beneath a personalised answer, inspect the referenced chat, saved item, Library file or connected app to understand where an assumption came from.
- Correct the summary when it contains an outdated assumption. For complete removal of an unwanted detail, also delete the source chat and every other source that contains it, such as files or connected-app content.
- Use Settings > Data controls if you want to export your account data or stop your eligible new conversations being used to improve models. Turning off training is a separate decision from enabling or deleting Memory.
- Temporary Chat is useful for one-off subjects that should not enter ordinary chat history or create new memories. Choose whether it should use existing personalisation at the start if your app offers that choice.

Turning Memory off is not the same as deleting chat history. Turning model improvement off is not the same as deleting your account or files.

## 4. Put short rules in Custom Instructions

Open Settings > Personalization or Customize ChatGPT and find the Custom Instructions controls. They are available on Free accounts, with a **1,500-character limit** for Free and Go. Make sure Enable customization is on. Updates apply immediately, but will not erase references to older instructions from earlier conversations. Menu wording may differ between desktop and mobile. A third-party plugin you use may receive relevant instructions, so avoid putting secrets in the global profile.

A practical short baseline to paste:

```text
Lead with the answer and complete the task when you have enough information.
Be concise, plain-spoken and precise. Avoid filler.
Do not invent facts, sources, links, actions or successful file saves.
Distinguish verified facts, interpretation, assumptions and unknowns.
For current information, use web search if available and cite dated sources.
Challenge my assumptions where the evidence disagrees.
Use clear tables for comparisons, and explain technical steps in ordinary language.
Ask only necessary questions; seek approval before irreversible changes.
Use light, dry humour only when appropriate.
```

Instructions help, but they are not a guarantee. They cannot create a tool your account does not have, force a model to remember everything, or override the platform's safety rules.

## 5. Give continuing work its own free Project

Create a Project called Aletheia, Family History, House Repairs or anything meaningful. Put its durable working rules in Project instructions and add only relevant files. Free users can create unlimited Projects, with up to five files per Project and separate upload-rate limits. **Project instructions override global Custom Instructions inside that Project.**

In Project settings, where available, choose Default or Project-only memory according to whether the project should draw on context outside itself. Shared Projects automatically use Project-only memory; permitted collaborators can see the shared chats, files and instructions. Free owners can currently share a Project with up to five collaborators. Before sharing, inspect every file and the project's permissions. You can also move eligible old chats into a Project or save a useful ChatGPT answer as a Project source.

For Aletheia AI Easy, use the small `aletheia-bootstrap.md` in the Project instructions, then add your reviewed `aletheia-memory.md` as a Project file if you want portable context. The bootstrap should offer Aletheia's evidence/continuity rules, optional Thalia humour, and explicit choices for other apps. It must not silently enable them or claim to have saved data that was only displayed.

Keep your own copies in a Documents/Aletheia folder. The provider's memory and your portable file are different things; review changes before replacing your file.

## 6. Eleven useful prompt shortcuts

These are **ordinary instructions**, not hidden ChatGPT commands. Speak them, paste them or add the ones you use most to Project instructions.

- **EXECUTE:** 'Complete the task now using the tools actually available. State what you completed and what you could not.'
- **NO FAFF:** 'Start with the result. Cut introductions, flattery and repetition.'
- **ELI5 or ELI10:** 'Explain this for a five-year-old or ten-year-old without changing the underlying facts.'
- **SEARCH CURRENT:** 'Search the current web, give primary sources and dates, and identify anything unconfirmed.'
- **SOURCE CHECK:** 'List every important factual claim, give the evidence for each and mark unsupported claims.'
- **TRUTH TEST:** 'Challenge the answer, distinguish fact from inference, and tell me what would change the conclusion.'
- **COMPARE:** 'Show options in a table with evidence, limitations, cost and relevant trade-offs.'
- **ONE QUESTION:** 'Ask only one essential clarifying question, otherwise proceed using stated assumptions.'
- **STEP BY STEP:** 'Give numbered steps and identify anything irreversible before suggesting it.'
- **CHECKPOINT:** 'Summarise current goal, completed work, verified sources, corrections and next action.'
- **HANDOVER:** 'Write a portable Markdown brief for another AI, including unknowns and links to files actually seen.'

For questions that need serious work, combine instructions: 'EXECUTE + SEARCH CURRENT + SOURCE CHECK + TABLE'. Actual built-in navigation includes the Search tool, available from the tools menu or, on supported interfaces, by typing `/` and selecting Search. This is separate from the sidebar search for your own chats, Projects and files. The words are shorthand for the explicit instructions above, not a secret mode.

## 7. What to do if the answer sounds confident but is wrong

Ask the AI to show which claims came from its built-in knowledge, which were checked against a source and which remain uncertain. Recheck a surprising result against an official source. For a website, ask it to show the exact page it opened; for a file, ask it to identify the uploaded filename and the relevant passage. A model that never accessed a page cannot honestly say it inspected it.

Do not upload passwords, one-time codes, recovery keys or private workplace records into a general bootstrap. For health, legal, financial and safety-critical decisions, use appropriate professional or primary-source confirmation.

## 8. A privacy checklist worth doing once

The controls are separate. Choose the one that matches what you want to happen:

- **Stop eligible new chat content being used to improve models:** Settings > Data controls > Improve the model for everyone, then turn it off. Your existing chats remain in history.
- **Try something without ordinary chat history or new memories:** Start a Temporary Chat. Before it begins, choose whether it may use your existing personalization if that option appears. Saving a temporary conversation makes it a regular chat.
- **Stop an AI assumption being repeated:** Correct your Memory summary or ask ChatGPT not to mention the information again. This does not itself remove the original source.
- **Remove sensitive information from remembered context:** Update the Memory summary and delete relevant original chats (including archived chats), Library files and connected-app sources. Allow for propagation time and platform retention exceptions.
- **Check what else you have shared:** Review existing shared links, Project collaborators and file permissions. Request a data export before irreversible cleanup if you may need a personal backup.

Be aware that ChatGPT Search can rewrite a query and send search terms to partner search providers, sometimes using a general location or relevant Memory preferences. Keep unnecessary personal identifiers out of external search requests.

## 9. The Aletheia AI Easy three-step setup

1. **Personalise:** Copy a short universal profile into Custom Instructions. On Free, keep it within 1,500 characters; let the local setup page count and display its size.
2. **Organise:** Create an Aletheia Project and add the full Project-specific bootstrap to Project instructions. Add a reviewed `aletheia-memory.md` only if wanted, subject to the Free five-file limit.
3. **Take control:** Review Data controls, select Project memory intentionally, and store your own bootstrap and portable memory in your chosen Documents/Aletheia folder. Use CHECKPOINT and HANDOVER to move work between AIs rather than relying on invisible model memory.

Aletheia Protocol provides evidence discipline and portable context; Thalia is an optional tone/humour layer. Neither protocol can grant missing tools, change platform memory settings, guarantee accurate research or silently save a file.

## Official OpenAI guidance

- ChatGPT Free FAQ: https://help.openai.com/en/articles/9275245-chatgpt-free-tier-faq
- ChatGPT Voice: https://help.openai.com/en/articles/20001274
- Voice Dictation: https://help.openai.com/en/articles/12168547
- Custom Instructions: https://help.openai.com/en/articles/8096356
- Memory: https://help.openai.com/en/articles/8590148
- Projects: https://help.openai.com/en/articles/10169521
- ChatGPT Search: https://help.openai.com/en/articles/9237897
- Data controls: https://help.openai.com/en/articles/7730893
