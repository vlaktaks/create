# create

A simple Bash CLI tool to quickly create executable files with the correct shebang.

No need to write the shebang manually or remember to set execution permissions. Just run `create` and start coding!

**Repository:** https://github.com/vlaktaks/create

## Features

- Quickly create new files with a single command.
- Automatically adds the correct shebang.
- Automatically makes files executable (`chmod +x`).
- Supports multiple programming languages.
- Prevents accidentally overwriting existing files.
- Available system-wide for your user.

## Installation

Clone the repository:

```bash
git clone https://github.com/vlaktaks/create.git
cd create
```

Make the program executable:

```bash
chmod +x create
```

Install it in your local binary directory:

```bash
mkdir -p ~/.local/bin
cp create ~/.local/bin/create
```

Make sure `~/.local/bin` is included in your `$PATH`.

If necessary, add this to your `~/.bashrc`:

```bash
export PATH="$HOME/.local/bin:$PATH"
```

Reload your shell configuration:

```bash
source ~/.bashrc
```

You can now use `create` from anywhere in your terminal.

### Quick installation

Alternatively, install it directly without cloning the repository:

```bash
mkdir -p ~/.local/bin
curl -fsSL https://raw.githubusercontent.com/vlaktaks/create/main/create -o ~/.local/bin/create
chmod +x ~/.local/bin/create
```

Make sure `~/.local/bin` is in your `$PATH`.

## Usage

### Create a Bash script

```bash
create --bash main
```

Creates a file named `main` containing:

```bash
#!/usr/bin/env bash
```

### Create a Python script

```bash
create --python main.py
```

Creates a file named `main.py` containing:

```python
#!/usr/bin/env python3
```

### Create a Shell script

```bash
create --sh install.sh
```

Creates a file named `install.sh` containing:

```sh
#!/bin/sh
```

## Permissions

Every newly created file automatically receives executable permissions.

You can execute your script immediately:

```bash
./main
```

## Safety

`create` checks whether a file already exists before creating it.

Existing files are never intentionally overwritten.

## Requirements

- Bash
- Linux or another Unix-like operating system
- `curl` (for quick installation)
- `~/.local/bin` in your `$PATH`

## License

This project is licensed under the MIT License.

Copyright (c) vlaktaks

See the [LICENSE](https://github.com/vlaktaks/create/blob/main/LICENSE) file for details.
