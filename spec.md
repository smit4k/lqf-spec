# LQF Language Specification

## Overview

LQF (Lightweight Quick Format) is a minimalistic, human-readable configuration language designed for simplicity and ease of parsing.

## File Structure

An LQF file consists of zero or more **sections**. Each section starts with a **section header**, followed by zero or more key-value **assignments**.

## Syntax

### Sections

- A section begins with a `>` followed immediately by a section name (an identifier).  
- Section names consist of ASCII alphanumeric characters (`[A-Za-z0-9]+`).  
- Example:

```lqf
> settings
```

### Assignments

- Assignments are key-value pairs within a section.  
- Syntax: `key >> value`  
- Keys are identifiers (ASCII alphanumeric).  
- Example:

```lqf
username >> "smit4k"
active >> true
```

### Values

Values can be one of the following types:

| Type       | Syntax Example             | Description                   |
|------------|----------------------------|-------------------------------|
| String     | `"Hello, world!"`           | Double-quoted text           |
| Number     | `42`, `3.14`                | Integers, Floating points    |
| Boolean    | `true`, `false`             | Logical values               |
| Null       | `null`                      | Null value                   |
| Array      | `[1, 2, 3]`, `["a", "b"]`   | Comma-separated list of values inside square brackets |

### Comments

- Comments start with `#` and continue to the end of the line.  
- Comments can appear anywhere outside tokens.

Example:

```lqf
# This is a comment
```
