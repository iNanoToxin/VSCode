# Tree Sitter Query

## Features
Syntax highlighting and snippets for tree-sitter query files. File extensions with `.scm` or `.tsq` are supported.

## Snippets
Supported snippets for predicates and directives:
- `eq?`, `not-eq?`, `any-eq?`, `any-not-eq?`
- `match?`, `not-match?`, `any-match?`, `any-not-match?`
- `any-of?`, `not-any-of?`
- `is?`, `is-not?`
- `set!`

## Customization
Token colors can be adjusted through the user `settings.json` file.

| Token Type | Token Scope                                                    |
| ---------- | -------------------------------------------------------------- |
| comment    | comment.tree-sitter-query                                      |
| node       | keyword.other.node.tree-sitter-query<br>node.tree-sitter-query |
| string     | string.tree-sitter-query                                       |
| capture    | variable.capture.tree-sitter-query                             |
| field      | entity.name.type.field.tree-sitter-query                       |
| directive  | entity.name.function.directive.tree-sitter-query               |
| quantifier | keyword.operator.arithmetic.quantifier.tree-sitter-query       |

Example usage in `settings.json` file:
```json
{
    "editor.tokenColorCustomizations": {
        "textMateRules": [
            {
                "name": "node",
                "scope": "keyword.other.node.tree-sitter-query",
                "settings": {
                    "foreground": "#f692ce"
                }
            },
            {
                "name": "capture",
                "scope": "variable.capture.tree-sitter-query",
                "settings": {
                    "foreground": "#f97583"
                }
            },
            {
                "name": "field",
                "scope": "entity.name.type.field.tree-sitter-query",
                "settings": {
                    "foreground": "#b392f0"
                }
            },
            {
                "name": "directive",
                "scope": "entity.name.function.directive.tree-sitter-query",
                "settings": {
                    "foreground": "#79b8ff"
                }
            }
        ]
    }
}
```