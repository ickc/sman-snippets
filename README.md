# sman-snippets

Snippets for [sman](https://github.com/ickc/sman).

Install sman first if not already:

```sh
# install binary
bash -c "$(curl https://raw.githubusercontent.com/ickc/sman/master/install.sh)"
# install source file for shell hook
mkdir -p "${XDG_DATA_HOME:-${HOME}/.local/share}/sman"
curl -O https://raw.githubusercontent.com/ickc/sman/refs/heads/main/sman.rc \
    --output-dir "${XDG_DATA_HOME:-${HOME}/.local/share}/sman"
# add these to your rc files
export PATH="$PATH:$HOME/.local/bin"
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
