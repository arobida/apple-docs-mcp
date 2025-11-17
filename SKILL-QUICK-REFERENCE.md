# Apple Developer Documentation Skill - Quick Reference

This is a quick reference guide for using the Apple Developer Documentation custom skill in Claude.

## Installation

### For Claude.ai
1. Download this repository or just the `SKILL.md` file
2. In Claude.ai, create or open a Project
3. Go to Project settings → Custom Skills
4. Upload or reference the `SKILL.md` file
5. Start using it by asking questions about Apple development

### For Claude Code
1. Place this repository (or `SKILL.md`) in your skills directory
2. Claude Code automatically discovers skills
3. Verify with: "What skills do you have?"

## Quick Examples

### Finding APIs
```
"What is UIViewController and how do I use it?"
"Show me SwiftUI animation modifiers"
"Find Core Data NSPersistentContainer documentation"
```

### WWDC Content
```
"Search WWDC 2024 sessions about SwiftUI"
"Get transcript for WWDC session about async/await"
"Show me all Swift-related WWDC videos from 2023"
```

### Code Examples
```
"Find sample code for ARKit"
"Show me SwiftUI animation examples"
"Get code examples using Combine framework"
```

### Platform Compatibility
```
"Can I use SwiftData on watchOS 9?"
"What's the minimum iOS version for async/await?"
"Check platform availability for Vision framework"
```

## Common Workflows

### Learning a New Framework
1. Ask: "List all machine learning frameworks"
2. Ask: "Get technology overview for Core ML"
3. Ask: "Find sample code for Core ML"
4. Ask: "Show WWDC sessions about Core ML"

### Finding the Right API
1. Ask: "Search for navigation controllers in UIKit"
2. Ask: "Get documentation for UINavigationController"
3. Ask: "Find similar APIs to UINavigationController"
4. Ask: "Check platform compatibility"

### Staying Updated
1. Ask: "What's new in iOS 18?"
2. Ask: "Show latest SwiftUI updates"
3. Ask: "Get WWDC 2024 announcements"

## Available Data

- **Frameworks**: 100+ including SwiftUI, UIKit, Foundation, ARKit, Core ML
- **Platforms**: iOS, macOS, watchOS, tvOS, visionOS
- **WWDC Videos**: 1,260+ sessions (2020-2025) with full transcripts
- **Sample Code**: Complete Apple sample projects
- **Languages**: Swift and Objective-C

## Tips

1. **Be Specific**: Instead of "how to make animations", ask "Show me SwiftUI withAnimation documentation"
2. **Use Framework Names**: Include framework names like "SwiftUI", "UIKit", "Core Data"
3. **Check Compatibility**: Always verify platform support for cross-platform apps
4. **Explore WWDC**: WWDC sessions often have the best explanations and examples
5. **Find Examples**: Sample code and WWDC code examples are great for learning

## Tool Categories

The skill provides 17 specialized tools organized into these categories:

### Documentation & Search
- search_apple_docs
- get_apple_doc_content
- search_framework_symbols

### Framework Discovery
- list_technologies
- get_technology_overviews

### API Analysis
- get_related_apis
- resolve_references_batch
- find_similar_apis
- get_platform_compatibility

### Updates & News
- get_documentation_updates

### Code & Examples
- get_sample_code
- get_wwdc_code_examples

### WWDC Content
- list_wwdc_videos
- search_wwdc_content
- get_wwdc_video
- browse_wwdc_topics
- find_related_wwdc_videos
- list_wwdc_years

## Need More Details?

Check the full `SKILL.md` file for comprehensive documentation including:
- Detailed tool descriptions
- Advanced usage patterns
- Complete parameter reference
- Framework categories
- Best practices

## Support

For issues or questions:
- GitHub: https://github.com/kimsungwhee/apple-docs-mcp
- Issues: https://github.com/kimsungwhee/apple-docs-mcp/issues
