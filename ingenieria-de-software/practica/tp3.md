# TP3

- Variables
- Asignación de variables
- Tipos básicos
- Operaciones aritmeticas
- Concatenación de strings
- Keyword: print

## Tokens

```ts
let a: boolean = true;
let b: number;
b = 4;

let c = 4 * 2 + 5;
let string: string = "asd" + "asd" + "cd";

print 3;
```

### Literals

- BOOLEAN_LITERAL: `true | false`
- NUMERIC_LITERAL: `(1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 0)+`
- STRING_LITERAL: `"[a-zA-Z]*"`
- null
- undefined

### Keywords

- `boolean`
- `number`
- `string`
- `let`
- `print`

### Operators

- `+`
- `-`
- `*`
- `/`
- `=`
- `%`

### Separators

- `(`
- `)`
- `;`
- `:`

### Identifiers

- `[a-zA-Z_$][0-9a-zA-Z_$]*`

## Parser

### Gramática

```bnf
LITERAL:
    'null'
    'undefined'
    BOOLEAN_LITERAL
    NUMERIC_LITERAL
    STRING_LITERAL

INDENTIFIER_REFERENCE:
    IDENTIFIER

PRIMARY_EXPRESSION:
    LITERAL
    INDENTIFIER_REFERENCE
    '(' EXPRESSION ')'

TYPE:
    'boolean'
    'number'
    'string'

MULTIPLICATIVE_EXPRESSION:
    PRIMARY_EXPRESSION
    MULTIPLICATIVE_EXPRESSION '*' PRIMARY_EXPRESSION
    MULTIPLICATIVE_EXPRESSION '/' PRIMARY_EXPRESSION
    MULTIPLICATIVE_EXPRESSION '%' PRIMARY_EXPRESSION

ADDITIVE_EXPRESSION:
    MULTIPLICATIVE_EXPRESSION
    ADDITIVE_EXPRESSION '+' MULTIPLICATIVE_EXPRESSION
    ADDITIVE_EXPRESSION '-' MULTIPLICATIVE_EXPRESSION

EXPRESSION:
    ADDITIVE_EXPRESSION

INITIALIZER: '=' EXPRESSION

TYPE_ANNOTATION: ':' TYPE

VARIABLE_DECLARATION: 'let' IDENTIFIER TYPE_ANNOTATION? INITIALIZER? ';'

PRINT: 'print' EXPRESSION ';'

COVER_INITIALIZED_NAME: IDENTIFIER_REFERENCE INITIALIZER ';'
```
