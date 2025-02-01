# Valorant Kill & Death Analyzer

## Overview

This Python script extracts and analyzes frames from a Valorant gameplay video to detect kills, deaths, headshots, and track player movement using a heatmap. It also identifies the weapon used based on Optical Character Recognition (OCR).

## Features

- **Frame Extraction**: Extracts one frame per second from the video.
- **Kill Detection**: Detects kills by identifying red-colored popups in the kill feed.
- **Death Detection**: Identifies deaths by detecting blue-colored popups in the kill feed.
- **Headshot Detection**: Determines headshots based on specific visual indicators.
- **Weapon Recognition**: Uses OCR to extract gun names from the HUD.
- **Player Movement Heatmap**: Analyzes minimap activity to generate a heatmap of player movement.
- **K/D Calculation**: Computes Kill/Death ratio and headshot percentage.

## Dependencies

Ensure you have the following dependencies installed:

```bash
pip install opencv-python numpy pytesseract
```

## Usage

1. **Set the video file path**: Modify the `video_path` variable to point to your gameplay video.
2. **Run the script**: Execute the script in your Python environment.
   ```bash
   python valorant_analyzer.py
   ```
3. **View the results**:
   - Extracted frames will be saved in the `extracted_frames/` directory.
   - The detected kills, deaths, and headshots will be printed.
   - A heatmap will be generated to show player movement.

## Configuration

- Modify `frame_interval` to adjust how frequently frames are extracted.
- Adjust color range values in `detect_kills_by_color` and `detect_deaths_by_color` if detection is inaccurate.
- Modify `KNOWN_GUN_NAMES` to include additional weapon names for better recognition.

## Output

- **Frame Images**: Extracted frames saved in `extracted_frames/`.
- **Console Output**: Displays kill, death, and headshot statistics along with the K/D ratio.
- **Heatmap**: A visual representation of player movement across the game map.

## Example Output

```
Video FPS: 30
Total Frames: 45000
Duration: 1500.00 seconds
Saved frame 00000 as extracted_frames/frame_00000.jpg
Detected Kill!
Detected Gun: Vandal
Total Kills Detected: 10
Total Deaths Detected: 5
Headshot Percentage: 50.00%
K/D Ratio: 2.0
```

## Notes

- The script assumes a 1920x1080 resolution. Adjust cropping coordinates if using a different resolution.
- The accuracy of kill/death detection depends on the color scheme of your game settings.
- Ensure `Tesseract-OCR` is installed and configured correctly for weapon name recognition.

## License

This project is open-source and free to use. Feel free to modify and improve it!

---

Enjoy analyzing your gameplay! 🎮

