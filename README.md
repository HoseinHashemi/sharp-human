# Sharp Human

Two portable skills for sharper thinking, more natural writing, and independent prose auditing with AI.

[`sharp-human`](./SKILL.md) asks an AI collaborator to challenge assumptions, stress-test reasoning, preserve concrete detail, and avoid the polished formulas that make generated prose feel manufactured. [`sharp-human-auditor`](./sharp-human-auditor/SKILL.md) independently checks finished text against those rules.

## Choose how to use it

### Make it global

Copy everything in [`GLOBAL-INSTRUCTIONS.md`](./GLOBAL-INSTRUCTIONS.md) into the account-level instruction setting for your chat application:

- **ChatGPT:** Settings → Personalization → Custom Instructions
- **Claude:** Settings → Instructions for Claude
- **Gemini:** Settings & help → Personal Intelligence → Instructions for Gemini

These account-level settings apply the writing instructions across ordinary conversations. The auditor remains separate so it can be invoked deliberately in a fresh conversation.

### Install it as a skill

Clone or download this repository, open Codex, Claude Code, or Gemini CLI in it, and ask:

> Install both Agent Skills from this repository globally: `sharp-human` from the root `SKILL.md`, and `sharp-human-auditor` from `sharp-human-auditor/SKILL.md`. Preserve my existing instructions, avoid duplication, and verify that both skills are discoverable after installation.

The agent can select its native user-level skill location. Some installers recognise only the skill at the repository root, so verify that both skill names are available after installation. Review any requested file-system changes before approving them.

### Use either skill in one chat without installing it

For writing or critique, attach the root [`SKILL.md`](./SKILL.md) and send:

> Read the attached `SKILL.md` and use it as my interaction and writing instructions for this conversation. Preserve the original meaning when adapting it to this product.

For auditing, start a fresh conversation, attach [`sharp-human-auditor/SKILL.md`](./sharp-human-auditor/SKILL.md), and send:

> Use the attached `sharp-human-auditor` skill to audit the text below. Highlight any remaining formulaic or AI-like patterns, explain which instruction each one violates, and stop before rewriting.

## Invoke it

After installation, ask the AI to use `sharp-human` when you want direct critique, stronger reasoning, or natural long-form prose. Invoke `sharp-human-auditor` explicitly when you want an independent review of finished text.

## Audit a draft or AI response

Run the auditor in a new conversation or a separate agent when possible. A separate skill invoked near the end of the same crowded conversation still shares that conversation's context limitations.

Paste or attach the text and ask:

> Use `sharp-human-auditor` to audit the text below. Highlight any remaining formulaic or AI-like patterns, explain which instruction each one violates, and stop before rewriting.

Include the original request if you also want the auditor to verify task-specific compliance. Without it, the auditor checks only the Sharp Human writing rules.

The audit returns a Pass, Partial, or Fail verdict and quotes the exact passages that need attention. If it finds genuine problems, it asks whether you want them revised. If you request an audit and revision in the same prompt, it can do both without pausing. For a document that approaches the model's context limit, audit it in sections and consolidate the findings afterward.

This is a style and instruction-compliance check, not an AI detector. A phrase that resembles a common AI pattern is not evidence that AI wrote the text.

## Make it yours

Fork the repository and edit [`SKILL.md`](./SKILL.md) for writing behaviour or [`sharp-human-auditor/SKILL.md`](./sharp-human-auditor/SKILL.md) for audit behaviour. If a change should also affect account-wide chat instructions, update [`GLOBAL-INSTRUCTIONS.md`](./GLOBAL-INSTRUCTIONS.md) with the compact equivalent. Keep shared rules aligned across the two skills. A shorter instruction set that changes behaviour is better than a comprehensive one the model ignores.

## License

[MIT](./LICENSE)
