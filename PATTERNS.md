# Regex Patterns / Padrões Regex

## Basics / Básicos

| Pattern | EN | PT | Example match |
|---------|----|----|---------------|
| `.` | Any char except newline | Qualquer char exceto newline | `a`, `1` |
| `\d` | Digit | Dígito | `0`-`9` |
| `\w` | Word char `[A-Za-z0-9_]` | Carácter de palavra | `a`, `_` |
| `\s` | Whitespace | Espaço em branco | space, tab |
| `^` / `$` | Start / end of string | Início / fim da string | — |
| `*` / `+` / `?` | 0+, 1+, 0 or 1 | 0+, 1+, 0 ou 1 | — |

## Common patterns / Padrões comuns

### Digits only / Só dígitos
```
^\d+$
```
Matches: `42` · Does not: `42a`

### UUID (simple) / UUID (simples)
```
^[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}$
```

### ISO date YYYY-MM-DD / Data ISO
```
^\d{4}-\d{2}-\d{2}$
```

### IPv4 (simple) / IPv4 (simples)
```
^(?:\d{1,3}\.){3}\d{1,3}$
```
**EN:** Not a full validation (allows 999.999.999.999). **PT:** Não é validação completa.

### Slug
```
^[a-z0-9]+(?:-[a-z0-9]+)*$
```

## Tips / Dicas

**EN:** Prefer well-tested libraries for email/URL validation over complex regex.

**PT:** Prefere bibliotecas testadas para validar email/URL em vez de regex complexas.
