# Contributing

Contributions are welcome: new tools, corrections, broken links, outdated entries, and additional workflows.

---

## Ways to contribute

- **New tool or feed:** Open an [issue](https://github.com/Nervi0z/phishing-analysis-ref/issues/new?template=add-tool.md) with the name, link, licensing model, and a note on its specific defensive value
- **Fix existing entry:** Broken link, outdated info, incorrect description — submit a pull request directly
- **New workflow or technique:** Open an issue first to discuss scope
- **Typos and formatting:** Small fixes are fine as pull requests without an issue

---

## Submitting a pull request

1. Fork the repository
2. Clone your fork:
   ```bash
   git clone https://github.com/YOUR_USERNAME/phishing-analysis-ref.git
   ```
3. Create a descriptive branch:
   ```bash
   git checkout -b add-urlscan-workflow
   git checkout -b fix-phishtank-api-link
   ```
4. Make your changes in `README.md` or the relevant file
5. Commit with [Conventional Commits](https://www.conventionalcommits.org/) prefixes:
   ```bash
   git commit -m "feat: add Unfurl to utility tools section"
   git commit -m "fix: update broken Hybrid Analysis link"
   git commit -m "docs: expand email header analysis workflow"
   ```
6. Push your branch:
   ```bash
   git push origin your-branch-name
   ```
7. Open a pull request against `main`. Reference any related issue with `Closes #NUMBER`

---

## Tool entry format

Use this table structure for new entries:

```markdown
| **Tool Name** | What it does, focused on phishing-specific defensive value | Free/Freemium/Commercial/FOSS | [link](https://...) |
```

Quality criteria:

- Descriptions must be specific to phishing analysis, detection, or prevention use cases
- All links verified before submitting
- Licensing model must be accurate
- Prefer tools that are actively maintained and widely used
- Quality over quantity — one well-documented entry is worth more than three incomplete ones
- No emojis, no generic filler phrases
