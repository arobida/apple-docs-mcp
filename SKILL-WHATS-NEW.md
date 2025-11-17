# Claude Custom Skill Support - What's New

This document explains the new Claude custom skill support added to the Apple Developer Documentation MCP server.

## What Changed?

The repository now supports **two ways** to use Apple Developer Documentation in AI assistants:

1. **New: Claude Custom Skill** - Drop-in skill for Claude.ai and Claude Code
2. **Existing: MCP Server** - Full integration for Claude Desktop, Cursor, VS Code, etc.

## For Existing MCP Server Users

**Nothing breaks!** If you're already using the MCP server with Claude Desktop, Cursor, or other tools, everything continues to work exactly as before. The MCP server functionality is unchanged.

## What's a Claude Custom Skill?

A Claude custom skill is a lightweight, modular way to extend Claude's capabilities:
- **Easier Setup**: Just upload a SKILL.md file (no configuration needed)
- **Efficient**: Uses progressive loading (loads only when needed)
- **Portable**: Works in Claude.ai Projects and Claude Code
- **Native**: Built into Claude's skill system

## New Files Added

### 1. SKILL.md
The main skill file that Claude loads. Contains:
- YAML metadata (name, description, version)
- Complete documentation of all 17 tools
- Usage guidelines and examples
- Best practices and workflows

### 2. SKILL-QUICK-REFERENCE.md
Quick examples and common patterns for users who want to get started fast.

### 3. SKILL-INSTALLATION.md
Detailed installation instructions for both Claude.ai and Claude Code, including troubleshooting.

## How to Use the Skill

### For Claude.ai Users
1. Download this repository or just SKILL.md
2. Open a Project in Claude.ai
3. Go to Project Settings → Custom Skills
4. Upload SKILL.md
5. Start asking about Apple development!

### For Claude Code Users
1. Place SKILL.md in your skills directory
2. Claude Code auto-discovers it
3. Verify with: "What skills do you have?"

## Comparison: Skill vs MCP Server

### Use the Skill When:
- You use Claude.ai web interface
- You use Claude Code IDE
- You want zero configuration
- You want portable setup across Claude platforms
- You don't need multi-tool support

### Use the MCP Server When:
- You use Claude Desktop
- You use Cursor or VS Code
- You want automation and programmatic access
- You need multi-tool support
- You prefer npm-based updates

## What Stays the Same

- All 17 tools/capabilities work identically
- Same access to 1,260+ WWDC videos
- Same Apple documentation coverage
- Same performance and caching
- Same code examples and sample projects

## Technical Details

### YAML Frontmatter
```yaml
---
name: apple-developer-documentation
description: Access comprehensive Apple Developer Documentation...
version: 1.0.0
---
```

### Progressive Loading
Claude loads skill metadata at session start, but only loads full content when relevant to your query. This saves context window space.

### Tools Available
All 17 tools from the MCP server are documented and available in the skill:
1. search_apple_docs
2. get_apple_doc_content
3. list_technologies
4. search_framework_symbols
5. get_related_apis
6. resolve_references_batch
7. get_platform_compatibility
8. find_similar_apis
9. get_documentation_updates
10. get_technology_overviews
11. get_sample_code
12. list_wwdc_videos
13. search_wwdc_content
14. get_wwdc_video
15. get_wwdc_code_examples
16. browse_wwdc_topics
17. find_related_wwdc_videos
18. list_wwdc_years

## Migration Path

### From MCP Server to Skill (Optional)

If you're currently using the MCP server and want to try the skill:

**Claude Desktop Users**: Stay on MCP server (skill not available)
**Claude.ai Users**: Try the skill (easier, no config needed)
**Claude Code Users**: You can use either (skill is simpler)

No migration needed - both work simultaneously!

## Package Distribution

The skill files (SKILL.md, SKILL-*.md) are now included in the npm package:
```json
"files": [
  "dist",
  "README.md",
  "README.*.md",
  "SKILL.md",
  "SKILL-*.md",
  "LICENSE"
]
```

This means when you install via npm, you get both:
- The MCP server (`dist/index.js`)
- The skill files (SKILL.md, etc.)

## Documentation Updates

The README.md now:
- Highlights both usage options
- Provides a decision guide
- Shows pros/cons of each approach
- Includes quick start for both methods

## Backwards Compatibility

**100% backwards compatible.** All existing configurations, scripts, and integrations continue to work without any changes.

## What's Next?

You can:
1. Keep using the MCP server (nothing changes)
2. Try the skill alongside the MCP server
3. Switch to the skill if you're on Claude.ai or Claude Code
4. Use both in different contexts (MCP for Cursor, skill for Claude.ai)

## Questions?

- **Installation Help**: See SKILL-INSTALLATION.md
- **Quick Examples**: See SKILL-QUICK-REFERENCE.md
- **Full Documentation**: See SKILL.md
- **Issues**: https://github.com/kimsungwhee/apple-docs-mcp/issues

## Learn More

- [Claude Custom Skills Guide](https://support.claude.com/en/articles/12512198-creating-custom-skills)
- [MCP Protocol Documentation](https://modelcontextprotocol.io)
- [Repository](https://github.com/kimsungwhee/apple-docs-mcp)
