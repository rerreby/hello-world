# hello-world
List of tips and code's snippets

### Table of Contents
1. [Perform command numerous times (for statement)](#multitimes)
2. [Create random string of characters](#randomstring)

### Perform command numerous times (for statement) <a name="multitimes"></a>
```bash
for run in {1..10}; do echo "Hello"; done
```

### Create random string of characters <a name="randomstring"></a>
```bash
cat /dev/urandom | head -c 16 | base64
```
Add `base64 -D` to pipe to decode the original raw
