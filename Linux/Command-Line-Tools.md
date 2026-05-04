# Linux Command Line Tools

### Pipes (`|`) - Passing output between programs
- A pipe takes the output of one command and feeds it as input to another.

**Example:**
```bash
ls -la | grep readme
```

**What happens:**
- `ls -la`: Produces output (files list) to STDOUT
- `|`: Connects STDOUT -> STDIN
- `grep readme`: Reads that input and filters it

Pipe is live data streaming between commands.
Pipe connects programs together.

### Redirections - Sending input/output to files

#### Output redirection (`>`)
```bash
echo hello > file.txt
```
- STDOUT goes into file.txt
- Overwrites the file

#### Append (>>)
```bash
echo hello >> file.txt
```
- Adds to the file instead of overwriting

#### Input redirection (`<`)
```bash
cat < file.txt
```
- File becomes STDIN for `cat`

## `./`
**Example:**
```bash
cat ./-
```
- `./` means "current directory"
- Removes ambiguity
- Forces filesystem lookup

## `--`
**Example:**
```bash
cat -- -
```
- `--` means "stop treating anything as an option"
- So anything after `--` equals literal filename

