# hello-world
List of tips and code's snippets

### Table of Contents
1. [Perform command numerous times (for statement)](#multitimes)
2. [Create random string of characters](#randomstring)
3. [Generate passwords with custom pattern](#custompasswords)

### Perform command numerous times (for statement) <a name="multitimes"></a>
```bash
for run in {1..10}; do echo "Hello"; done
```

### Create random string of characters <a name="randomstring"></a>
```bash
cat /dev/urandom | head -c 16 | base64
```
Add `base64 -D` to pipe to get the original raw

### Generate passwords with custom pattern <a name="custompasswords"></a>
This single example uses `tr` command to substitute all numbers with capitalized letters, underscore and minus
```bash
date | md5 | tail -c 10 | tr -s 0-9 _-A-Z
```
