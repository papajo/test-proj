# Welcome To Test Project

A repository demonstrating OKF templates, Entity Maps, and AI engineer roadmaps.

---

## Table of Contents

- [Overview](#overview)
- [Documentation](#documentation)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

This project contains:

1. **OKF Templates** - Objectives, Key Results, and project structure
2. **Entity Maps** - Visual relationship diagrams for knowledge mapping
3. **FDE Roadmap** - 90-day Forward Deployed Engineer learning path

---

## Documentation

### OKF System

| File | Description |
|------|-------------|
| [OKF.md](OKF.md) | Project objectives and key results |
| [okf-instructions.md](okf-instructions.md) | How to use OKF templates |

### Entity Maps

| File | Description |
|------|-------------|
| [entity-maps.md](entity-maps.md) | Entity maps overview |
| [entity-maps-instructions.md](entity-maps-instructions.md) | How to create entity maps |

### FDE AI Engineer Roadmap

| File | Description |
|------|-------------|
| [FDE-AI-Engineer-Roadmap.md](FDE-AI-Engineer-Roadmap.md) | Original 90-day roadmap |
| [FDE-AI-Engineer-Roadmap-OKF.md](FDE-AI-Engineer-Roadmap-OKF.md) | OKF version with objectives |
| [fde-roadmap-entity-map.md](fde-roadmap-entity-map.md) | Architecture visualization |

---

## Getting Started

### Prerequisites

- Python 3.10+
- Git

### Installation

```bash
# Clone the repository
git clone https://github.com/papajo/test-proj.git
cd test-proj

# Install OKF tools
bash ~/.agents/skills/okf-template-builder/install.sh
```

---

## Usage

### Create OKF for New Project

```bash
python ~/.agents/skills/okf-template-builder/scripts/build_template.py
```

### Create Entity Map

```bash
python ~/.agents/skills/entity-maps/scripts/create_map.py "Project Architecture"
```

### Create New Project with OKF

```bash
newproject my-new-project
```

---

## Project Structure

```
test-proj/
├── README.md                                    # This file
├── OKF.md                                       # Project OKF
├── okf-instructions.md                          # OKF usage guide
├── entity-maps.md                               # Entity maps overview
├── entity-maps-instructions.md                  # Entity maps guide
├── FDE-AI-Engineer-Roadmap.md                   # Original roadmap
├── FDE-AI-Engineer-Roadmap-OKF.md               # Roadmap OKF
└── fde-roadmap-entity-map.md                    # Roadmap entity map
```

---

## Quick Reference

### OKF Template Structure

```markdown
# Project Name

## Overview
[Description]

## Objectives
1. [Objective 1]
2. [Objective 2]

## Key Results
- [ ] [Measurable result]

## Architecture
| Component | Technology |
|-----------|------------|

## Dependencies
- [dep1]

## Next Steps
1. [Action]
```

### Entity Map Structure

```markdown
## Entities
- **Entity**: Description `[tags]`

## Relationships
- Entity A → [relates-to] → Entity B

## Graph
```mermaid
graph LR
    A -->|relates-to| B
```
```

---

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to your fork
5. Submit a pull request

---

## License

MIT License - See [LICENSE](LICENSE) for details.

---

## Project Links

- [OKF Documentation](OKF.md)
- [OKF Instructions](okf-instructions.md)
- [Entity Maps](entity-maps.md)
- [Entity Maps Instructions](entity-maps-instructions.md)
- [FDE Roadmap](FDE-AI-Engineer-Roadmap.md)
- [FDE Roadmap OKF](FDE-AI-Engineer-Roadmap-OKF.md)
- [FDE Entity Map](fde-roadmap-entity-map.md)
