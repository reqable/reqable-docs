---
title: Regular Expressions
description: Regular expression help documentation.
sidebar_position: 0
---

A regular expression (regex) is a pattern language used to match, search, and replace text. In Reqable, regex is widely used in search filters, rewrite rules, content replacement, and more. You can also test patterns online with the Regex tool in the Toolbox.

This guide covers the basics, common syntax, and practical examples to help you get started quickly.

## What Is a Regular Expression

Plain text search only finds exact strings, such as `reqable.com`. A regular expression describes a whole class of text with rules, for example:

- Match any email address
- Match URLs that start with `https://`
- Extract a field value from JSON
- Batch-replace request parameters or response content

A regex consists of literal characters and special characters (metacharacters). Literals match themselves; metacharacters express more flexible matching rules.

For example:

```text
reqable\.com
```

matches `reqable.com` in text. Here `\.` matches a literal dot, not “any character”.

Another example:

```text
https?://[^\s]+
```

matches links that start with `http://` or `https://`.

:::tip
Regex dialects differ slightly across engines (such as JavaScript, Python, and PCRE). In Reqable, regex behavior depends on each feature module. After writing a pattern, test it first with the Regex tool in the Toolbox.
:::

## Basic Syntax

### Literal Characters

Letters, digits, and most symbols match themselves.

| Pattern | Meaning | Example match |
| --- | --- | --- |
| `abc` | Matches the text `abc` | `abc` |
| `123` | Matches the text `123` | `123` |

### Metacharacters

Metacharacters have special meaning and form the core of regex.

| Metacharacter | Meaning |
| --- | --- |
| `.` | Matches any single character except a newline |
| `^` | Matches the start of a string |
| `$` | Matches the end of a string |
| `*` | Repeats the previous element 0 or more times |
| `+` | Repeats the previous element 1 or more times |
| `?` | Repeats the previous element 0 or 1 time |
| `\|` | OR — matches either the left or the right side |
| `()` | Groups and captures the matched content |
| `[]` | Character class — matches any one character inside |
| `{}` | Specifies a repetition count |
| `\` | Escape — removes the special meaning of a metacharacter |

### Escaping

To match a metacharacter literally, escape it with `\`.

| Pattern | Meaning |
| --- | --- |
| `\.` | Matches a literal `.` |
| `\*` | Matches a literal `*` |
| `\+` | Matches a literal `+` |
| `\?` | Matches a literal `?` |
| `\(` `\)` | Matches parentheses |
| `\\` | Matches a backslash `\` |

### Character Classes

Use square brackets `[]` to define a set of allowed characters.

| Pattern | Meaning | Example match |
| --- | --- | --- |
| `[abc]` | Matches `a`, `b`, or `c` | `a` |
| `[0-9]` | Matches a digit from 0 to 9 | `7` |
| `[a-z]` | Matches a lowercase letter | `m` |
| `[A-Z]` | Matches an uppercase letter | `M` |
| `[a-zA-Z0-9]` | Matches a letter or digit | `A`, `9` |
| `[^0-9]` | Matches a non-digit | `a`, `_` |

### Predefined Character Classes

| Pattern | Meaning |
| --- | --- |
| `\d` | A digit, equivalent to `[0-9]` |
| `\D` | A non-digit, equivalent to `[^0-9]` |
| `\w` | A word character, equivalent to `[A-Za-z0-9_]` |
| `\W` | A non-word character |
| `\s` | A whitespace character (space, tab, newline, etc.) |
| `\S` | A non-whitespace character |

### Quantifiers

Quantifiers specify how many times the previous element may appear.

| Pattern | Meaning |
| --- | --- |
| `a*` | `a` appears 0 or more times |
| `a+` | `a` appears 1 or more times |
| `a?` | `a` appears 0 or 1 time |
| `a{3}` | `a` appears exactly 3 times |
| `a{2,4}` | `a` appears 2 to 4 times |
| `a{2,}` | `a` appears at least 2 times |

By default, quantifiers are greedy and match as much as possible. Add `?` after a quantifier to make it non-greedy (lazy):

| Pattern | Meaning |
| --- | --- |
| `.*` | Greedy — match as much as possible |
| `.*?` | Non-greedy — match as little as possible |

For the text `<a>1</a><a>2</a>`:

- `<a>.*</a>` matches the entire `<a>1</a><a>2</a>`
- `<a>.*?</a>` matches the shorter `<a>1</a>` first

### Anchors

| Pattern | Meaning |
| --- | --- |
| `^` | Matches the start of a line or string |
| `$` | Matches the end of a line or string |
| `\b` | Word boundary |
| `\B` | Non-word boundary |

Examples:

- `^https` matches a string that starts with `https`
- `\.com$` matches a string that ends with `.com`
- `\bapi\b` matches the whole word `api`, but not `apikey`

### Groups and Captures

Parentheses `()` group parts of a pattern and can also capture matches for later reference or replacement.

```text
(https?)://([^/\s]+)(/[^\s]*)?
```

Meaning:

1. Group 1: protocol `http` or `https`
2. Group 2: hostname
3. Group 3: optional path

In replacements, you can usually refer to groups with `$1`, `$2`, `$3`. For example, transform:

```text
key=12345
```

into:

```text
key=api-$1
```

When the match pattern is `key=(\d+)`, the result becomes:

```text
key=api-12345
```

If you only need grouping and not capturing, use a non-capturing group:

```text
(?:http|https)
```

### Alternation

Use `|` for “or”:

```text
GET|POST|PUT
```

This matches `GET`, `POST`, or `PUT`.

With grouping, it is clearer:

```text
^(GET|POST|PUT)$
```

### Common Flags

Some engines support flags. Common ones include:

| Flag | Meaning |
| --- | --- |
| `i` | Case-insensitive |
| `g` | Global — find all matches, not just the first |
| `m` | Multiline — `^` and `$` match the start and end of each line |
| `s` | Dotall — `.` can also match newlines |

For example, with the `i` flag, `reqable` also matches `Reqable` and `REQABLE`.

## Practical Examples

### 1. Match HTTP Methods

```text
^(GET|POST|PUT|PATCH|DELETE|HEAD|OPTIONS)$
```

### 2. Match a Domain Name

```text
^[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
```

Matches values such as `reqable.com` and `api.example.com`.

### 3. Match a URL

```text
https?://[^\s"'<>]+
```

Matches `http` or `https` links until whitespace or a common delimiter is reached.

### 4. Match an IP Address (Simplified)

```text
\b\d{1,3}(\.\d{1,3}){3}\b
```

Matches values such as `127.0.0.1` and `192.168.1.1`. This is a simplified pattern and does not strictly validate that each octet is ≤ 255.

### 5. Match an Email Address

```text
[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}
```

### 6. Match a Phone Number (Simplified US Format)

```text
^\+?1?[-.\s]?\(?\d{3}\)?[-.\s]?\d{3}[-.\s]?\d{4}$
```

Matches values such as `4155552671`, `(415) 555-2671`, and `+1-415-555-2671`.

### 7. Extract a Query Parameter Value

Given this URL:

```text
https://reqable.com?key=12345&foo=bar
```

Extract the value of `key`:

```text
[?&]key=([^&]*)
```

Capture group 1 is `12345`.

### 8. Extract a JSON Field Value

Given this text:

```json
{"token":"abc123","expired":false}
```

Extract the value of `token`:

```text
"token"\s*:\s*"([^"]*)"
```

Capture group 1 is `abc123`.

:::caution
Parsing complex JSON with regex is not robust. It is fine for simple structures; for complex cases, use a JSON parser instead.
:::

### 9. Match an Authorization Header

```text
(?i)^Authorization:\s*Bearer\s+(\S+)
```

Case-insensitively matches `Authorization: Bearer xxx` and captures the token.

### 10. Replacement Example: Add a Prefix to a Parameter Value

Original text:

```text
key=12345&foo=bar
```

Match:

```text
key=([^&]*)
```

Replace with:

```text
key=api-$1
```

Result:

```text
key=api-12345&foo=bar
```

## Writing Tips

1. **Define the goal first**: Decide what should and should not match before writing the pattern.
2. **Prefer non-greedy matching**: When extracting content inside tags or quotes, use `.*?` to avoid over-matching.
3. **Watch escaping**: Dots, question marks, parentheses, slashes, and similar characters often need escaping.
4. **Anchor when possible**: Use `^`, `$`, and `\b` to narrow the match and reduce false positives.
5. **Test before applying**: Validate the pattern in Reqable’s Regex toolbox tool before using it in search or rewrite rules.
6. **Keep it simple**: If contains/wildcard matching is enough, you do not need a complex regex.

## Quick Reference

| Need | Example pattern |
| --- | --- |
| Any character (except newline) | `.` |
| One or more digits | `\d+` |
| Optional `s` | `s?` |
| Starts with `api` | `^api` |
| Ends with `.json` | `\.json$` |
| Match `a` or `b` | `a\|b` |
| Capture digits | `(\d+)` |
| Non-greedy any content | `.*?` |
| Non-whitespace token | `\S+` |

With these basics, you can cover most regex use cases in day-to-day Reqable debugging. For more complex rules, build them step by step and validate against real request/response content.
