# Command Entry Template

Copy this skeleton for every new command entry. Fill every section — a PR missing "Common Errors & Fixes" will be asked to add it.


## `command-name`

**Category:** (File Management / Networking / Package Manager / Text Processing / System / Termux-API / etc.)
**Works on:** Termux | Linux | Both

### Description
1-2 line plain-language explanation of what the command does.

### Syntax
    command [options] [arguments]

### Common Options
| Flag | Meaning |
|------|---------|
| -x   | what -x does |

### Example
    actual command with real arguments

**Output:**
    expected output shown here

### Real Use Case
One real scenario where this command actually solves a problem.

### ⚠️ Common Errors & Fixes
| Error | Reason | Fix |
|-------|--------|-----|
| `example error text` | why it happens | how to fix it |

### Related Commands
`command-a`, `command-b`


### Quality checklist before submitting a PR
- [ ] Description written
- [ ] Syntax block included
- [ ] At least 1 real Example + Output
- [ ] Common Errors & Fixes filled in (or explicitly marked "None known" if truly none)
- [ ] Related Commands linked
- [ ] Category and "Works on" fields filled
