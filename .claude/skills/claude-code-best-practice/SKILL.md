# claude-code-best-practice Development Patterns

> Auto-generated skill from repository analysis

## Overview

This repository establishes best practices for Claude Code development, focusing on workflow creation, documentation patterns, and orchestration examples. The codebase demonstrates how to structure Claude agents, commands, and documentation in a systematic way, with emphasis on weather workflow orchestration and comprehensive changelog tracking.

## Coding Conventions

### File Naming
- Use camelCase for file naming: `workflowAgent.md`, `changelogReport.md`
- Agent files: `workflow-*-agent.md` pattern in `.claude/agents/`
- Command files: `workflow-*.md` pattern in `.claude/commands/`
- Documentation: kebab-case for directories: `best-practice/`, `orchestration-workflow/`

### Import/Export Style
- Mixed import styles depending on context
- Maintain consistency within individual workflow components

### Directory Structure
```
.claude/
├── agents/workflows/best-practice/
├── commands/workflows/best-practice/
└── skills/weather-*/
best-practice/
implementation/
changelog/
orchestration-workflow/
```

## Workflows

### Best Practice Workflow Creation
**Trigger:** When adding or updating a best practice feature
**Command:** `/new-best-practice-workflow`

1. Create or update workflow agent in `.claude/agents/workflows/best-practice/workflow-*-agent.md`
2. Create or update workflow command in `.claude/commands/workflows/best-practice/workflow-*.md`
3. Update main best practice documentation in `best-practice/*.md`
4. Update `README.md` with new content and examples
5. Create changelog in `changelog/best-practice/*/changelog.md`
6. Create verification checklist in `changelog/best-practice/*/verification-checklist.md`

**Example Agent Structure:**
```markdown
# Workflow Agent

## Purpose
Define the specific workflow purpose and scope

## Responsibilities  
- Task coordination
- Documentation generation
- Quality assurance
```

### README Content Updates
**Trigger:** When adding new tips, features, or content to the main documentation
**Command:** `/update-readme`

1. Update `README.md` with new content sections
2. Update `CLAUDE.md` in parallel if needed
3. Add supporting assets or tags in `!/tags/*.svg`
4. Ensure cross-references are maintained
5. Validate all links and examples

### Orchestration Workflow Updates
**Trigger:** When updating the weather orchestration example workflow  
**Command:** `/update-weather-workflow`

1. Update weather agent configuration in `.claude/agents/weather*.md`
2. Update weather-related skills in `.claude/skills/weather-*/SKILL.md`
3. Update orchestration workflow documentation in `orchestration-workflow/orchestration-workflow.md`
4. Generate new output files in `orchestration-workflow/output.md`
5. Update visual diagrams in `orchestration-workflow/weather.svg`
6. Update `.claude/settings.json` if configuration changes are needed

### Implementation Documentation Sync
**Trigger:** When best practices are updated and need implementation guidance
**Command:** `/sync-implementation-docs`

1. Update best practice documentation in `best-practice/claude-*.md`
2. Update corresponding implementation files in `implementation/claude-*-implementation.md`
3. Sync changes to `README.md`
4. Update main `CLAUDE.md` if architectural changes occurred
5. Verify all cross-references between practice and implementation docs

### Changelog Report Workflow
**Trigger:** When documenting changes to specific features or components
**Command:** `/create-changelog-report`

1. Create workflow changelog agent in `.claude/agents/workflows/reports/workflow-changelog-*-agent.md`
2. Create workflow changelog command in `.claude/commands/workflows/reports/workflow-changelog-report-*.md`
3. Generate changelog documentation in `changelog/*/changelog.md`
4. Create verification checklist in `changelog/*/verification-checklist.md`
5. Update main documentation and reports in `reports/*.md`

**Changelog Template:**
```markdown
# Feature Changelog

## Changes
- Addition/modification details
- Impact assessment

## Files Modified
- List of affected files

## Verification Steps
- [ ] Documentation updated
- [ ] Examples tested
- [ ] Cross-references validated
```

## Testing Patterns

- Test files follow `*.test.*` pattern
- Testing framework not explicitly defined, allowing flexibility
- Focus on verification checklists for manual validation
- Emphasis on documentation testing through cross-reference validation

## Commands

| Command | Purpose |
|---------|---------|
| `/new-best-practice-workflow` | Create complete best practice workflow with agents, commands, and docs |
| `/update-readme` | Update main documentation with new content and tips |
| `/update-weather-workflow` | Update weather orchestration example components |
| `/sync-implementation-docs` | Synchronize best practice and implementation documentation |
| `/create-changelog-report` | Generate changelog reports with verification checklists |