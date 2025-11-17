# Claude Configuration

This directory contains Claude-specific configuration files.

## Skills

### apple-docs.md

A Claude skill that provides expert access to Apple Developer Documentation using **direct Python code execution**. This skill enables Claude to fetch, parse, and present Apple documentation without relying on MCP tools.

#### How It Works

The skill provides Claude with complete Python code for:

1. **HTTP Requests**: Fetching documentation from Apple's APIs with proper Safari user agents
2. **JSON/HTML Parsing**: Extracting structured data from Apple's documentation
3. **WWDC Data Access**: Reading bundled offline WWDC video transcripts and code (2014-2025)
4. **Platform Analysis**: Checking API availability across Apple platforms

#### Core Capabilities

- **Search Apple Documentation**: Find APIs, classes, methods, and frameworks
- **Fetch Documentation Content**: Get detailed API documentation with examples
- **Browse Technologies**: List all Apple frameworks and technologies
- **Access WWDC Content**: Search 1,260+ video transcripts and code examples (offline)
- **Platform Compatibility**: Check API availability across iOS, macOS, watchOS, tvOS, visionOS

#### Implementation Details

The skill includes complete Python implementations for:

**Core Functions:**
- `search_apple_docs()` - Search developer documentation
- `get_doc_content()` - Fetch and parse API documentation
- `list_technologies()` - Browse frameworks and technologies
- `get_platform_compatibility()` - Check platform availability

**WWDC Functions:**
- `load_wwdc_index()` - Load full WWDC index
- `load_wwdc_year()` - Load videos for a specific year
- `search_wwdc_content()` - Search transcripts and code
- `list_wwdc_videos()` - List videos with filters
- `get_wwdc_video()` - Get complete video content
- `list_wwdc_topics()` - List all WWDC topics
- `list_wwdc_years()` - List available years

**Helper Functions:**
- `fetch_url()` - HTTP requests with Safari user agents
- `fetch_json()` - Fetch and parse JSON APIs
- `convert_to_json_api_url()` - Convert doc URLs to API URLs
- `extract_text_from_content()` - Parse documentation content

#### Data Sources

**Online APIs:**
- Apple Developer Documentation: `https://developer.apple.com/documentation/`
- Apple Search API: `https://developer.apple.com/search/`
- Apple JSON API: `https://developer.apple.com/tutorials/data/`

**Offline WWDC Data:**
- Location: `/home/user/apple-docs-mcp/data/wwdc/`
- Contents: 1,260+ WWDC videos (2014-2025)
- Includes: Full transcripts, code examples, metadata
- Size: ~35MB of optimized JSON

#### Example Usage

When this skill is active, ask Claude:

```
"Find the SwiftUI List documentation"
# Claude will execute: search_apple_docs("SwiftUI List")
# Then fetch details with: get_doc_content(url)

"Show me WWDC 2024 videos about async/await"
# Claude will execute: list_wwdc_videos(year="2024")
# And search: search_wwdc_content("async await", year="2024")

"What's the platform compatibility for SwiftData?"
# Claude will execute: search_apple_docs("SwiftData")
# Then: get_platform_compatibility(url)
```

#### Advantages Over MCP

- **No external dependencies**: Pure Python code execution
- **Faster startup**: No MCP server to initialize
- **Full control**: Complete code visibility and customization
- **Offline WWDC access**: All video data bundled locally
- **Transparent operation**: See exactly what code is running

#### Requirements

- Python 3 with standard library (json, urllib, re, pathlib)
- Access to `/home/user/apple-docs-mcp/data/wwdc/` for WWDC data
- Internet connection for live documentation queries

#### Technical Details

**User-Agent Handling:**
- Uses Safari user agents for best compatibility with Apple's site
- Rotates between multiple recent Safari versions
- Includes proper Accept and Accept-Language headers

**Error Handling:**
- All functions return dictionaries with 'error' key on failure
- Graceful degradation when data is unavailable
- Timeout protection (30 seconds default)

**Data Parsing:**
- JSON API parsing for structured documentation
- HTML parsing for search results
- Text extraction from nested content structures
- Code block formatting preservation

## Installation

This skill works standalone with the bundled WWDC data. No additional installation required beyond having the apple-docs-mcp repository cloned locally with the `data/wwdc/` directory intact.

## Contributing

To modify or enhance the skill, edit the `skills/apple-docs.md` file. All helper functions are embedded directly in the skill file as executable Python code.

## Maintenance Notes

- WWDC data is bundled in `data/wwdc/` and built into the npm package
- Update WWDC data by rebuilding the npm package
- Apple's API structure may change; update parsing logic as needed
- Safari user-agent strings should be updated periodically for best results
