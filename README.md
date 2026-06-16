# sman-snippets

Snippets for [sman](https://github.com/ickc/sman).

Install sman first if not already:

For system with Python 3.7+:

```sh
curl -fsSL https://raw.githubusercontent.com/ickc/envoy/main/install/sman.py | python3 - install
```

Or bootstrap uv for newer version of python if needed:

```sh
curl -LsSf https://astral.sh/uv/install.sh | sh
export PATH="$PATH:$HOME/.local/bin"
uv run --managed-python https://raw.githubusercontent.com/ickc/envoy/refs/heads/main/install/sman.py install
```

Then add these to your rc files,

```sh
export PATH="$PATH:$HOME/.local/opt/$(uname -sm | tr ' ' -)/bin"
export SMAN_APPEND_HISTORY=false
export SMAN_EXEC_CONFIRM=false
export SMAN_SNIPPET_DIR="${XDG_DATA_HOME:-${HOME}/.local/share}/sman/snippets"
. "${XDG_DATA_HOME:-${HOME}/.local/share}/sman/sman.rc"
```

## Installation

Expected install location: `$XDG_DATA_HOME/sman/snippets` (default: `~/.local/share/sman/snippets`)

```sh
mkdir -p "${XDG_DATA_HOME:-${HOME}/.local/share}/sman"
git clone git@github.com:ickc/sman-snippets.git "${XDG_DATA_HOME:-${HOME}/.local/share}/sman/snippets"
```

Or publicly without ssh auth:

```sh
mkdir -p "${XDG_DATA_HOME:-${HOME}/.local/share}/sman"
git clone https://github.com/ickc/sman-snippets.git "${XDG_DATA_HOME:-${HOME}/.local/share}/sman/snippets"
```
