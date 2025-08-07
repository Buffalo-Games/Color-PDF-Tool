# Payload Assets

This folder and these preset files are **not needed** since they are automatically included in the default payload of the cm-tool.sh script. 

## Purpose

These files are provided here for:

1. **Transparency** - to show exactly which color management assets are embedded in the script
2. **Custom payload reference** - to demonstrate the proper file structure when using the `--payload-dir` feature

## Contents

This folder contains the standard Buffalo Games color management preset files:

### Color Settings Files (.csf)
- `Buffalo Color Settings (GRACoL 2013).csf` - Adobe color settings configured for GRACoL 2013 standards

### PDF Job Options (.joboptions)
Print files:
- `Buffalo PDFX1a Print - Outline Bleed Crops.joboptions`
- `Buffalo PDFX1a Print - Outline Bleed.joboptions` 
- `Buffalo PDFX1a Print - Outline No Bleed.joboptions`
- `Buffalo PDFX4 Print - Bleed Crops.joboptions`
- `Buffalo PDFX4 Print - Bleed.joboptions`
- `Buffalo PDFX4 Print - No Bleed.joboptions`

Proof files:
- `Buffalo PDFX1a Proof - Outline Bleed Slug 150dpi.joboptions`
- `Buffalo PDFX4 Proof - Bleed Slug 150dpi.joboptions`

### Flattener Presets (.flst)
- `Buffalo Flattener Print Outline.flst` - Transparency flattener settings for print output

### ICC Color Profiles (.icc)
- `GRACoL2013_CRPC6.icc` - GRACoL 2013 color profile for consistent CMYK printing

## Using Custom Payload Assets

To use this folder structure as a reference for creating custom payload assets:

1. Create a new directory with the color management files
2. Organize files in the same structure (no subdirectories required)
3. Use the `--payload-dir` option:
   ```bash
   ./cm-tool.sh install --payload-dir /path/to/custom/assets
   ```

The script will automatically detect and install all supported file types (.csf, .joboptions, .flst, .icc, .icm) from the specified directory.
