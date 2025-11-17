---
name: apple-developer-documentation
description: Access comprehensive Apple Developer Documentation including iOS/macOS/SwiftUI/UIKit APIs, frameworks, WWDC videos with transcripts, sample code, and technical guides. Use when users ask about Apple development, iOS APIs, Swift programming, SwiftUI components, UIKit classes, WWDC content, or need Apple platform documentation.
version: 1.0.0
---

# Apple Developer Documentation Skill

This skill provides comprehensive access to Apple's official developer documentation, including API references, framework guides, WWDC video transcripts, and sample code projects. Use this skill when working with iOS, macOS, watchOS, tvOS, or visionOS development.

## When to Use This Skill

- When users ask about Apple APIs, frameworks, or development tools
- When searching for SwiftUI views, UIKit controllers, or Foundation classes
- When looking for WWDC session content or video transcripts
- When finding code examples or sample projects
- When checking platform compatibility or API availability
- When exploring Apple technologies and their relationships
- When learning about new features announced at WWDC

## Available Capabilities

### 1. Documentation Search & Retrieval

**search_apple_docs** - Search Apple Developer Documentation
- Find specific APIs, classes, methods, frameworks, or guides
- Filter by type: all, documentation, or sample code
- Best for: finding specific APIs or technical references
- Example: "Search for SwiftUI animations" or "Find UIViewController delegate methods"

**get_apple_doc_content** - Get detailed documentation for a specific API
- Retrieve full documentation with optional enhanced analysis
- Options: related APIs, references, similar APIs, platform compatibility
- Best for: deep-diving into API details and relationships
- Example: "Get details about SwiftUI's withAnimation API"

### 2. Framework & Technology Exploration

**list_technologies** - Browse all Apple technologies and frameworks
- Filter by category (App frameworks, Graphics and games, etc.)
- Filter by language (Swift, Objective-C)
- Filter by beta status
- Best for: discovering available frameworks and understanding the ecosystem
- Example: "List all graphics and games frameworks"

**search_framework_symbols** - Search symbols within a specific framework
- Search classes, structs, protocols in a framework
- Support wildcard patterns for flexible searching
- Filter by symbol type
- Best for: exploring framework structure and finding specific types
- Example: "Search for UIKit classes related to navigation"

### 3. API Relationship Analysis

**get_related_apis** - Discover related APIs and relationships
- Shows inheritance hierarchies
- Shows protocol conformances
- Shows Apple's recommended related APIs
- Best for: understanding API ecosystems and relationships
- Example: "Find APIs related to UIViewController"

**resolve_references_batch** - Deep dive into referenced types
- Resolves all types, methods, and properties mentioned in documentation
- Filter by reference type (symbol, protocol, class, etc.)
- Configurable depth (max 50 references)
- Best for: understanding API dependencies
- Example: "Resolve all references from SwiftUI View documentation"

**find_similar_apis** - Find alternative and functionally similar APIs
- Discover modern replacements for deprecated APIs
- Find platform-specific alternatives
- Configurable search depth (shallow, medium, deep)
- Best for: finding better implementation approaches
- Example: "Find modern alternatives to UIAlertView"

### 4. Platform & Compatibility

**get_platform_compatibility** - Check API availability across platforms
- Shows minimum OS version requirements
- Shows deprecation status
- Checks iOS, macOS, watchOS, tvOS, visionOS support
- Can analyze single API or entire framework
- Best for: planning deployment targets and cross-platform development
- Example: "Check platform compatibility for SwiftUI List"

### 5. Documentation Updates & News

**get_documentation_updates** - Track latest Apple platform updates
- Filter by category: WWDC, technology updates, release notes
- Filter by specific technology or framework
- Filter by year (for WWDC content)
- Include/exclude beta features
- Best for: staying current with Apple development
- Example: "Show latest SwiftUI updates" or "Get WWDC 2024 announcements"

**get_technology_overviews** - Access comprehensive guides and tutorials
- Browse by category (app design, games, AI/ML, AR, etc.)
- Filter by platform (iOS, macOS, watchOS, tvOS, visionOS)
- Search with keywords
- Best for: learning new frameworks or understanding best practices
- Example: "Get AI and machine learning technology overviews"

### 6. Sample Code & Examples

**get_sample_code** - Browse complete Apple sample projects
- Filter by framework (SwiftUI, ARKit, CoreML, etc.)
- Filter beta status: include, exclude, or only beta samples
- Search by keywords for best results
- Best for: learning by example and finding working implementations
- Example: "Find SwiftUI animation sample code" or "Show ARKit examples"

### 7. WWDC Video Content (Offline Access to 1,260+ Sessions)

**list_wwdc_videos** - Browse WWDC session videos
- Filter by year (2020-2025 available)
- Filter by topic (19 categories including Swift, SwiftUI, Machine Learning)
- Filter by code availability
- Full offline access to transcripts and code
- Best for: discovering WWDC content
- Example: "List WWDC 2024 SwiftUI sessions" or "Show videos with code examples"

**search_wwdc_content** - Full-text search across transcripts and code
- Search in transcripts, code, or both
- Filter by year
- Filter by programming language (for code search)
- More powerful than list_wwdc_videos for specific content
- Best for: finding specific discussions or API mentions
- Example: "Search for 'async await' in WWDC transcripts"

**get_wwdc_video** - Access complete session content
- Get full transcript with timestamps
- Get all code examples from the session
- Includes resources and session metadata
- Complete offline access
- Best for: deep-diving into a specific session
- Example: "Get WWDC 2024 session 10101 with transcript"

**get_wwdc_code_examples** - Browse code examples from WWDC
- Filter by framework (SwiftUI, SwiftData, RealityKit, etc.)
- Filter by topic or keyword
- Filter by year
- Filter by language (Swift, Objective-C, JavaScript, Metal)
- Best for: finding implementation patterns and API usage examples
- Example: "Show SwiftUI code examples from WWDC 2024"

**browse_wwdc_topics** - List all WWDC topic categories
- View all 19 topic categories with IDs
- Browse videos within specific topics
- Filter by year within topics
- Best for: understanding WWDC organization and finding topic IDs
- Example: "Browse swiftui-ui-frameworks topic"

**find_related_wwdc_videos** - Discover related WWDC sessions
- Find prerequisite sessions
- Find follow-up content
- Find thematically similar talks
- Essential for creating learning paths
- Best for: comprehensive learning and session discovery
- Example: "Find videos related to WWDC 2024 session 10101"

**list_wwdc_years** - List all available WWDC years
- Shows available years (2020-2025)
- Includes video counts per year
- Best for: understanding content availability
- Example: "List all WWDC years with content"

## Usage Guidelines

### Best Practices

1. **Start Broad, Then Narrow**
   - Use `list_technologies` to discover frameworks
   - Use `search_apple_docs` to find specific APIs
   - Use `get_apple_doc_content` to get detailed information

2. **Leverage Enhanced Analysis**
   - Enable `includeRelatedApis` to see inheritance and protocols
   - Enable `includeSimilarApis` to discover alternatives
   - Enable `includePlatformAnalysis` for cross-platform projects

3. **WWDC Content Strategy**
   - Use `browse_wwdc_topics` first to understand categories
   - Use `search_wwdc_content` for specific technical terms
   - Use `get_wwdc_video` for complete session content
   - Use `find_related_wwdc_videos` to build learning paths

4. **Platform Compatibility**
   - Always check `get_platform_compatibility` for cross-platform apps
   - Use it to find minimum OS version requirements
   - Identify deprecated APIs and their replacements

5. **Finding Examples**
   - Use `get_sample_code` for complete projects
   - Use `get_wwdc_code_examples` for code snippets
   - Use `search_apple_docs` with type="sample" for inline examples

### Common Workflows

**Learning a New Framework:**
1. `list_technologies` - Find the framework
2. `get_technology_overviews` - Read comprehensive guides
3. `get_sample_code` - Browse sample projects
4. `search_wwdc_content` - Find relevant WWDC sessions

**Finding the Right API:**
1. `search_apple_docs` - Search for functionality
2. `get_apple_doc_content` - Review API details
3. `find_similar_apis` - Explore alternatives
4. `get_platform_compatibility` - Check availability

**Building a Learning Path:**
1. `browse_wwdc_topics` - Understand topic categories
2. `list_wwdc_videos` - Find sessions in the topic
3. `get_wwdc_video` - Access session content
4. `find_related_wwdc_videos` - Discover prerequisite or follow-up content

**Modernizing Legacy Code:**
1. `get_apple_doc_content` - Check if APIs are deprecated
2. `find_similar_apis` - Find modern replacements
3. `get_platform_compatibility` - Verify new API availability
4. `get_sample_code` - Find migration examples

## Key Features

### 📚 Comprehensive Coverage
- **Full API Access**: All iOS, macOS, watchOS, tvOS, visionOS documentation
- **Framework Coverage**: SwiftUI, UIKit, Foundation, CoreData, ARKit, and 100+ frameworks
- **1,260+ WWDC Videos**: Full transcripts and code examples (2020-2025)
- **Sample Code**: Complete Apple sample projects with source code

### 🔍 Smart Search
- Intelligent search across documentation
- Full-text search in WWDC transcripts
- Framework-specific symbol search
- Wildcard pattern support

### 🔗 Relationship Discovery
- API inheritance hierarchies
- Protocol conformances
- Similar and alternative APIs
- Related WWDC sessions

### 📊 Platform Analysis
- Cross-platform compatibility checking
- Version requirement tracking
- Beta status identification
- Deprecation warnings

### ⚡ Performance
- Cached documentation (30-minute TTL)
- Bundled WWDC data (zero network latency)
- Offline WWDC access
- Optimized response times

## Example Queries

### API Research
```
"What is UIViewController and what are its key methods?"
→ Use search_apple_docs then get_apple_doc_content

"Show me all SwiftUI view modifiers for animations"
→ Use search_framework_symbols with framework="SwiftUI"

"Find modern alternatives to NSManagedObject"
→ Use find_similar_apis
```

### Learning & Exploration
```
"I want to learn about machine learning frameworks"
→ Use list_technologies with category="Machine learning"

"Show me WWDC sessions about SwiftUI from 2024"
→ Use list_wwdc_videos with year="2024" and topic="swiftui"

"Find sample code for AR applications"
→ Use get_sample_code with framework="ARKit"
```

### Development Planning
```
"Can I use SwiftData on watchOS 9?"
→ Use get_platform_compatibility

"What's new in iOS 18 for developers?"
→ Use get_documentation_updates

"Show me related APIs for URLSession"
→ Use get_related_apis
```

### Deep Dives
```
"Get the full transcript of WWDC 2024 keynote"
→ Use get_wwdc_video with year="2024" and videoId="10101"

"Search WWDC transcripts for mentions of 'async await'"
→ Use search_wwdc_content

"What are all the types referenced in SwiftUI View documentation?"
→ Use resolve_references_batch
```

## Technical Notes

### Data Sources
- **Live Documentation**: Fetched from developer.apple.com with caching
- **WWDC Content**: Bundled in package (35MB, 1,260+ videos)
- **Updates**: WWDC data updated with package releases

### Performance Considerations
- Documentation cached for 30 minutes
- WWDC searches are instant (offline data)
- Enhanced analysis options increase response time
- Batch operations (resolve_references_batch) may take longer

### Limitations
- WWDC video years: 2020-2025 (may be limited based on data available)
- Sample code framework filtering has some limitations
- Maximum 50 references in resolve_references_batch
- Search results are limited by Apple's API

## Framework Categories

### App Frameworks
SwiftUI, UIKit, AppKit, WatchKit, CarPlay

### Graphics & Games
Metal, SpriteKit, SceneKit, GameplayKit, RealityKit

### Machine Learning & AI
Core ML, Vision, Natural Language, Speech, CreateML

### Media
AVFoundation, Core Audio, Core Video, PhotoKit

### System
Foundation, Core Foundation, Combine, Swift Standard Library

### App Services
CloudKit, StoreKit, HealthKit, HomeKit, CallKit

### Developer Tools
Xcode, Swift Package Manager, Instruments, XCTest

### And Many More...
ARKit, MapKit, Core Data, Core Location, Push Notifications, Widgets, App Clips, and 100+ other frameworks

## Version Information

- **Skill Version**: 1.0.0
- **Based on**: Apple Developer Documentation MCP Server v1.0.26
- **WWDC Content**: 2020-2025 sessions
- **Last Updated**: 2025

## Support & Resources

For issues, questions, or contributions related to the underlying MCP server:
- Repository: https://github.com/kimsungwhee/apple-docs-mcp
- Issues: https://github.com/kimsungwhee/apple-docs-mcp/issues

## Disclaimer

This skill is not affiliated with or endorsed by Apple Inc. It uses publicly available Apple Developer Documentation APIs for educational and development purposes.
