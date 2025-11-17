# Installing Apple Developer Documentation as a Claude Custom Skill

This guide walks you through installing the Apple Developer Documentation as a custom skill in Claude.

## Prerequisites

- Access to Claude.ai with Projects feature OR Claude Code
- The `SKILL.md` file from this repository

## Option 1: Claude.ai Web Interface

### Step 1: Get the SKILL.md File

**Method A: Clone the Repository**
```bash
git clone https://github.com/kimsungwhee/apple-docs-mcp.git
cd apple-docs-mcp
# The SKILL.md file is now available
```

**Method B: Download Just the File**
1. Go to https://github.com/kimsungwhee/apple-docs-mcp
2. Click on `SKILL.md`
3. Click the "Raw" button
4. Right-click → "Save As" to download

### Step 2: Create or Open a Project in Claude.ai

1. Go to https://claude.ai
2. Click on "Projects" in the sidebar
3. Create a new project or open an existing one

### Step 3: Add the Custom Skill

1. In your Project, click on "Project Settings" (gear icon)
2. Navigate to the "Skills" or "Custom Skills" section
3. Click "Add Skill" or "Upload Skill"
4. Select the `SKILL.md` file you downloaded
5. Confirm the skill is loaded

### Step 4: Verify Installation

In your project chat, try asking:
```
What skills do you have available?
```

Claude should list the "apple-developer-documentation" skill.

### Step 5: Start Using

Try these example queries:
```
Search for SwiftUI animations
What is UIViewController?
Show me WWDC 2024 sessions about Swift
Find sample code for ARKit
```

## Option 2: Claude Code

### Step 1: Get the Repository

```bash
git clone https://github.com/kimsungwhee/apple-docs-mcp.git
```

### Step 2: Place in Skills Directory

**Method A: Copy to Skills Directory**
```bash
# Create skills directory if it doesn't exist
mkdir -p ~/.claude-code/skills

# Copy the entire folder
cp -r apple-docs-mcp ~/.claude-code/skills/

# Or just copy the SKILL.md file
cp apple-docs-mcp/SKILL.md ~/.claude-code/skills/apple-developer-documentation.md
```

**Method B: Symlink (for easy updates)**
```bash
# Create skills directory if it doesn't exist
mkdir -p ~/.claude-code/skills

# Create symlink to the repository
ln -s /path/to/apple-docs-mcp ~/.claude-code/skills/apple-docs-mcp
```

### Step 3: Restart Claude Code

Close and reopen Claude Code to load the new skill.

### Step 4: Verify Installation

In Claude Code, ask:
```
What skills do you have?
```

The skill should appear in the list.

### Step 5: Start Using

The skill is now available in all your Claude Code conversations.

## Troubleshooting

### Skill Not Appearing

**For Claude.ai:**
- Make sure you're in a Project (skills don't work in regular chats)
- Check that the SKILL.md file has proper YAML frontmatter
- Try refreshing the page
- Try removing and re-adding the skill

**For Claude Code:**
- Verify the file is in the correct directory
- Check that the file is named with `.md` extension
- Ensure the YAML frontmatter is properly formatted
- Restart Claude Code completely

### Skill Not Working

1. **Check YAML Frontmatter**: The file must start with:
   ```yaml
   ---
   name: apple-developer-documentation
   description: ...
   version: 1.0.0
   ---
   ```

2. **Verify File Format**: Ensure it's a plain text Markdown file, not a Word doc or PDF

3. **Test with Simple Query**: Try a basic question like "What is SwiftUI?"

### YAML Validation Issues

If you get YAML parsing errors, check:
- Three dashes (`---`) at the beginning and end of frontmatter
- No tabs (use spaces only)
- Proper indentation
- Quotes around values with special characters

## Updating the Skill

### For Claude.ai
1. Download the latest `SKILL.md` file
2. Remove the old skill from Project Settings
3. Add the new skill file

### For Claude Code
**If you used a symlink:**
```bash
cd /path/to/apple-docs-mcp
git pull
```
Then restart Claude Code.

**If you copied the file:**
```bash
cd apple-docs-mcp
git pull
cp SKILL.md ~/.claude-code/skills/apple-developer-documentation.md
```
Then restart Claude Code.

## Using Multiple Skills

You can use this skill alongside other custom skills. Claude will automatically:
- Load all skills efficiently (progressive loading)
- Use the appropriate skill based on your query
- Combine skills when needed

## Performance Tips

1. **Be Specific**: Mention framework names (SwiftUI, UIKit) in your queries
2. **Use the Right Tool**: The skill has 17 specialized tools - being specific helps Claude choose the right one
3. **Check Context**: Skills are most effective in Project contexts where they can maintain conversation history

## Advanced: Creating Your Own Modified Skill

You can customize the SKILL.md file:

1. Copy the SKILL.md file
2. Modify the YAML frontmatter:
   ```yaml
   ---
   name: my-custom-apple-docs
   description: My customized Apple documentation skill
   version: 1.0.0
   ---
   ```
3. Modify the instructions to suit your needs
4. Save and add to Claude as described above

## Getting Help

- **Quick Reference**: See `SKILL-QUICK-REFERENCE.md` for common usage patterns
- **Full Documentation**: See the complete `SKILL.md` for detailed information
- **MCP Server Issues**: https://github.com/kimsungwhee/apple-docs-mcp/issues
- **Claude Skills Documentation**: https://support.claude.com/en/articles/12512198-creating-custom-skills

## Next Steps

Once installed, check out:
- `SKILL-QUICK-REFERENCE.md` for quick examples
- `SKILL.md` for comprehensive documentation
- Try the example workflows in the documentation
