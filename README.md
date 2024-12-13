# KirbyRelocator42

KirbyMover42 is a script that moves the heaviest directories from `/home` to `sgoinfre` to free up local space. It replaces the original directories with symbolic links, ensuring files remain accessible while optimizing storage. Perfect for managing large files and saving disk space.

## Installation

Open your terminal and run the following command:

```bash
git clone https://github.com/XabierMatute/KirbyRelocator42.git && cd KirbyRelocator42 && chmod +x installer.sh; /bin/sh installer.sh; kirby42
```

## How It Works

1. **Identify the Heaviest Directory**: The script scans the home directory (`$HOME`) to find the heaviest directory.
2. **Prompt User for Action**: It prompts the user to confirm if they want to relocate the identified directory.
3. **Relocate Directory**: If the user agrees, the script moves the directory to `sgoinfre` and creates a symbolic link from the original location to the new location.

## Scripts

### kirby.sh

This is the main script that identifies the heaviest directory and prompts the user for relocation.

#### Usage

```bash
./kirby.sh
```

### realocate.sh

This script moves a directory from a source path to a destination path, deletes the original directory, and creates a symbolic link in its place.

#### Usage

```bash
./realocate.sh <source_path> <destination_path>
```

### deallocate.sh

This script reverses the operation performed by `realocate.sh`. It removes the symbolic link at the source path, moves the content back from the destination path to the source path, and deletes the destination path.

#### Usage

```bash
./deallocate.sh <source_path> <destination_path>
```