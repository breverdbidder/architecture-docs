# RepoSwarm Configuration

## Investigation Prompts

### 1. LangGraph Orchestration
**Applies to:** Python repos with `requirements.txt` containing `langgraph`

Analyzes multi-agent orchestration patterns, state management, checkpoint strategies, and token budget management.

### 2. MCP Integration
**Applies to:** Repos with `mcp_nodes.py` or `.mcp.json`

Documents Model Context Protocol server implementations, tool definitions, and integration patterns.

### 3. GitHub Actions Deployment
**Applies to:** Repos with `.github/workflows/`

Catalogs deployment pipelines, secret management, Cloudflare Pages deployments, and orchestrator patterns.

### 4. Smart Router Architecture
**Applies to:** Python repos with `smart_router` or `router` modules

Documents LLM routing logic, cost optimization strategies, and multi-tier model selection.

### 5. Foreclosure Domain Logic
**Applies to:** Repos with `foreclosure` or `auction` keywords

Documents lien discovery patterns, max bid calculations, and real estate domain logic.

### 6. Observability Patterns
**Applies to:** Repos with `structured_logger` or `metrics` modules

Documents logging, metrics collection, error tracking, and Supabase integration.

## Prompt Versioning

Current version: **v1.0**

When prompts are updated:
1. Increment version number in workflow
2. All repos will be re-analyzed on next run
3. Previous analyses are archived with version tags

## Cache Strategy

**Cache Key Format:** `{repo_name}_{commit_hash}_v{prompt_version}`

**Cache Invalidation Triggers:**
- New commits to analyzed repository
- Prompt version update
- Manual cache clear (workflow dispatch)

## Adding New Prompts

To add custom investigation prompts:

1. Edit `.github/workflows/reposwarm.yml`
2. Add new prompt definition in `analyze.py` script
3. Specify `applies_to` conditions (file patterns, keywords)
4. Increment prompt version
5. Commit and push - next run will use new prompts

## Repository Selection

**Included by Default:**
- Non-archived repositories
- Pushed within last 12 months
- From `breverdbidder` organization

**Excluded:**
- Archived repositories
- Repositories with no activity in 12+ months
- Test/demo repositories (manually configured)

## Cost Controls

**Token Budgets:**
- Max 4,000 tokens per repository analysis
- Max 5KB per source file included in context
- Max 20 files per repository analysis
- Caching reduces re-analysis by 80-90%

**Monthly Estimate:**
- 5 repos × 30 days = 150 potential analyses
- With 85% cache hit rate = 22.5 actual analyses
- 22.5 × 3,000 tokens average = 67,500 tokens/month
- At Sonnet 4.5 rates: ~$0.20/month (included in Max plan)
