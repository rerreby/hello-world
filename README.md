# hello-world
List of tips and code's snippets of oneself

### Table of Contents
1. [Perform command numerous times (for statement)](#multitimes)
2. [Create random string of characters](#randomstring)
3. [Generate passwords with custom pattern](#custompasswords)
4. [Encrypt data using openssl](#openssl1)
5. [Before to do anything on command line git](#gitstatus)
6. [Start NodeJS](#startnodejs)
7. [TAR commands](#tar)
8. [neofetch](#neofetch)

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
### Encrypt data using openssl <a name="openssl1"></a>
```bash
# Encrypt the message with AES with password "pass"
echo "Hello, Rerreby" | openssl enc -aes-256-cbc -a # U2FsdGVkX1/GxSmGLOFgDIm9KgCpOdw2iwkw4QCBEYw=

# Decrypt the message
echo "U2FsdGVkX1/GxSmGLOFgDIm9KgCpOdw2iwkw4QCBEYw=" | openssl enc -aes-256-cbc -d -a
```
openssl asks you type a pass and then return enctypted string. To decrypt message use `-d` parameter

### Before to do anything on command line git <a name="gitstatus"></a>
Before you're going to do anything on your git project in command line, run this line
```bash
git status
```

### Start NodeJS <a name="startnodejs"></a>
It's easy to use NodeJS in cli. NodeJS appears to be a good thing to use. It's easy to run it
```bash
node file.js
```

### TAR archive commands <a name="tar"></a>
Most common commands with tar archive are create and extract. So, let's consider them
```bash
tar cvf name.tar * // create tarball with name name.tar
```
`c` - create
`v` - verbose 
`f` - file to output (should be always the last letter if you use non-hyphens forms)
`*` - files to be archived

Next example is extract
```bash
tar xvf name.tar // extracts files from name.tar in current dir
```
`x` - extract
`v` - verbose (can be ommited)
`f` - archive (as in example above, f should be last letter)

### neofetch - Info about system <a name="neofetch"></a>
```bash
nepfetch # prints info about system

