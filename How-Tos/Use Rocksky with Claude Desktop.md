
This guide will walk you through setting up Rocksky [MCP (Model Control Protocol)](https://modelcontextprotocol.io/introduction) and using it with [Claude Desktop](https://claude.ai/download) to interact with the Rocksky API.

![Screenshot from 2025-04-26 01-28-22.png](https://api.apidog.com/api/v1/projects/821757/resources/354190/image-preview)

## Prerequisites

- [Node.js](https://nodejs.org/en) and [npm](https://www.npmjs.com) installed on your system
- Claude Desktop application installed
- A Rocksky account (if you don't have one, sign up at [rocksky.app](https://rocksky.app))

## Setting Up Rocksky MCP

### Step 1: Install Rocksky CLI
First, install the Rocksky CLI globally using npm:
```bash
npm install -g @rocksky/cli
```

### Step 2: Configure Claude Desktop for Rocksky MCP

1. Open Claude Desktop
2. Go to Settings (gear icon) > Advanced > Model Control Protocol
3. Enable MCP by toggling the switch to "On"
4. Click "Edit Configuration" to open the MCP config file
5. Add the following configuration to the file:

```json
{
  "mcpServers": {
    "rocksky": {
      "command": "rocksky",
      "args": [
        "mcp"
      ]
    }
  }
}
```

6. Save the configuration file
7. Restart Claude Desktop for the changes to take effect

## Using Rocksky with Claude
Once you've set up Rocksky MCP, you can start interacting with the Rocksky API through Claude. Here are some examples of what you can do:

## Get Recently Played Tracks
Simply ask Claude:
```
What are my recently played tracks?
```

Claude will use the Rocksky MCP to fetch your scrobble history and display it.

## View Your Top Artists
Ask Claude:
```
Show me my top artists on Rocksky
```

## Search for Music
You can search for tracks, artists, or albums:
```
Search for tracks by Radiohead
```

## View User Stats
Get your listening statistics:
```
What are my Rocksky stats?
```

## View Now Playing
See what's currently playing:
```
What am I listening to right now?
```

## Advanced Usage
### Viewing Other Users' Data

You can also view other users' listening data by specifying their username or DID:
```
Show me the recently played tracks for username.bsky.social
```

### Limiting Results
You can specify how many results you want to see:
```
Show me my top 10 tracks
```

### API Keys (For Developers)

If you're developing with Rocksky, you can create API keys:
```
Create a new Rocksky API key called "My Application"
```
### Troubleshooting

If you encounter any issues:

1. Ensure the Rocksky CLI is properly installed
2. Verify your MCP configuration is correct
3. Check if you're logged into your Rocksky account
4. Restart Claude Desktop

## Further Resources

- [AT Protocol Documentation](https://atproto.com)
- [Claude MCP Documentation](https://docs.anthropic.com/en/docs/agents-and-tools/mcp)

