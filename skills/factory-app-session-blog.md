# factory-app-session-blog Skill Definition

## Purpose

Transform development work into portfolio-ready documentation. Extract architectural patterns, design decisions, and business value from session work.

## Skill Invocation

```bash
/factory-app-session-blog <your work description>
```

## Input Format

Provide a description of the architectural work, implementation challenges, or technical decisions you completed:

```
"I implemented a shared transaction pattern for EF Core + Dapper that prevents 
deadlocks when updating domain state and logging bulk telemetry in the same operation. 
Tested with concurrent loads up to 1000 requests/sec."
```

## Output Format

The skill generates:

1. **Executive Summary** (100-200 words)
   - Problem statement
   - Solution approach
   - Key outcomes

2. **Technical Deep-Dive** (1500-2500 words)
   - Architecture overview with diagrams
   - Implementation walkthrough with code examples
   - Performance metrics and testing results
   - Lessons learned and trade-offs

3. **Portfolio Piece** (500-800 words)
   - Audience: Hiring managers, architects, technical leads
   - Focuses on business value and technical impact
   - Includes ROI quantification
   - Actionable recommendations

4. **Distribution Options**
   - Private GitHub Gist (default)
   - Pull request to repository documentation
   - Markdown file for local editing
   - Linked from LinkedIn profile

## Supported Patterns

The skill recognizes and documents these architecture patterns:

### Full-Stack Patterns
- **Type-Safety Pipeline**: Backend build → schema export → frontend code generation
- **Shared Transaction Patterns**: EF Core + Dapper coordinated operations
- **DataLoader Optimization**: N+1 query prevention with batching
- **Elsa Workflow Integration**: Long-running state machine orchestration

### Security Patterns
- **Secret Scanning**: Automated credential detection and push protection
- **Dependency Management**: Automated updates with granular auto-merge rules
- **Code Quality Analysis**: Static analysis across full-stack layers
- **Branch Protection**: Automated governance and PR validation

### Performance Patterns
- **Query Optimization**: Projection-based field selection
- **Batch Processing**: High-velocity telemetry ingestion
- **Change Detection**: OnPush strategies for high-frequency updates
- **Buffer Management**: RxJS buffering for streaming data

## Context Variables

The skill automatically captures:

- **Repository**: Full-stack monorepo (ng-graphql-playground)
- **Tech Stack**: Angular 17+, Hot Chocolate GraphQL, ASP.NET Core, SQL Server
- **Development Model**: Solo developer with GitHub Copilot CLI
- **Current Phase**: Ongoing security hardening (Issue #7), performance optimization
- **Prior Work**: Issue #7 (5-phase security plan), Dependabot automation

## Example Outputs

### Example 1: Shared Transaction Pattern

**Input**: "I fixed deadlock issues in the build workflow by implementing a shared transaction pattern..."

**Output**:
- Blog post: "Atomic Operations in Hybrid Data Access: EF Core + Dapper Patterns" (2400 words)
- Code examples: Transaction initialization, error handling, rollback strategies
- Performance impact: 99.8% deadlock elimination at scale
- Portfolio piece: "Technical Leadership: Designing for Factory Floor Scale" (650 words)

### Example 2: DataLoader Optimization

**Input**: "Implemented DataLoaders for Build → Parts → TestRuns queries, eliminated N+1 queries..."

**Output**:
- Blog post: "Batching Strategies in GraphQL: DataLoaders for Full-Stack Monorepos" (2200 words)
- Benchmarks: Query time reduction from 2.5s → 180ms
- Architecture diagram: DataLoader flow and batch resolution
- Portfolio piece: "Performance Engineering: From N+1 to Optimized Queries" (700 words)

### Example 3: Security Automation

**Input**: "Implemented GitHub security hardening with Dependabot, Secret Scanning, CodeQL..."

**Output**:
- Blog post: "Automating Security for Full-Stack Development" (2100 words)
- Implementation timeline: 4 hours → enterprise-grade governance
- Benefits quantification: 10+ vulnerability classes automated
- Portfolio piece: "Security-First Development: GitHub Native Tools" (750 words)

## Skill Configuration

### Privacy Settings

```bash
# Generate private gist (default, secret URL)
/factory-app-session-blog Document this work

# Generate and publish to public gist
/factory-app-session-blog --public Document this work
```

### Output Formats

```bash
# Generate markdown file locally
/factory-app-session-blog --format markdown Document this work

# Create pull request with documentation
/factory-app-session-blog --create-pr --format markdown Document this work

# Output to stdout (for piping)
/factory-app-session-blog --format json Document this work | jq .
```

### Target Audience

```bash
# Technical (architects, engineers) — default
/factory-app-session-blog Document this work

# Executive (hiring managers, team leads)
/factory-app-session-blog --audience executive Document this work

# Tutorial (step-by-step walkthrough)
/factory-app-session-blog --audience tutorial Document this work
```

## Troubleshooting

### Session Context Not Captured

Ensure you provide sufficient work description:
- What problem did you solve?
- How did you approach it?
- What were the outcomes?
- What did you learn?

### Output Too Short/Long

Adjust verbosity:
```bash
/factory-app-session-blog --verbose Document extensive architectural work
/factory-app-session-blog --concise Document quick implementation
```

### Gist Creation Failed

Verify GitHub authentication:
```bash
gh auth status
gh auth login  # If needed
```

## See Also

- [Plugin Repository](https://github.com/pluto-atom-4/copilot-plugin-factory-app)
- [CLAUDE.md - Skill Configuration](https://github.com/pluto-atom-4/ng-graphql-playground/blob/main/CLAUDE.md)
- [GitHub Copilot CLI Docs](https://docs.github.com/copilot/how-tos/copilot-cli)

