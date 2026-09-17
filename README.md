# Sharp Human

Portable instructions for sharper thinking and more natural writing with AI.

Sharp Human asks an AI collaborator to challenge assumptions, stress-test reasoning, preserve concrete detail, and avoid the polished formulas that make generated prose feel manufactured.

## Choose how to use it

### Make it global

Copy everything in [`GLOBAL-INSTRUCTIONS.md`](./GLOBAL-INSTRUCTIONS.md) into the account-level instruction setting for your chat application:

- **ChatGPT:** Settings → Personalization → Custom Instructions
- **Claude:** Settings → Instructions for Claude
- **Gemini:** Settings & help → Personal Intelligence → Instructions for Gemini

These account-level settings are the reliable way to apply Sharp Human across ordinary conversations. Attaching a file to one conversation does not necessarily make it global.

### Install it as a skill

The complete portable Agent Skill is defined in [`SKILL.md`](./SKILL.md). Clone or download this repository, open Codex, Claude Code, or Gemini CLI in it, and ask:

> Install the `sharp-human` skill from this repository for me globally. Preserve my existing instructions, avoid duplication, and verify that the skill is discoverable after installation.

The agent can select its native user-level skill location. Review any requested file-system changes before approving them.

Gemini CLI can also install the repository directly:

```shell
gemini skills install https://github.com/HoseinHashemi/sharp-human.git
```

### Use it in one chat without installing it

Download `SKILL.md`, attach it to a conversation in ChatGPT, Claude, or Gemini, and send:

> Read the attached `SKILL.md` and use it as my interaction and writing instructions for this conversation. Preserve the original meaning when adapting it to this product.

## Invoke it

After installation, ask the AI to use `sharp-human` when you want direct critique, stronger reasoning, or natural long-form prose. Products that support automatic skill selection may activate it when the request matches the description in `SKILL.md`.

## Make it yours

Fork the repository and edit `SKILL.md`. If the change should also affect account-wide chat instructions, update `GLOBAL-INSTRUCTIONS.md` with the compact equivalent. Keep the instructions concrete and remove any rule that does not reliably improve the output. A shorter instruction set that changes behaviour is better than a comprehensive one the model ignores.

## License

[MIT](./LICENSE)
