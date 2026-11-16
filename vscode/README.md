# Trellix Rules (Expert Rules & IOC Rules)

Syntax highlighting for two Trellix rule languages:

**Expert Rules**: Trellix Endpoint Security (ENS) Exploit Prevention
- YAML files (`.yml`, `kind: expert-rule`, format of Trellix Rules Editor): the regular YAML highlighting is kept and the Tcl of the top-level `content: |` block is highlighted. Snippet `expert-rule` inserts a complete file.
- Bare Tcl: *Change Language Mode → Trellix Expert Rules* (no file extension is associated).
- Covers AAC rules (`Rule`, `Initiator`, `Process`, `Target`, `Match`, `Include`/`Exclude`, `AggregateMatch`, `Reaction`…) and legacy Host IPS sections.
- Snippets: `rule-file`, `rule-registry`, `rule-process`, `Match`, `Include`, `Exclude`, `AggregateMatch`, `Reaction`, `Next_Process_Behavior`, `iEnv`.
- Markdown: fenced blocks tagged ` ```expertrule ` are highlighted too.

**IOC Rules**: Trellix EDR / Endpoint Security (HX)
- Files: `.ioc` (OpenIOC 1.1 XML) and `.rule` (HX JSON).
- The regular XML/JSON highlighting is kept. On top of it, the extension highlights the HX event tokens (`processEvent/processCmdLine`…), operators, `presence`/`execution` and platforms.
- **Unknown or misspelled `*Event/…` tokens are marked as errors.**

Source and Notepad++ files: https://github.com/bmarandel/trellix-rules-highlighting

This is a community project. It is not affiliated with or endorsed by Trellix.
