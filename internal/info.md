## Package

```
bear-vscode/
    package.json                  # Extension manifest
    language-configuration.json   # Bracket matching, auto-close, comments
    syntaxes/
        bear.tmLanguage.json      # TextMate grammar (the actual highlighting rules)
README.md
```

## Scopes -> Theme Colors

VSCode themes color tokens are by their TextMate scope. The scopes used here follow
standard conventions, so any theme should highlight them out of the box:

| Bear construct     | Vim group      | TextMate scope                       |
|--------------------|----------------|--------------------------------------|
| import             | Include        | keyword.control.import               |
| mut var static ... | StorageClass   | storage.modifier                     |
| struct variant ... | Structure      | storage.type                         |
| return yield ...   | Statement      | keyword.control.flow                 |
| if else match      | Conditional    | keyword.control.conditional          |
| while for in       | Repeat         | keyword.control.loop                 |
| sizeof alignof ... | Macro          | keyword.operator.expression          |
| true false null    | Boolean        | constant.language                    |
| i32 f64 bool ...   | Type           | storage.type.primitive               |
| FOO_BAR            | Constant       | constant.other                       |
| FooBar             | PascalType     | entity.name.type                     |
| foo(               | Function       | entity.name.function                 |
| foo..bar           | ScopedIdent    | variable.other.scoped                |
| foo                | Identifier     | variable.other                       |
| operators          | Operator       | keyword.operator                     |
| (){}[]             | Bracket        | punctuation.brackets                 |
| ,;:#.              | Delimiter      | punctuation.delimiter                |
| "string"           | String         | string.quoted.double                 |
| 'c'                | Char           | string.quoted.single                 |
| 0-9                | Number         | constant.numeric.integer             |
| 0.0                | Float          | constant.numeric.float               |
| 0x...              | Number (hex)   | constant.numeric.hex                 |
| // comment         | Comment        | comment.line.double-slash            |
| TODO FIXME         | Todo           | keyword.other.todo                   |

## notes on grammar ordering vs vim

TextMate grammars are first-match-wins (opposite of Vim's last-wins). The
order of `patterns` at the top level and within `keyword.patterns` matters:
- `constant-case` is listed before `pascal-type` so ALL_CAPS words are claimed first.
- Keywords are matched before identifiers for the same reason.
- Longer operator patterns appear before shorter ones to avoid partial matches.

##### other notes 
- for myself: a publish field with my publisher id once I have one
