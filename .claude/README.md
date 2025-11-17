# Claude Configuration

This directory contains Claude-specific configuration files.

## Skills

### apple-docs.md

A Claude skill that provides expert access to Apple Developer Documentation. This skill enhances Claude's ability to help with Apple platform development by providing structured access to:

- Apple Developer Documentation search and retrieval
- Framework and API discovery
- WWDC video content and transcripts
- Sample code browsing
- Platform compatibility checking
- API relationship analysis

#### How to Use

When this skill is activated, Claude will have enhanced capabilities for:

1. **Searching Documentation**: Finding specific APIs, classes, methods, and frameworks
2. **Understanding APIs**: Deep diving into documentation with enhanced analysis
3. **Exploring Frameworks**: Browsing and understanding Apple's framework ecosystem
4. **WWDC Content**: Searching and accessing WWDC videos with transcripts and code
5. **Platform Analysis**: Checking API availability across iOS, macOS, watchOS, tvOS, and visionOS
6. **Finding Alternatives**: Discovering similar or related APIs

#### Available Tools

The skill provides access to 18 specialized MCP tools:

**Core Documentation (4 tools)**
- search_apple_docs
- get_apple_doc_content
- list_technologies
- search_framework_symbols

**API Discovery (4 tools)**
- get_related_apis
- resolve_references_batch
- find_similar_apis
- get_platform_compatibility

**Documentation Updates (3 tools)**
- get_documentation_updates
- get_technology_overviews
- get_sample_code

**WWDC Videos (7 tools)**
- list_wwdc_videos
- search_wwdc_content
- get_wwdc_video
- get_wwdc_code_examples
- browse_wwdc_topics
- find_related_wwdc_videos
- list_wwdc_years

#### Examples

Ask Claude things like:

- "Find the SwiftUI List documentation with related APIs"
- "Show me WWDC videos about async/await in Swift"
- "What's the platform compatibility for SwiftData?"
- "Find sample code for ARKit"
- "Search for UIViewController delegate methods"
- "Get WWDC 2024 videos about SwiftUI"

#### Features

- **Offline WWDC Access**: All WWDC content (2014-2025) is bundled locally
- **Smart Caching**: Intelligent caching for fast responses
- **Enhanced Analysis**: Optional deep-dive into API relationships
- **Full Text Search**: Search across 1,260+ WWDC transcripts
- **Platform Support**: iOS, macOS, watchOS, tvOS, visionOS

## Installation

This skill works with the apple-docs MCP server. Make sure the MCP server is installed and configured:

```bash
# Install the MCP server
npm install -g @kimsungwhee/apple-docs-mcp

# Or use via npx
npx -y @kimsungwhee/apple-docs-mcp
```

## Contributing

To modify or enhance the skill, edit the `skills/apple-docs.md` file and ensure it follows Claude skill best practices.
