# macOS Color & PDF Settings Deployment Tool

A unified tool for deploying, discovering, and cleaning color management assets on macOS systems. This script manages Adobe color and PDF settings with both embedded payloads and custom directory support.

## Features

- **Install color management assets**: Deploy Adobe color settings (.csf) and PDF job options (.joboptions) files
- **Discover existing settings**: Scan the system to find all installed color profiles, PDF settings, and related assets  
- **Interactive removal**: Browse discovered files and selectively remove unwanted color management assets
- **Flexible deployment**: Use embedded payload or specify custom directory with color assets
- **User or system-wide installation**: Install for current user or all users on the system

## Default Color Profiles

The embedded payload includes standard Adobe color management files:
- Color Settings Files (.csf)
- PDF Job Options (.joboptions) 
- ICC Color Profiles (.icc, .icm)
- Flattener Presets (.flst)

Users can also specify their own custom payload directory containing additional color management assets.

## Get Started

### Direct Installation (Recommended)
```bash
bash <(curl -sSL https://github.com/Buffalo-Games/Color-PDF-Tool/cm-tool.sh) install
```

### Local Installation
1. Download the script:
   ```bash
   curl -sSL https://github.com/Buffalo-Games/Color-PDF-Tool/cm-tool.sh -o cm-tool.sh
   ```

2. Make executable:
   ```bash
   chmod +x cm-tool.sh
   ```

3. Run installation:
   ```bash
   ./cm-tool.sh install
   ```

## Usage

### Install Assets
```bash
# Install embedded assets for current user
./cm-tool.sh install

# Install for all users (requires sudo)
./cm-tool.sh install --system

# Install from custom directory
./cm-tool.sh install --payload-dir /path/to/assets
```

### Discover Assets
```bash
# List all discovered color/PDF assets
./cm-tool.sh discover

# Interactive removal interface
./cm-tool.sh discover --interactive-remove
```

### Remove Assets
```bash
# Remove embedded payload assets
./cm-tool.sh uninstall
```

### Help
```bash
./cm-tool.sh help
```

## Terminal Instructions

1. Open Terminal (Cmd + Space, type "Terminal", press Enter)
2. Copy and paste any command above
3. Press Enter to execute
4. Installation is user-only by default. To install for the system, enter password when prompted
