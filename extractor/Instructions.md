# VirtuGhan Extractor Plugin for QGIS

VirtuGhan Extractor is a QGIS plugin to extract raster data using the VirtuGhan engine. It allows selecting an Area of Interest (AOI), setting dates, bands, and other extraction parameters.

## Features

- Draw AOI on the map canvas or use current map extent
- Select date range and cloud cover filters
- Choose bands to extract
- Supports multiple workers for faster extraction
- Optional ZIP output and smart filtering
- Loads resulting rasters automatically into QGIS

## Installation

1. Clone or download this repository into your QGIS plugin folder:
    ```bash
    git clone https://github.com/SaharAbdulallim/Virtughan_QGIS_Plugin.git
    ```
2. Open QGIS, go to `Plugins > Manage and Install Plugins > Installed`, and enable `VirtuGhan Extractor`.

## Usage

1. Click on `VirtuGhan • Extractor` in the QGIS toolbar.
2. Set AOI using:
    - Current map canvas extent
    - Drawing a rectangle/polygon on the map
3. Configure start/end dates, cloud cover, and bands.
4. Select output folder.
5. Click **Run** to start extraction.
6. Rasters are automatically loaded into your QGIS project.

## Development / Making Changes

1. Clone this repo locally.
2. Make changes to the Python files inside the `extractor` or `engine` folders.
3. Test changes in QGIS by reloading the plugin (`Plugins > Manage and Install Plugins > Reload Plugin`).
4. Commit your changes:
    ```bash
    git add .
    git commit -m "Describe your changes"
    git push
    ```

### Notes / Changes Made

- Updated `_AoiDrawTool` for QGIS 3.40+ (QgsRubberBand constructor)
- Added missing PyQt imports (e.g., `QVBoxLayout`) to avoid `NameError`
- `show_extractor` function added to main plugin for separate extractor dock
- Supports modern Python 3.12 with QGIS 3.40

## License

MIT License (or your preferred license)
