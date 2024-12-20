# README: Interactive US Map with CSV Data

## Overview
This project is an interactive web-based map of the United States. It dynamically displays state-specific information using SVG data and a CSV file. Users can hover over or click on states to explore detailed legal statuses and additional information.

## Features
- **Dynamic SVG Integration**: The map is rendered via an external SVG file.
- **Color-coded States**: States are color-coded based on legal status.
- **Interactive Information Display**:
  - Hovering over a state shows its details in the info box.
  - Clicking on a state pins its information for easy comparison.
- **CSV Data Parsing**: Legal statuses and additional state-specific information are fetched from a TSV file hosted online.
- **Responsive Design**: The layout adapts to various screen sizes and orientations.

## Folder Structure
The main file for this project is `desktop.html`, containing:
- **HTML**: Structure of the interactive map.
- **CSS**: Styles for the map, legend, and info box.
- **JavaScript**: Functionality for dynamic interaction, data parsing, and user interactions.

## Requirements
To run this project, you need:
- A modern web browser (Chrome, Firefox, Edge, Safari).
- Internet access to fetch the SVG and TSV data files.

## Setup
1. **Download or Clone the Repository**: Save the `desktop.html` file.
2. **Run the File**: Open `desktop.html` in your web browser.

## How It Works
1. **Loading the Map**:
   - The SVG map of the United States is fetched from a remote server.
   - It is dynamically injected into the `#svg-container`.
2. **Parsing Data**:
   - TSV data is downloaded from a hosted Google Sheets link.
   - Data is parsed and linked to the corresponding state IDs in the SVG file.
3. **Color Assignment**:
   - Each state’s color is determined based on its legal status.
   - If no data exists for a state, it defaults to a dark gray color.
4. **User Interaction**:
   - Hovering over a state displays its data in the info box.
   - Clicking on a state pins its data for persistent display.
   - Clicking the same state again unpins the data.

## Key Files
- **SVG File**: Hosted at `https://s3.us-east-1.amazonaws.com/aubintime.spatialstudieslab.org/assets/svgs/us_states.svg`.
- **TSV File**: Hosted at `https://docs.google.com/spreadsheets/d/e/2PACX-1vRSw8J1erY15jXjGpurdxPAc1LRLTe6fu1lbHkVFyMuiRYUsdF17LDIQQKXium6pK3uB4Io5RJDsjj7/pub?gid=586541007&single=true&output=tsv`.

## Core Functions
### JavaScript Functions
- **`getColorFromType(type)`**: Maps legal status types to specific colors.
- **`parseTSV(tsvText)`**: Converts TSV data into JavaScript objects.
- **`showStateInfo(stateId)`**: Displays a state’s information in the info box.
- **`sanitize(text)`**: Sanitizes text for safe HTML rendering.
- **`resetInfoBox()`**: Resets the info box content when not hovering or pinned.

## Customization
To modify the map or its functionality:
1. Update the CSS in the `<style>` section for layout or design changes.
2. Replace the TSV or SVG file URLs with your own data sources.
3. Modify JavaScript functions to include additional interactivity or features.

## Troubleshooting
1. **SVG Not Loading**:
   - Check the network connection and the hosted SVG URL.
2. **TSV Data Issues**:
   - Verify the structure and accessibility of the hosted TSV file.
3. **State Colors Not Updating**:
   - Ensure that state IDs in the SVG match those in the TSV data.

## Credits
- **Design**: Uilvim E. G. Franco and Bruno Sousa
- **Logos**: Displayed at the bottom right are provided by Rice University and associated institutions.

## License
This project is open-source. Feel free to use, modify, and share with proper attribution.

