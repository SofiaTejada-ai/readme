##Project 1 CECS Operating systems (Sofia Tejada and Joe) 

## How it Works

The program uses inter-process communication with pipes to copy files:
- Parent process reads from the source file and writes to a pipe
- Child process reads from the pipe and writes to the destination file
- Data is transferred in chunks of 4096 bytes for optimal performance

## Compilation

### All Platforms
```bash
gcc filecopy.c -o filecopy
```

## Usage

```bash
./filecopy source_file destination_file
```

**Arguments:**
- `source_file`: Path to the file you want to copy
- `destination_file`: Path where the copied file will be created

**Example:**
```bash
# Create a test file
echo "Hello, World!" > test.txt

# Copy the file
./filecopy test.txt copied_test.txt

# Verify the copy
cat copied_test.txt
```

## Platform-Specific Notes

### Windows
- Requires Windows Subsystem for Linux (WSL) or MinGW/MSYS2
- Use Git Bash, WSL terminal, or MinGW terminal
- Standard Windows Command Prompt won't work (lacks Unix system calls)

### macOS
- Works natively with Terminal
- No additional dependencies required
- Use built-in Terminal app

### Linux
- Works natively with any terminal
- No additional dependencies required
- Compatible with all Linux distributions

## Error Handling

The program includes comprehensive error handling for:
- Missing or incorrect command-line arguments
- File creation/opening failures
- Pipe creation failures
- Process forking failures
- Read/write operation failures

## Requirements

- C compiler (gcc, clang, etc.)
- Unix-like operating system or compatible environment
- Standard C library

## Output

On successful copy:
```
File has been opened successfully.
Child process successfully completed
Enjoy your new copy :)
```

On errors, descriptive error messages are displayed with appropriate exit codes.
