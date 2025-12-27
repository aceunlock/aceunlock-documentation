# AceUnlock Documentation

Welcome to the AceUnlock documentation repository. This contains comprehensive guides for AceUnlock, an AI-powered recruitment platform that streamlines hiring through automated interviews and intelligent candidate evaluation.

**📚 Live Documentation:** [https://aceunlock.github.io/aceunlock-documentation](https://aceunlock.github.io/aceunlock-documentation)

## Documentation Structure

```
docs/
├── getting-started/     # Onboarding guides for new users
├── features/           # Detailed feature documentation
├── use-cases/          # Industry/scenario-specific guides
├── troubleshooting/   # Common issues and solutions
└── faq/               # Frequently asked questions
```

## Available Documentation

### 🚀 Getting Started
- **[Create Account](docs/getting-started/create-account.md)** - Account setup and onboarding

### ⚙️ Core Features

#### Job Management
- **[Create New Job Posting](docs/features/create-new-job.md)** - Comprehensive guide to creating job postings with full control and customization
- **[Quick Create Job Posting](docs/features/quick-create.md)** - Rapidly create job postings with AI-powered automation
- **[Job Postings Dashboard](docs/features/job-postings.md)** - Manage job interviews and track applications
- **[Interview Dashboard](docs/features/interview-dashboard.md)** - Monitor and manage candidate interviews in real-time

#### Evaluation & Assessment
- **[Evaluation Rubrics](docs/features/rubrics.md)** - AI-powered evaluation rubrics and scoring system
- **[Interview Questions](docs/features/question.md)** - Question bank and management system for AI interviews

#### Communication
- **[Email Templates](docs/features/email-template.md)** - Customizable email templates for candidate communication

#### Organization & Settings
- **[Company Management](docs/features/company.md)** - Company profiles and settings
- **[User Profile](docs/features/user-profile.md)** - User profile management and settings

### 💼 Use Cases
- **[Recruiting](docs/use-cases/recruiting.md)** - Best practices for recruitment workflows
- **[Startups](docs/use-cases/startups.md)** - Tailored guidance for startup hiring needs

### ❓ Support
- **[FAQ](docs/faq/README.md)** - Frequently asked questions
- **[Troubleshooting](docs/troubleshooting/README.md)** - Common issues and solutions

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

## Viewing the Documentation

### Online
Visit our live documentation site: **[https://aceunlock.github.io/aceunlock-documentation](https://aceunlock.github.io/aceunlock-documentation)**

### Locally
To preview the documentation locally:
- Use any markdown editor (VS Code, Cursor, Typora)
- Or run Jekyll locally:
  ```bash
  bundle install
  bundle exec jekyll serve
  ```
  Then visit `http://localhost:4000/aceunlock-documentation/`

## Support

Need help? Contact us:
- 📧 Email: support@aceunlock.com
- 💬 [FAQ](docs/faq/README.md)
- 🐛 [Report Issues](https://github.com/aceunlock/aceunlock-documentation/issues)

## License

Copyright © 2024 AceUnlock. All rights reserved.
