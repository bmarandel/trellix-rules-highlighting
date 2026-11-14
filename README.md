# Trellix Rules : coloration syntaxique

Coloration syntaxique dans **Visual Studio Code** et **Notepad++** pour deux langages de règles Trellix :

| Langage | Produit | Fichiers |
| --- | --- | --- |
| **Expert Rules** (Tcl : règles AAC + sections legacy Host IPS) | Trellix Endpoint Security (ENS), Exploit Prevention | `.expertrule`, `.er` |
| **IOC Rules** (OpenIOC 1.1 XML, JSON HX) | Trellix EDR / Endpoint Security (HX) | `.ioc`, `.rule` |

Projet communautaire, sans lien avec Trellix et non validé par Trellix.

## Installer

Les fichiers sont dans les [releases](../../releases).

**VS Code** : télécharger `trellix-rules-<version>.vsix`, puis
`code --install-extension trellix-rules-<version>.vsix` (ou *Extensions → … → Install from VSIX…*).

- Expert Rules : coloration, snippets (`rule-file`, `rule-registry`, `rule-process`, `Match`, `Include`, `AggregateMatch`, `Reaction`…), repli de code sur `{ }`, commentaire `#` (Ctrl+/), coloration des blocs ` ```expertrule ` dans le Markdown.
- IOC Rules : la coloration XML/JSON habituelle est conservée. S'y ajoutent les tokens HX (`processEvent/processCmdLine`…), les opérateurs, `presence`/`execution` et les plateformes. **Un token `*Event/…` inconnu ou mal orthographié est souligné comme une erreur.**

**Notepad++** : *Langage → Langage utilisateur → Définir votre langage… → Importer…* → `Trellix-Expert-Rules.udl.xml` et `Trellix-HX-Rule.udl.xml`, puis redémarrer Notepad++. Les couleurs sont prévues pour le thème clair par défaut. Pour les `.ioc`, garder le lexer XML intégré : *Paramètres → Configurateur de styles → XML → Ext. utilisateur : `ioc`*.

## Contenu

```
vscode/      extension VS Code (grammaires TextMate, snippets, configuration de langage)
notepad++/   langages définis par l'utilisateur (UDL) pour Notepad++
```

Ces fichiers sont générés : merci de signaler les erreurs de coloration dans les [issues](../../issues), avec un extrait de règle.

## Limites connues

- **Notepad++** : la couleur d'un mot ne dépend pas de sa position (`PROCESS` a la même couleur partout), et les variables `$x` ne sont pas colorées. Dans les chaînes, seuls les access tokens sont colorés. Le `#` est accepté comme commentaire n'importe où (pour `; # commentaire`).
- **Les deux éditeurs** : un `#` juste après `{` sur la même ligne n'est pas traité comme un commentaire.

## Licence

[Apache-2.0](LICENSE). La liste des tokens HX vient en partie des dictionnaires [OpenIOC 1.1](https://github.com/fireeye/OpenIOC_1.1) de FireEye (Apache-2.0) : voir [NOTICE](NOTICE).
