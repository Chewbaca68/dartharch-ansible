# dartharch-ansible

Automated BlackArch CTF attack box setup that runs from an Arch Linux ISO.

## Quick Start

From the Arch Linux live ISO:

```bash
# Download and run the install script
curl -LO https://github.com/Chewbaca68/dartharch-ansible/raw/master/install
chmod +x install
./install
```

The script will:
1. Prompt for root and user passwords
2. Download user_configuration.json with retry logic
3. Run archinstall to set up the base system
4. Clone this repository and run the Ansible playbook (via archinstall's custom_commands)
5. Configure BlackArch repository and install CTF tools

## What Gets Installed

- **Arch Linux base system** (via archinstall)
- **User account** with sudo access
- **BlackArch repository** with full mirror list
- **CTF tools** (blackarch-officials metapackage)
- **Utility tools**: nvim, git, curl, wget, rsync, fd, fzf, bat, tree, etc.
- **Paru AUR helper** for accessing Arch User Repository
- **Network tools**: tcpdump, openbsd-netcat, net-tools

## Files

- `install` - Main entry point script (run this to start setup)
- `user_configuration.json` - Archinstall configuration
- `playbook_core.yml` - Ansible playbook for system configuration

## After Installation

Reboot your system and log in with the username you provided during setup. The CTF attack box is ready to use!

## Development

See `AGENTS.md` for development guidelines.

## License

See LICENSE file in this repository.
