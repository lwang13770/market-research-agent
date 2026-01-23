# Market Research Agent

An AI-powered assistant for conducting comprehensive market research on any company. Built for PM interview prep, competitive intelligence, and strategic research.

## What It Does

1. **Collects context** - Asks for company name, industry, stage, research goal, and desired depth
2. **Conducts live research** - Searches the web for current market data, competitors, and trends
3. **Generates structured output** - Delivers formatted reports tailored to your specific needs

## Use Cases

- **Interview Prep** - Research a company before a PM interview
- **Competitive Analysis** - Understand competitor positioning, pricing, and strategy
- **Market Exploration** - Learn about a new industry or market opportunity

## How to Use

1. Open this folder in Claude Code
2. Start a conversation - the agent will prompt you for information
3. Answer the intake questions:
   - Company name
   - Industry/space
   - Company stage (Startup/Growth/Enterprise)
   - Your context (interview prep, competitive analysis, etc.)
   - Research depth (Quick or In-depth)
4. Receive your research reports

## Research Modes

### Quick Mode
Focused research delivering two reports (1500-2000 words each):
- Company overview and competitive landscape
- Best for time-sensitive needs or initial exploration

### In-Depth Mode
Comprehensive analysis across 5 dimensions (3000-4000 words total):

| Dimension | What It Covers |
|-----------|----------------|
| **Market Sizing** | TAM/SAM/SOM estimates, growth rates, segmentation |
| **Competitive Intelligence** | Competitor analysis, positioning, pricing, strengths/weaknesses |
| **Tech Maturity** | Infrastructure readiness, technology trends, adoption barriers |
| **Economic Sentiment** | Macro indicators, funding environment, market conditions |
| **Regulatory** | Compliance requirements, legal considerations, policy trends |

Each dimension receives a score (1-10) with supporting rationale.

## Output

Reports are saved to `research/[company]-[date]/`:

**Quick Mode:**
| File | Contents |
|------|----------|
| `company-overview.md` | Company facts, recent news, opportunities, risks, context-specific insights |
| `competitive-research.md` | Market overview, competitor analysis, strategic positioning, recommendations |

**In-Depth Mode:**
| File | Contents |
|------|----------|
| `indepth-market-research.md` | Comprehensive analysis across all 5 dimensions with scores |

## Project Structure

```
market-research-agent/
├── CLAUDE.md                              # Agent instructions and guardrails
├── README.md                              # This file
├── prompts/
│   ├── intake.md                          # Information gathering questions
│   ├── quick-market-research.md           # Quick mode research prompt
│   ├── indepth-01-market-sizing.md        # In-depth: TAM/SAM/SOM
│   ├── indepth-02-competitive-intelligence.md  # In-depth: Competitors
│   ├── indepth-03-tech-maturity.md        # In-depth: Infrastructure
│   ├── indepth-04-economic-sentiment.md   # In-depth: Macro indicators
│   └── indepth-05-regulatory-research.md  # In-depth: Compliance
├── templates/
│   ├── company-overview.md                 # Company template
│   ├── quick-market-research.md           # Quick mode: competitive template
│   └── indepth-market-research.md         # In-depth mode: comprehensive template
└── research/                              # Generated reports (gitignored)
```

## Requirements

- Claude Code CLI or VS Code extension
- Web search enabled for current market data

## Notes

- Research outputs are gitignored to avoid committing sensitive company data
- Each research session creates a timestamped folder for version tracking
- The agent will check for existing research before re-researching the same company
