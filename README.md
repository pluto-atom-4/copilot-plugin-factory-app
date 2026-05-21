# GitHub Copilot CLI Plugin: factory-app-session-blog

Portfolio-ready documentation skill for full-stack monorepo work. Document your architectural achievements as professional blog posts, gists, and portfolio pieces.

## Overview

The `factory-app-session-blog` plugin brings the power of professional documentation to your GitHub Copilot CLI sessions. Transform your development work into portfolio-ready content that showcases architectural patterns, design decisions, and business value.

### Features

✨ **Automatic Pattern Extraction**
- Identifies architectural patterns (type-safety pipelines, DataLoaders, shared transactions)
- Extracts design trade-offs and decisions
- Captures technical implementation details

📝 **Professional Documentation**
- Generates blog-post quality markdown
- Structures content for portfolio portfolios and technical audiences
- Includes lessons learned and recommendations

🎯 **ROI Quantification**
- Quantifies time investment vs. business value
- Measures technical debt reduction
- Demonstrates developer productivity improvements

🔗 **GitHub Integration**
- Publish directly to private gists
- Create pull requests with documentation
- Link to related issues and commits

## Installation

### Prerequisites

- GitHub Copilot CLI v1.0.0+
- GitHub authentication (`gh auth login`)
- Write permissions to the repository (for PR creation)

### Install the Plugin

```bash
# Install from GitHub marketplace
gh copilot -- plugin install pluto-atom-4/copilot-plugin-factory-app

# Verify installation
gh copilot -- plugin list
```

**Expected output:**
```
Installed plugins:

Name: factory-app-session-blog
Version: 1.0.0
Source: pluto-atom-4/copilot-plugin-factory-app
```

## Usage

### Interactive Session

```bash
# Start interactive Copilot session
gh copilot

# In the session, type:
/factory-app-session-blog I implemented a DataLoader optimization that reduced N+1 queries by 80%
```

### Non-Interactive Mode

```bash
gh copilot -p "Use the factory-app-session-blog skill to document my shared transaction pattern work" \
  --allow-all-tools
```

### Examples

#### Example 1: Document Architectural Work

```bash
/factory-app-session-blog Create a portfolio piece about the end-to-end type-safety pipeline 
(backend build → schema export → frontend code-gen) that automatically synchronizes types 
across our full-stack monorepo
```

**Output**: Blog post covering:
- Architecture overview
- Technical implementation details
- Performance impact
- Lessons learned
- Recommendations for other full-stack teams

#### Example 2: Document Security Implementation

```bash
/factory-app-session-blog Document the GitHub Issue #7 security hardening implementation 
including Dependabot automation, Secret Scanning, and the benefits for solo developer workflows
```

**Output**: Portfolio piece with:
- Security features overview
- Implementation effort (4 hours)
- Automation benefits
- Enterprise-grade governance
- ROI analysis

#### Example 3: Create Reusable Pattern Guide

```bash
/factory-app-session-blog I solved a deadlock issue by implementing a shared transaction 
pattern for EF Core + Dapper. Create a reusable guide for this pattern.
```

**Output**: Documentation including:
- Problem statement and root cause
- Solution architecture
- Code examples
- Testing strategies
- Common pitfalls

## Configuration

### For Repository Maintainers

Add to `CLAUDE.md` or contributing guidelines:

```markdown
### Using the factory-app-session-blog Skill

Our plugin generates portfolio-ready documentation from development work:

1. **Install the plugin**:
   ```bash
   gh copilot -- plugin install pluto-atom-4/copilot-plugin-factory-app
   ```

2. **Use in sessions**:
   ```bash
   gh copilot -i "Use factory-app-session-blog to document this architectural work"
   ```

3. **Review and publish**:
   - Output goes to private gists by default
   - Transfer to public portfolio as needed
   - Link from LinkedIn, GitHub profile, or portfolio site
```

### Environment Variables

```bash
# Customize gist privacy (default: secret)
export GIST_PRIVACY=public

# Customize documentation output directory
export COPILOT_PLUGIN_OUTPUT_DIR=~/portfolio-docs
```

## How It Works

```
Your Development Work
        │
        ▼
┌─────────────────────────────────────────┐
│   GitHub Copilot CLI (gh copilot)       │
│                                          │
│  /factory-app-session-blog              │
│  <your work description>                │
└─────────────────────────────────────────┘
        │
        ▼
Skill Analysis & Generation
  ├── Extract architectural patterns
  ├── Identify design trade-offs
  ├── Quantify technical impact
  └── Structure portfolio content
        │
        ▼
Output Formats
  ├── Private GitHub Gist (default)
  ├── Markdown file for review
  ├── Pull request documentation
  └── Portfolio piece template
        │
        ▼
┌─────────────────────────────────────────┐
│   Portfolio-Ready Documentation         │
│                                          │
│   - Blog posts (5000+ words)            │
│   - Technical deep-dives                │
│   - Architecture guides                 │
│   - Lessons learned                     │
│   - ROI quantification                  │
└─────────────────────────────────────────┘
```

## Troubleshooting

### Plugin Not Found After Installation

```bash
# Verify installation
gh copilot -- plugin list

# If missing, try reinstalling
gh copilot -- plugin uninstall factory-app-session-blog
gh copilot -- plugin install pluto-atom-4/copilot-plugin-factory-app
```

### Skill Not Recognized in Session

Ensure you're using correct syntax:

```bash
# ✅ Correct
/factory-app-session-blog Document this work

# ❌ Incorrect (missing leading slash)
factory-app-session-blog Document this work
```

### Output Not Generated

Check permissions:

```bash
# Verify GitHub authentication
gh auth status

# Ensure write permissions
gh repo view --json nameWithOwner
```

### Permission Denied Errors

Reinstall with explicit permissions:

```bash
gh copilot -- plugin uninstall factory-app-session-blog
gh copilot -- plugin install --permissions "*" pluto-atom-4/copilot-plugin-factory-app
```

## Updates and Versions

### Check Current Version

```bash
gh copilot -- plugin list | grep factory-app-session-blog
```

### Update to Latest

```bash
gh copilot -- plugin update factory-app-session-blog
```

### Version History

- **1.0.0** (May 21, 2026) — Initial release
  - Core skill implementation
  - Gist generation
  - Portfolio piece creation

## Contributing

Found a bug or have a feature request?

1. Open an issue: [Issues](https://github.com/pluto-atom-4/copilot-plugin-factory-app/issues)
2. Include:
   - Your Copilot CLI version: `gh copilot -- --version`
   - Your OS and architecture
   - Steps to reproduce
   - Expected vs. actual behavior

## Support

- **Documentation**: [https://github.com/pluto-atom-4/copilot-plugin-factory-app](https://github.com/pluto-atom-4/copilot-plugin-factory-app)
- **Issues**: [GitHub Issues](https://github.com/pluto-atom-4/copilot-plugin-factory-app/issues)
- **GitHub Copilot CLI Docs**: [https://docs.github.com/copilot/how-tos/copilot-cli](https://docs.github.com/copilot/how-tos/copilot-cli)
- **Plugin System Docs**: [https://docs.github.com/copilot/concepts/agents/copilot-cli/about-cli-plugins](https://docs.github.com/copilot/concepts/agents/copilot-cli/about-cli-plugins)

## License

MIT License — See LICENSE file for details

---

**Made with ❤️ for solo developers and full-stack teams building with GitHub Copilot CLI**

