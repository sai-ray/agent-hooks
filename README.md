# agent-hooks

A collection of reusable hooks for AI-powered IDEs.

## Kiro Hooks

Hooks for [Kiro](https://kiro.dev) that automate common workflows.

### agent-done-notify

Plays a system sound (macOS) when the Kiro agent finishes its response, so you don't have to keep watching the screen.

**Setup:**

```bash
cp kiro-hooks/agent-done-notify.kiro.hook <your-project>/.kiro/hooks/
```

Or symlink it:

```bash
mkdir -p .kiro/hooks
ln -s $(pwd)/kiro-hooks/agent-done-notify.kiro.hook .kiro/hooks/
```

**Requirements:**
- macOS (uses `afplay` and system sounds)

**Customization:**

You can swap the sound by editing the hook file and changing the path. Available sounds are in `/System/Library/Sounds/`:
`Basso`, `Blow`, `Bottle`, `Frog`, `Funk`, `Glass`, `Hero`, `Morse`, `Ping`, `Pop`, `Purr`, `Sosumi`, `Submarine`, `Tink`

> **Note:** Kiro does not currently support global hooks (`~/.kiro/hooks/`). Each workspace needs its own copy. See [this feature request](https://github.com/sai-ray/agent-hooks/issues) for tracking.
