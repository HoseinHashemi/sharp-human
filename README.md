# Sharp Human

Portable instructions for sharper thinking and more natural writing with AI.

Sharp Human asks an AI collaborator to challenge assumptions, stress-test reasoning, preserve concrete detail, and avoid the polished formulas that make generated prose feel manufactured.

The repository contains one portable, instruction-only Agent Skill: [`SKILL.md`](./SKILL.md).

## Use it in a chat

Download `SKILL.md`, attach it to a conversation in ChatGPT, Claude, or Gemini, and send:

> Read the attached `SKILL.md` and use it as my personal interaction and writing instructions. If this product allows you to install it as a reusable skill or persistent instruction set, do that. If you cannot change my account settings directly, apply it throughout this conversation and tell me the single manual action required to make it persistent. Preserve the original meaning when adapting it to this product.

A chat application may be able to follow the file without being allowed to change account-wide settings. In that case, it should apply the instructions to the current conversation and identify the remaining manual step.

## Install it with a coding agent

Clone or download this repository, open Codex, Claude Code, or Gemini CLI in the repository, and ask:

> Install the `sharp-human` skill from this repository for me globally. Preserve my existing instructions, avoid duplication, and verify that the skill is discoverable after installation.

The agent can select its native user-level skill location. Review any requested file-system changes before approving them.

Gemini CLI can also install the repository directly:

```shell
gemini skills install https://github.com/HoseinHashemi/sharp-human.git
```

## Invoke it

After installation, ask the AI to use `sharp-human` when you want direct critique, stronger reasoning, or natural long-form prose. Products that support automatic skill selection may activate it when the request matches the description in `SKILL.md`.

## Make it yours

Fork the repository and edit `SKILL.md`. Keep the instructions concrete and remove any rule that does not reliably improve the output. A shorter instruction set that changes behaviour is better than a comprehensive one the model ignores.

## License

[MIT](./LICENSE)
