# SKILLS

Create a deep agent, pass in a list of directories containing skills. As the agent starts, it reads through the frontmatter of each SKILL.md file.
When the agent receives a prompt, the agent checks if it can use any skills while fulfilling the prompt. If it finds a matching prompt, it then reviews the rest of the skill files. This pattern of only reviewing the skill information when needed is called progressive disclosure.

---

# Example (skills folder)

You have a skills folder that contains a skill to improve the prompts like system prompt:

![file-structure](/file-structure.png)


---
# What the agent sees?

When skills are configured, a “Skills System” section is injected into the agent’s system prompt. The agent uses this information to follow a three-step process:
* Match — When a user prompt arrives, the agent checks whether any skill’s description matches the task.
* Read — If a skill applies, the agent reads the full SKILL.md file using the path shown in its skills list.
* Execute — The agent follows the skill’s instructions and accesses any supporting files (scripts, templates, reference docs) as needed.
