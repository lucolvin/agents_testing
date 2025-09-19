# agents_testing Repository

This is a minimal testing repository for validating GitHub Copilot coding agent workflows and development practices.

**ALWAYS follow these instructions first and fallback to additional search and context gathering only if the information in the instructions is incomplete or found to be in error.**

## Repository Overview
This is a minimal repository containing:
- README.md with basic project information
- No existing applications, build processes, or dependencies
- Full development environment support for multiple programming languages

## Development Environment

The repository environment includes the following pre-installed tools:
- Node.js v20.19.5 with npm 10.8.2
- Python 3.12.3
- Go 1.24.7
- Java 17 (OpenJDK Temurin)
- GCC, Make, CMake for C/C++ development
- Git version control

## Working Effectively

### Initial Repository Setup
- Navigate to repository: `cd /home/runner/work/agents_testing/agents_testing`
- Verify environment: `node --version && npm --version && python3 --version && go version && java --version`
- Check repository status: `git --no-pager status`
- List repository contents: `ls -la`

### Exploring the Repository
- List all non-git files: `find . -not -path "./.git/*" -type f`
- View README content: `cat README.md`
- Check git history: `git --no-pager log --oneline -10`
- View current branch: `git --no-pager branch -a`

### Node.js Development
- Initialize new Node.js project: `npm init -y` (takes ~0.5 seconds)
- Install dependencies: `npm install [package-name]` (timing varies by package size, jest takes ~25 seconds)
- Run tests: `npm test` (takes ~0.1 seconds for basic scripts)
- NEVER CANCEL: Long installs may take 30+ seconds. Set timeout to 180+ seconds for npm installations.

### Python Development
- Run Python code: `python3 -c "print('Hello World')"` (takes ~0.02 seconds)
- Check Python environment: `python3 --version`
- Install packages: `pip3 install [package-name]`

### Go Development
- Check Go environment: `go version` (takes ~0.003 seconds)
- Initialize Go module: `go mod init [module-name]`
- Build Go code: `go build`
- Run Go code: `go run [file.go]`

### Java Development
- Check Java environment: `java --version` (takes ~0.03 seconds)
- Compile Java code: `javac [file.java]`
- Run Java code: `java [ClassName]`

### Git Operations
- Check status: `git --no-pager status` (takes ~0.003 seconds)
- View changes: `git --no-pager diff`
- Add files: `git add [files]`
- Commit changes: `git commit -m "message"`
- ALWAYS use `--no-pager` flag with git commands to avoid timeouts

## Validation Requirements

### Before Making Changes
- Run `git --no-pager status` to check repository state
- Verify current branch with `git --no-pager branch -a`
- List files to understand current structure: `ls -la`

### After Making Changes
- Always validate that commands work by running them
- Test any new scripts or applications you create
- Verify file contents with `cat [filename]` or appropriate viewers
- Check git status to confirm expected file changes

### Build and Test Validation
- For Node.js projects: Run `npm install` then `npm test`
- For Python projects: Run `python3 -m py_compile [file.py]` to check syntax
- For Go projects: Run `go build` to verify compilation
- For Java projects: Run `javac [file.java]` to verify compilation

## Common Tasks

### Repository Structure
```
agents_testing/
├── .git/           # Git repository data
├── .github/        # GitHub configuration
├── README.md       # Project documentation
```

### Available Commands Output
```bash
# Repository root listing
$ ls -la
total 20
drwxr-xr-x 4 runner runner 4096 [date] .
drwxr-xr-x 3 runner runner 4096 [date] ..
drwxrwxr-x 7 runner runner 4096 [date] .git
drwxrwxr-x 2 runner runner 4096 [date] .github
-rw-rw-r-- 1 runner runner   16 [date] README.md

# README content
$ cat README.md
# agents_testing

# Environment verification
$ node --version && npm --version
v20.19.5
10.8.2

$ python3 --version
Python 3.12.3

$ go version
go version go1.24.7 linux/amd64

$ java --version
openjdk 17.0.16 2025-07-15
OpenJDK Runtime Environment Temurin-17.0.16+8 (build 17.0.16+8)
OpenJDK 64-Bit Server VM Temurin-17.0.16+8 (build 17.0.16+8, mixed mode, sharing)
```

## Time Expectations

### Fast Operations (< 1 second)
- File listing and basic git commands
- Version checks for installed tools
- Simple Python/Go/Java execution
- Basic file operations (cat, echo, ls)

### Medium Operations (1-30 seconds)
- npm package installations (varies by package)
- Small builds and compilations
- File system searches

### Long Operations (30+ seconds)
- Large npm package installations: NEVER CANCEL, set timeout to 180+ seconds
- Complex builds: NEVER CANCEL, wait for completion
- Comprehensive test suites: Wait for completion, may take several minutes

## Development Workflow

1. **Understand Requirements**: Read the problem statement thoroughly
2. **Explore Repository**: Use `ls -la` and `find` commands to understand structure
3. **Set Up Environment**: Initialize appropriate language tools (npm, go mod, etc.)
4. **Make Incremental Changes**: Test each change as you make it
5. **Validate Continuously**: Run builds, tests, and manual verification
6. **Document Changes**: Update documentation if creating new functionality

## Critical Reminders

- **NEVER CANCEL** long-running operations like npm installs or builds
- **ALWAYS** use `--no-pager` with git commands to prevent hanging
- **VALIDATE** every command before documenting it in code
- **TEST** applications and scripts after creation to ensure they work
- **TIME** operations appropriately and set adequate timeouts
- **CLEAN UP** temporary files and test artifacts before committing changes

This repository serves as a foundation for testing development workflows across multiple programming languages and can be extended with any necessary project structure.
