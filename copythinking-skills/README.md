# Copythinking Skills

A Claude Code plugin providing expert copywriting and marketing skills.

## Installation

### Via Claude Code CLI

```bash
# Add the marketplace
/plugin marketplace add truebrewbirdie/copythinking-marketplace

# Install the plugin
/plugin install copythinking-skills@truebrewbirdie-marketplace
```

### Manual Installation

Clone this repository and add it as a local marketplace:

```bash
git clone https://github.com/truebrewbirdie/copythinking-skills.git
cd copythinking-skills
claude
/plugin marketplace add ./
```

## Included Skills

| Skill | Description |
|-------|-------------|
| `copythinking-orchestrator` | Master orchestrator for all Copythinking skills. Loads and coordinates specializ... |
| `copythinking-awareness` | Strategic foundation for copywriting - determines customer awareness level (unaw... |
| `copythinking-advanced` | Advanced research methods, market sophistication analysis, and deep customer psy... |
| `copythinking-persuasion-psychology` | Master psychological triggers and persuasion frameworks for high-converting copy... |
| `copythinking-tactical` | Tactical execution tools for copywriting including 19 bullet-point formulas, hoo... |
| `copywriting-fundamentals` | Essential foundation for writing clear, compelling copy that connects with reade... |
| `copy-quality-frameworks` | Core copywriting quality frameworks that apply to ALL copy. Use automatically wh... |
| `hook-creator` | Generate attention-grabbing headlines and hooks for marketing content. Use when ... |
| `ad-hook-creator` | Generate high-performing ad hooks for Meta, LinkedIn, TikTok, and YouTube. Creat... |
| `aeo-optimizer` | Optimize content for AI Engine Optimization (AEO) - ensuring content ranks well ... |


## Usage

Skills are automatically invoked by Claude based on your request. Just ask naturally:

- "Help me write a compelling headline for my SaaS product"
- "Review this landing page copy for conversion issues"
- "Create 10 hook options for my email campaign"
- "What awareness level should I target for this audience?"

## Skill Workflow

```
User Query
    │
    ├─ Strategic question? → copythinking-awareness + copythinking-advanced
    ├─ "How to write...?" → copywriting-fundamentals + copythinking-tactical  
    ├─ Persuasion/emotion? → copythinking-persuasion-psychology
    ├─ Templates needed? → copythinking-tactical
    └─ Deep research? → copythinking-advanced
```

## License

MIT License - True Brew Birdie Ltd.
