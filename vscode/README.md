# Trellix Rules (Expert Rules & IOC Rules)

Syntax highlighting for two Trellix rule languages:

**Expert Rules**: Trellix Endpoint Security (ENS) Exploit Prevention
- Files: `.expertrule`, `.er` (or *Change Language Mode → Trellix Expert Rules*).
- Covers AAC rules (`Rule`, `Initiator`, `Process`, `Target`, `Match`, `Include`/`Exclude`, `AggregateMatch`, `Reaction`…) and legacy Host IPS sections.
- Snippets: `rule-file`, `rule-registry`, `rule-process`, `Match`, `Include`, `Exclude`, `AggregateMatch`, `Reaction`, `Next_Process_Behavior`, `iEnv`.
- Markdown: fenced blocks tagged ` ```expertrule ` are highlighted too.

**IOC Rules**: Trellix EDR / Endpoint Security (HX)
- Files: `.ioc` (OpenIOC 1.1 XML) and `.rule` (HX JSON).
- The regular XML/JSON highlighting is kept. On top of it, the extension highlights the HX event tokens (`processEvent/processCmdLine`…), operators, `presence`/`execution` and platforms.
- **Unknown or misspelled `*Event/…` tokens are marked as errors.**

Source and Notepad++ files: https://github.com/bmarandel/trellix-rules-highlighting

This is a community project. It is not affiliated with or endorsed by Trellix.
