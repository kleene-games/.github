# Kleene Games

**Text adventures that remember you chose NOT to open the door**

## Play AND Create Interactive Fiction in Claude Code

Kleene brings classic text adventure gameplay directly into your Claude Code sessions. Slay dragons, solve mysteries, explore dungeons—or type whatever wild action you can imagine and watch Claude improvise the outcome.

But here's the magic: **you can also create your own adventures.** Generate complete scenarios from a simple theme, validate their structure, and share them with others.

```bash
# Play a game
/kleene play

# Create a new scenario from scratch
/kleene generate "a detective mystery in 1920s Paris"

# Validate your scenario's structure
/kleene analyze my_scenario

# Or jump straight into an existing adventure
/kleene play dragon_quest
```

No separate app. No server. Just conversation-driven storytelling with persistent save states and a full authoring toolkit.

## Quick Start

```bash
# Install the plugin (see kleene repository)
cd ~/.claude/plugins
git clone https://github.com/kleene-games/kleene.git

# Play a game
/kleene play

# Generate a new scenario
/kleene generate [theme]

# Analyze scenario structure
/kleene analyze
```

## Features

### For Players
- **Improvisation Support**: Type any action—Claude interprets and responds dynamically
- **State Persistence**: Save/load game states, pick up where you left off
- **Auto-approval Hooks**: Seamless gameplay without permission prompts
- **Pure Claude Code Integration**: No separate app, plays in your terminal

### For Creators
- **AI-Powered Generation**: Create complete scenarios from a single theme prompt
- **YAML-based Format**: Human-readable, version-controllable scenario files
- **Structural Validation**: Analyze completeness across Bronze/Silver/Gold tiers
- **Nine Cells Framework**: Built-in guidance for rich, non-binary storytelling
- **Preconditions & Consequences**: Full game logic with inventory, traits, flags, relationships

## Create Your Own Scenarios

Kleene isn't just a game engine—it's a complete authoring toolkit:

1. **Generate**: Start with a theme (`/kleene generate "space station mystery"`)
2. **Edit**: Scenarios are YAML files you can hand-edit or ask Claude to refine
3. **Validate**: Check structural completeness (`/kleene analyze my_scenario`)
4. **Play**: Test your creation immediately (`/kleene play my_scenario`)
5. **Share**: Push to the community scenarios repo

The framework guides you through the Nine Cells model, ensuring your scenarios have depth beyond simple binary choices. Bronze tier (4 cells) is fully playable—Silver and Gold add nuance.

## Repository Structure

- **[kleene](https://github.com/kleene-games/kleene)** - Core plugin and framework
- **[scenarios](https://github.com/kleene-games/scenarios)** - Community scenario library (coming soon)

## How It Works: Three-Valued Logic

Under the hood, Kleene is built on a fascinating bit of computer science. Named after [Stephen Cole Kleene](https://en.wikipedia.org/wiki/Stephen_Cole_Kleene), who formalized three-valued logic in 1938, it models narrative states using Option types:

- **Some(value)** - The protagonist exists and can act
- **None** - The protagonist has ceased (death, departure, transcendence)
- **Unknown** - The narrative hasn't resolved yet

### The Nine Cells Framework

Every choice in a Kleene game exists at the intersection of three player states and three world responses:

|                    | World Permits | World Indeterminate | World Blocks |
|--------------------|---------------|---------------------|--------------|
| **Player Chooses** | Triumph       | Commitment          | Barrier      |
| **Player Unknown** | Discovery     | Limbo               | Revelation   |
| **Player Avoids**  | Escape        | Deferral            | Fate         |

This creates nine distinct narrative cells, each representing a unique combination of player agency and world response. The center cell—**Limbo**—is where improvisation thrives, allowing players to take free-text actions beyond predefined choices.

Traditional branching narratives use binary choices (yes/no, success/fail). Kleene adds a third dimension: uncertainty. This models real decision-making where outcomes aren't always known, paths aren't always taken, and the world doesn't always cooperate.

The result? Richer, more nuanced interactive storytelling that captures hesitation, discovery, and the beautiful chaos of improvised action.

## Contributing

We welcome scenario contributions, framework improvements, and documentation enhancements. See the main [kleene repository](https://github.com/kleene-games/kleene) for contribution guidelines.

## Learn More

- 📚 [Framework Documentation](https://github.com/kleene-games/kleene/tree/main/lib/framework)
- 🎮 [Example Scenarios](https://github.com/kleene-games/kleene/tree/main/scenarios)
- 💡 [Plugin Architecture](https://github.com/kleene-games/kleene/blob/main/CLAUDE.md)

---

*"In logic, as in life, not everything is true or false. Sometimes, it's simply unknown."*
