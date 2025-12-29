# BidDeed.AI Architecture Documentation

**Auto-generated architecture documentation via RepoSwarm**

This repository contains automatically generated architecture documentation for all BidDeed.AI repositories. Documentation is updated daily at 2 AM EST by analyzing source code, workflows, and patterns across our organization.

## Available Documentation

Each repository in the BidDeed.AI ecosystem has its own `.arch.md` file:

- **brevard-bidder-scraper.arch.md** - Core foreclosure auction intelligence pipeline
- **life-os.arch.md** - Life OS orchestration and ADHD task tracking
- **biddeed-conversational-ai.arch.md** - Conversational AI agent and landing pages
- **spd-site-plan-dev.arch.md** - Site Plan Development (SPD) pipeline
- **tax-insurance-optimizer.arch.md** - Tax and insurance optimization module

## How It Works

### Investigation Prompts
RepoSwarm uses specialized investigation prompts tailored to our tech stack:

1. **LangGraph Orchestration** - Multi-agent coordination, checkpoints, state flow
2. **MCP Integration** - Model Context Protocol server implementations
3. **GitHub Actions Deployment** - CI/CD workflows and autonomous deployments
4. **Smart Router Architecture** - LLM cost optimization and tier selection
5. **Foreclosure Domain Logic** - Lien analysis and bidding strategies
6. **Observability Patterns** - Logging, metrics, error tracking

### Prompt Result Caching
- Caches analysis results by commit hash + prompt version
- Only re-analyzes when code changes or prompts are updated
- Saves 80-90% of token costs on unchanged repositories

### Update Schedule
- **Daily:** 2 AM EST (automatic)
- **Manual:** Trigger via GitHub Actions UI

## For AI Agents

These architecture documents are optimized for AI agent consumption. When working on BidDeed.AI projects:

1. Read the relevant `.arch.md` file first for context
2. Cross-reference related repos via dependency sections
3. Follow established patterns documented in each file
4. Update PROJECT_STATE.json in source repos when making architectural changes

## Configuration

Configuration is managed in the source repository workflows. See `.github/workflows/reposwarm.yml` for:
- Repository inclusion/exclusion rules
- Investigation prompt definitions
- Caching strategies
- Schedule settings

## Cost Optimization

**Token Usage Strategy:**
- Claude Sonnet 4.5 for analysis (1M context window)
- ~2,000-4,000 tokens per repository analysis
- Caching reduces costs by 80-90% after initial run
- Estimated: $5-10/month for 5 repositories with daily updates

## Links

- **GitHub Organization:** [breverdbidder](https://github.com/breverdbidder)
- **Main Website:** [brevard-bidder-landing.pages.dev](https://brevard-bidder-landing.pages.dev)
- **Conversational Agent:** [brevard-bidder-landing.pages.dev/agent](https://brevard-bidder-landing.pages.dev/agent)

---

**Last Updated:** Auto-generated daily by RepoSwarm
**Maintained By:** Claude AI (AI Architect) + GitHub Actions
