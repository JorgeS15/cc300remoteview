# Engel CC300 Remote View (Windows Script)

A Windows batch script that automates remote VNC connections to IMM Engel CC300 Control Panels, with optional SSH tunneling support.

## Prerequisites

- **VNC Viewer** (RealVNC) - Required
  - Download: [RealVNC Viewer](https://www.realvnc.com/en/connect/download/viewer/)
  
- **PuTTY** - Only required for newer CC300 versions that need SSH tunnel
  - Download: [PuTTY](https://www.putty.org/)

## Quick Start

1. Download `cc300remoteview.bat`
2. Install VNC Viewer (and PuTTY if needed)
3. Edit the script to configure your settings:
   - Set `SSH_USER` and `SSH_PASSWORD` if using SSH tunnel
   - Optionally set `USE_IP_BASE=TRUE` and `IP_BASE` to only enter last IP octet
4. Run the script and follow the prompts

## CC300 Version Compatibility

**Older CC300 versions**: Direct VNC connection (select **N** for SSH)

**Newer CC300 versions**: SSH tunnel required (select **Y** for SSH, requires PuTTY)

> **Tip**: Not sure? Try direct connection first. If it fails, use SSH tunnel.

## Configuration

Edit these settings in the script if needed:
```batch
set "USE_IP_BASE=FALSE"      # TRUE = enter only last octet
set "IP_BASE=10.201.52"      # Base IP for last octet mode

set "SSH_USER=changeme"      # CC300 SSH username
set "SSH_PASSWORD=changeme"  # CC300 SSH password
