# QT-RulesMCP

MCP server for [QT-Rules](https://github.com/lpmwfx/QT-Rules) — Qt AI anti-patterns, correct patterns, RULE/BANNED markers.

## Install

```bash
pipx install git+https://github.com/lpmwfx/QT-RulesMCP.git
```

## Add to Claude Code

```bash
claude mcp add -s user qt-rules -- qt-rules-mcp
```

## Tools

| Tool | Description |
|------|-------------|
| `search_rules(query, category?, limit?)` | Search rules by keyword — matches tags, concepts, qt_apis, title |
| `get_rule(file)` | Get full markdown content of a specific rule file |
| `get_context(languages, topics?)` | Combined rules context for given languages and topics |
| `get_learning_path(languages, phase?)` | Rules in implementation order — foundational first, dependent later |
| `list_rules(category?)` | List available rule files by category |

## Learning Path

`get_learning_path` returns rules grouped in phases based on dependency analysis of the QT-Rules repo. Phase 1 = foundational rules to read first. Avoids rule overflow by giving only what's relevant for the current implementation stage.

```
get_learning_path(languages=["cpp", "qml"], phase=1)
```

Categories: `cpp`, `qml`, `js`, `rust`, `build-rules`

## License

EUPL-1.2


---

<!-- LARS:START -->
<a href="https://lpmathiasen.com">
  <img src="https://carousel.lpmathiasen.com/carousel.svg?slot=9" alt="Lars P. Mathiasen"/>
</a>
<!-- LARS:END -->

<!-- MIB-NOTICE -->

> **Note:** This project is as-is — it is an artefact of a MIB process. See [mib.lpmwfx.com](https://mib.lpmwfx.com/) for details. It is only an MVP, not a full release. Feel free to use it for your own projects as you like.
