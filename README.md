# Market Research Agent

An AI-powered assistant for conducting comprehensive market research on any company. Built for PM interview prep, competitive intelligence, and strategic research.

## What It Does

1. **Collects context** - Asks for company name, industry, stage, and your research goal
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
4. Receive your research reports

## Output

The agent generates two files saved to `research/[company]-[date]/`:

| File | Contents |
|------|----------|
| `company-overview.md` | Company facts, recent news, opportunities, risks, context-specific insights |
| `competitive-research.md` | Market overview, competitor analysis, strategic positioning, recommendations |

## Research Scope

**Market Sizing & Trends**
- TAM/SAM/SOM estimates
- Growth rates and projections
- Market segmentation

**Competitive Landscape**
- Direct and indirect competitors
- Pricing, positioning, strengths/weaknesses
- Win/loss analysis

**Target Audience**
- Customer personas
- Demographics and psychographics
- Behavioral traits

**Opportunities & Risks**
- Market gaps and unmet needs
- Technology trends
- Regulatory and competitive threats

## Project Structure

```
market-research-agent/
├── CLAUDE.md                     # Agent instructions and guardrails
├── README.md                     # This file
├── prompts/
│   ├── intake.md                 # Information gathering questions
│   └── market-research.md        # Research execution prompt
├── templates/
│   ├── company-overview.md       # Output template
│   └── competitive-research.md   # Output template
└── research/                     # Generated reports (gitignored)
```

## Requirements

- Claude Code CLI or VS Code extension
- Web search enabled for current market data

## Notes

- Research outputs are gitignored to avoid committing sensitive company data
- Each research session creates a timestamped folder for version tracking
- The agent will check for existing research before re-researching the same company
