# cepepe

`cepepe` is a lightweight, no-nonsense CLI for bootstrapping modern C++ projects
in seconds. It combines simple **Bash** scripting, reproducible **Nix flakes**,
and flexible **CMake** templates.

- Single-command stand up:
  ```bash
  cepepe my-app
  ```
- Two stacks: plain C++ or HTTP server (Drogon)
- Reproducible dev & prod shells via `flake.nix`
- Built‑in `build.sh` (supports `--clean`, `--debug`)
- Sensible defaults (.clangformat, .gitignore)
- Debug‑friendly CMake: AddressSanitizer enabled

## Requirements

- [Nix](https://nixos.org) (cepepe checks and prompts you if it’s missing). You
  can use [Determinate Nix](https://docs.determinate.systems/#products).
- `determinate-nixd` (with a NOPASSWD sudoer entry so `upgrade` never asks)

## Installation

```bash
git clone https://github.com/alwaysvitorious/cepepe.git
cd cepepe
chmod +x bin/cepepe
sudo ln -fs "$(pwd)/bin/cepepe" /usr/local/bin/cepepe
```

## Usage

```bash
cd ~/projects
cepepe myapp
# → “Will this be an HTTP server? [y/N]”
...
```
