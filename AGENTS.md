# Repository instructions

This repository provides the MixMatter image-reconstruction skill for Codex.

- When the user requests MixMatter, load `.agents/skills/mixmatter/SKILL.md` and the relevant bundled references.
- Preserve source identity and aspect ratio; add no new text unless the user supplies exact wording.
- Check actual tool availability before promising image output. A loaded skill is not an image model.
- Use an available image editing/generation tool for the attached source image. If none is available, follow the skill's concise prompt-delivery fallback and explain the limitation.
- Do not upload user photographs, generated images, secrets, or API credentials to this repository unless explicitly requested.
- This skill has no runtime package installation or long-running service requirement.
