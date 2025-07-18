# NVLib GUI Builder

**A Browser-Based Visual GUI Builder for the NVLib Python Library**

NVLib GUI Builder is a powerful, standalone HTML application that provides a complete visual environment for designing user interfaces. It leverages a drag-and-drop canvas to allow developers to create, customize, and lay out GUI components, then export the entire design to a `layout.json` file. This file can be seamlessly integrated into a Python project, allowing the NVLib library to programmatically reconstruct the GUI with pixel-perfect accuracy.

## Features

- **Visual Drag & Drop Canvas**: Design your interface by dragging, dropping, and resizing components on a scrollable, grid-based canvas.
- **Rich Component Library**: Build with a wide selection of components including buttons, text fields, sliders, image views, and container elements like panels and cards.
- **Advanced Customization**:
    - **Typography**: Customize text with a built-in Google Fonts picker.
    - **Styling**: Adjust colors, corner radius, opacity, and more.
    - **Icons & Images**: Use Google Material Symbols in labels or upload images directly into your layout.
- **JSON Export/Import**: Save and load your entire UI design as a single, self-contained `layout.json` file.
- **Live Interactive Preview**: Test the look, feel, and interactivity of your design in a live preview window with a full-screen option.

## Installation

No installation is required. This tool is a single, self-contained HTML file.

1.  **Open in Browser**:
    Open this link 

## Usage

The workflow is designed to be simple and efficient.

1.  **Design Your GUI**:
    Launch the HTML file. Use the left-hand panel to add components to the canvas. Select any component to access its unique properties in the right-hand panel, where you can customize everything from its ID and color to its font.

2.  **Export the Layout**:
    Once you are satisfied with your design, click the **"Save to JSON"** button in the header. This will download a `layout.json` file containing all the necessary data to recreate your GUI.

3.  **Integrate with Python**:
    Move the `layout.json` file into your Python project. Use a script to load and parse this file, then use your NVLib library to dynamically generate the user interface.

## Acknowledgments

* **Tailwind CSS**: For providing the utility-first CSS framework.
* **Google Fonts**: For the dynamic font and icon integration.
