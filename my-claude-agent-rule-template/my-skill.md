Let me check the skills page for templates and examples:The docs have a **complete example** and **best practices**:

**Template structure** (from docs):
```
my-skill/
├── SKILL.md           # Main instructions (required)
├── template.md        # Template for Claude to fill in
├── examples/
│   └── sample.md      # Example output showing expected format
└── scripts/
    └── validate.sh    # Script Claude can execute
```
Supporting Folders (Optional):

- templates/ or assets/: Formats, boilerplates, or templates for Claude to use.
- references/: Deep-dive data, like a company brand style guide or long documentation, that Claude can look at only if needed.
- scripts/: Executable scripts (Python or Shell) that Claude can run dynamically to do complex math, analyze CSV files, or pull data.

**Best practices:**
- Keep `SKILL.md` under 500 lines; move detailed reference to separate files
- Use `description` in frontmatter so Claude knows when to use it
- Use dynamic context injection (`!`command``) to pull live data
- Reference supporting files from SKILL.md so Claude knows when to load them
- Use `disable-model-invocation: true` for side-effect skills (deploy, commit)
- Use `user-invocable: false` for background knowledge only Claude should see

**Full working example** in the docs: `/summarize-changes` skill that uses `!`git diff HEAD`` to inject live diffs.

See the skills page for the complete frontmatter reference and more examples:
```suggestions
(Create your first skill)[/en/skills#create-your-first-skill]
(Frontmatter reference)[/en/skills#frontmatter-reference]
(Add supporting files)[/en/skills#add-supporting-files]
```