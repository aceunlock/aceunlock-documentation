# AceUnlock Documentation

This repository contains the complete documentation for AceUnlock, structured to be both human-readable and LLM-friendly for chatbot support.

## Documentation Structure

```
docs/
├── getting-started/     # Onboarding guides for new users
├── features/           # Detailed feature documentation
├── use-cases/          # Industry/scenario-specific guides
├── api/               # API documentation (if applicable)
├── troubleshooting/   # Common issues and solutions
└── faq/               # Frequently asked questions
```

## How to Contribute

1. Keep markdown files focused on a single topic
2. Use clear, descriptive filenames (e.g., `password-reset.md`, not `guide1.md`)
3. Include frontmatter metadata in each file
4. Cross-link related documents
5. Update the relevant index file when adding new docs

## Frontmatter Format

Each markdown file should include frontmatter:

```yaml
---
title: "Your Document Title"
description: "Brief description for search"
category: "getting-started|features|use-cases|etc"
tags: ["tag1", "tag2"]
last_updated: "2024-01-15"
---
```

## Local Preview

To preview the documentation locally:
- Use any markdown editor (VS Code, Cursor, Typora)
- Or run a local docs server (instructions below)

## License

[Your License Here]
