# Contributing to AceUnlock Documentation

Thank you for contributing! This guide will help you maintain consistency and quality across our documentation.

## Quick Reference

- **Template**: See [TEMPLATE.md](./TEMPLATE.md) for the standard document structure
- **Setup**: See [SETUP-GUIDE.md](./SETUP-GUIDE.md) for detailed setup instructions
- **Style**: See style guide below

## Before You Start

1. Pull latest changes: `git pull`
2. Create a branch for your changes: `git checkout -b your-branch-name`
3. Use the template for new documents: Copy `TEMPLATE.md`

## Documentation Standards

### File Naming

✅ **Good**:
- `password-reset.md`
- `sso-configuration.md`
- `api-authentication.md`

❌ **Bad**:
- `doc1.md`
- `new-guide.md`
- `PWReset.md`

**Rules**:
- All lowercase
- Use hyphens, not underscores or spaces
- Descriptive and specific
- No dates in filename

### Frontmatter

Every document **must** include frontmatter:

```yaml
---
title: "Your Document Title"
description: "One-sentence description for search"
category: "getting-started|features|use-cases|troubleshooting|faq|api"
tags: ["tag1", "tag2", "tag3"]
last_updated: "2024-12-25"
---
```

**Guidelines**:
- `title`: Use title case, be specific
- `description`: Single sentence, no period
- `category`: Choose from existing categories
- `tags`: 2-5 relevant tags, lowercase
- `last_updated`: Update when you edit (YYYY-MM-DD format)

### Writing Style

**Tone**:
- Friendly and helpful
- Clear and concise
- Action-oriented
- Avoid jargon

**Voice**:
- Use second person ("you" not "users")
- Active voice ("Click the button" not "The button should be clicked")
- Present tense ("Click" not "You will click")

**Examples**:

✅ **Good**: "Click **Settings** to configure your account."

❌ **Bad**: "Users should navigate to the Settings page where they will be able to configure their account."

### Formatting

**Headers**:
- H1 (`#`) for document title only
- H2 (`##`) for main sections
- H3 (`###`) for subsections
- Don't skip levels (no H4 without H3)

**Lists**:
- Use bullets for unordered lists
- Use numbers for sequential steps
- Keep items parallel (all sentences or all fragments)

**Emphasis**:
- **Bold** for UI elements, buttons, field names
- `Code` for commands, code, filenames, URLs
- *Italic* sparingly for emphasis

**Links**:
- Use relative links for internal docs: `[Guide](./other-guide.md)`
- Use descriptive text: "See the [SSO guide](./sso.md)" not "Click [here](./sso.md)"
- Check all links work before committing

**Code Blocks**:
- Always specify language: ` ```bash `, ` ```python `, etc.
- Include comments explaining non-obvious parts
- Keep examples realistic and practical

### Structure

**Every document should have**:

1. **Introduction**: What is this about? Who is it for?
2. **Main Content**: The information, organized logically
3. **Related Links**: Cross-references to related docs
4. **Next Steps**: What to do after reading

**Optional sections** (use when relevant):
- Prerequisites
- Step-by-Step Guide
- Troubleshooting
- Examples
- Best Practices
- FAQ

### Cross-Linking

Link to related documents to help users (and the chatbot) navigate:

```markdown
For more details, see [Two-Factor Authentication](./two-factor-auth.md).

Related articles:
- [Account Security](./security-settings.md)
- [Password Policy](./password-policy.md)
```

**Guidelines**:
- Link at first mention of related topic
- Always use relative paths
- Check links work (use VS Code link checker)
- Don't over-link (1-3 links per paragraph max)

## Document Organization

### Where to Put New Documents

```
docs/
├── getting-started/    → First-time user guides, onboarding
├── features/          → How to use specific features
├── use-cases/         → Industry or scenario-specific guides
├── api/              → API documentation
├── troubleshooting/  → Problem solving, errors
└── faq/              → Quick Q&A format
```

**Decision tree**:
- Is it for new users? → `getting-started/`
- Is it about a specific feature? → `features/`
- Is it industry/scenario specific? → `use-cases/`
- Is it solving a problem? → `troubleshooting/`
- Is it a quick answer? → `faq/`

### Updating Index Files

When adding a new document, update the relevant `README.md` index file:

```markdown
## Features

- [Single Sign-On (SSO)](./sso.md)
- [Two-Factor Authentication](./two-factor-auth.md)
- [Your New Feature](./your-new-feature.md)  ← Add this line
```

## Contribution Workflow

### 1. Create a Branch

```bash
git checkout -b update-password-docs
```

Branch naming:
- `add-[feature]` for new docs
- `update-[topic]` for updates
- `fix-[issue]` for corrections

### 2. Make Your Changes

- Copy `TEMPLATE.md` for new docs
- Edit existing files for updates
- Follow style guide above
- Preview in VS Code/Cursor

### 3. Test Your Changes

Before committing:
- [ ] Read through your changes
- [ ] Check all links work
- [ ] Verify code examples are correct
- [ ] Run spell check
- [ ] Update `last_updated` in frontmatter
- [ ] Preview markdown rendering

### 4. Commit

```bash
git add docs/features/your-file.md
git commit -m "Add guide for [feature name]"
```

**Commit message format**:
- Start with verb: Add, Update, Fix, Remove
- Be specific: "Add SSO setup guide" not "Update docs"
- One logical change per commit

### 5. Push and Create PR

```bash
git push origin your-branch-name
```

Then create a Pull Request on GitHub:
- Clear title and description
- Reference any related issues
- Request review from team

## Review Checklist

When reviewing someone's documentation:

**Content**:
- [ ] Information is accurate
- [ ] Examples work
- [ ] Steps are clear and complete
- [ ] Links work

**Style**:
- [ ] Frontmatter is complete
- [ ] Follows writing style guide
- [ ] Formatting is consistent
- [ ] No spelling/grammar errors

**Organization**:
- [ ] In correct folder
- [ ] Filename follows conventions
- [ ] Index updated if needed
- [ ] Cross-links are appropriate

## Common Mistakes to Avoid

❌ **Don't**:
- Use first person ("I", "we") - use "you" instead
- Write walls of text - break into sections
- Skip frontmatter - it's required
- Forget to update `last_updated`
- Use absolute URLs for internal links
- Create orphaned pages (no links to them)

✅ **Do**:
- Use clear, descriptive headings
- Add examples and screenshots
- Link to related documents
- Keep paragraphs short (3-4 sentences max)
- Test your instructions
- Use consistent terminology

## Tools We Use

**Recommended**:
- VS Code with Markdown extensions
- markdownlint extension
- Grammarly for spell check

**Optional**:
- Cursor (AI-powered editing)
- Typora (WYSIWYG markdown editor)
- Obsidian (knowledge base)

## Questions?

- Check [SETUP-GUIDE.md](./SETUP-GUIDE.md) for detailed instructions
- Ask in team Slack channel
- Open an issue on GitHub
- Email docs-team@aceunlock.com

## Recognition

Great documentation makes a huge difference! Contributors who consistently create high-quality docs will be recognized in:
- Monthly team updates
- README contributors section
- Quarterly awards

Thank you for helping make AceUnlock documentation excellent! 🎉
