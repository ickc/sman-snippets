# sman-snippets

Snippets for [sman](https://github.com/ickc/sman).

Install sman first if not already:

For system with Python 3.7+:

```sh
curl -fsSL https://raw.githubusercontent.com/ickc/envoy/main/install/sman.py | python3 - install
```

Or bootstrap pixi for newer version of python if needed:

```sh
# bootstrap pixi first
export PIXI_HOME="${HOME}/.local/opt/$(uname -sm | tr ' ' -)/pixi"
export PIXI_BIN_DIR="${PIXI_HOME}/bin"
export PIXI_NO_PATH_UPDATE=1
curl -fsSL https://pixi.sh/install.sh | sh
# then run it like this:
curl -fsSL https://raw.githubusercontent.com/ickc/envoy/main/install/sman.py | "${PIXI_BIN_DIR}/pixi" exec --spec python python3 - install
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
