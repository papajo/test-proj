# OKF Template Instructions

## Overview

OKF (Objectives, Key Results, Framework) templates help maintain project clarity and save tokens by providing structured documentation from day one.

## Skills

### 1. OKF Template Builder

Auto-generates OKF.md from project metadata.

**Run:**
```bash
python ~/.agents/skills/okf-template-builder/scripts/build_template.py
```

**Auto-detects:**
- Project type (Python, React, Node.js, Rust, Go, etc.)
- Primary language
- Dependencies
- Version info

### 2. OKF Template Usage

Optimizes existing OKF templates for token efficiency.

**Techniques:**
- Convert paragraphs to tables (saves ~60% tokens)
- Use bullet points over prose
- Add hierarchical structure for context memory
- Create cross-references between sections

**Targets:**
- 20% token reduction
- 30% context memory improvement
- 85% user satisfaction

## Installation

```bash
# Install all tools
bash ~/.agents/skills/okf-template-builder/install.sh

# Add to PATH (if not already)
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

## Usage

### Create New Project

```bash
cd ~/Projects
newproject my-awesome-project
```

This creates:
- Project directory
- Git repository
- OKF.md template

### Existing Project

```bash
cd /path/to/existing-project
python ~/.agents/skills/okf-template-builder/scripts/build_template.py
```

## Git Hook

Installed globally - warns on `git commit` if OKF.md is missing.

**Sections checked:**
- Overview
- Objectives
- Key Results

## GitHub Action

CI check for PRs to main/master.

**File:** `.github/workflows/check-okf.yml`

**Validates:**
- OKF.md exists
- Required sections present

## OKF Template Structure

```markdown
# Project Name

## Overview
[Project description]

## Objectives
1. [Primary objective]
2. [Secondary objective]

## Key Results
- [ ] [Measurable outcome]
- [ ] [Measurable outcome]

## Architecture
| Component | Technology |
|-----------|------------|
| Language | [Detected] |
| Type | [Detected] |

## Dependencies
- [dep1]
- [dep2]

## Next Steps
1. [Action item]
2. [Action item]
```

## Files Location

```
~/.agents/skills/okf-template-builder/
├── SKILL.md                    # Skill definition
├── install.sh                  # Installation script
├── hooks/
│   └── pre-commit              # Git hook
├── scripts/
│   ├── build_template.py       # Template generator
│   └── newproject.sh           # Shell function
└── .github/workflows/
    └── check-okf.yml           # CI check
```

## Tips

1. Generate OKF early - before writing code
2. Review and update monthly
3. Use as onboarding material
4. Link to detailed docs from OKF sections
5. Keep key results measurable
