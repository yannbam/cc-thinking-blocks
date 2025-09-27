cc-thinking-blocks - Extract thinking blocks from Claude Code sessions

Thinking blocks from previous messages get removed by the API so Claude can't see them.
A bug in Claude Code can even cause thinking blocks from the current message to disappear.
This tool enables Claude to retrieve ALL previous thinking blocks.
Use this tool *proactively* to maintain continuity across turns.
Never lose your train of thought again!

Usage:
  cc-thinking-blocks <session-id> [mode]
  cc-thinking-blocks --project-path <path> [mode]

Modes:
  previous (default) - All thinking blocks from previous assistant message
  current            - All thinking blocks from current assistant message
  list               - Overview of all messages with thinking block counts
  message <N>        - All thinking blocks from assistant message N

Options:
  --project-path      Use newest session file for this project directory instead of session-id
  --debug             Show all user messages with line indices for testing
  --help              Show this help message

Usage Examples:
cc-thinking-blocks <session-id>            # "What did I think in my previous turn?"
cc-thinking-blocks <session-id> current    # "My current thinking blocks are gone! Let me recover them."
cc-thinking-blocks <session-id> list       # "Let me get an overview to find the message where I... "
cc-thinking-blocks <session-id> message 3  # "Let me see that analysis again"
cc-thinking-blocks --project-path .        # "I don't know the session id. Let me use the current project directory instead.
