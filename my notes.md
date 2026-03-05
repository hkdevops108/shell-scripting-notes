Here are your **notes in Markdown (`.md`) format** so you can save them in your notes or Git repository.

````markdown
# Bash String Checks (-z and -n)

## 1. `-z` (Zero Length)

**Meaning:**  
Checks if a variable is empty.

### Syntax

```bash
if [ -z "$var" ]
then
   commands
fi
````

### Logic

* Variable empty → **TRUE** → `if` block executes
* Variable not empty → **FALSE** → `if` block skipped

### Example

```bash
name=""

if [ -z "$name" ]
then
   echo "Variable is empty"
fi
```

---

## 2. `-n` (Not Zero Length)

**Meaning:**
Checks if a variable is **not empty**.

### Syntax

```bash
if [ -n "$var" ]
then
   commands
fi
```

### Logic

* Variable not empty → **TRUE** → `if` block executes
* Variable empty → **FALSE** → `if` block skipped

### Example

```bash
name="Sridhar"

if [ -n "$name" ]
then
   echo "Variable is not empty"
fi
```

---

## Important Rule

Always use **quotes around variables**.

✅ Correct:

```bash
if [ -z "$name" ]
```

❌ Wrong:

```bash
if [ -z $name ]
```

---

## Summary

| Operator | Meaning               |
| -------- | --------------------- |
| `-z`     | Variable is empty     |
| `-n`     | Variable is not empty |

```

You can save this as:

```

bash-string-checks.md

```

If you want, I can also give you a **complete Bash conditional operators `.md` cheat sheet** (`-f`, `-d`, `-e`, `$?`, etc.) which is **very useful for DevOps scripts**.
```
