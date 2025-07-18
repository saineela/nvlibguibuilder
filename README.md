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

1.  **Download the File**:
    Save the `nvlib_gui_builder.html` file to your local machine.

2.  **Open in Browser**:
    Open the file in any modern web browser (e.g., Google Chrome, Firefox, Microsoft Edge).

## Usage

The workflow is designed to be simple and efficient.

1.  **Design Your GUI**:
    Launch the HTML file. Use the left-hand panel to add components to the canvas. Select any component to access its unique properties in the right-hand panel, where you can customize everything from its ID and color to its font.

2.  **Export the Layout**:
    Once you are satisfied with your design, click the **"Save to JSON"** button in the header. This will download a `layout.json` file containing all the necessary data to recreate your GUI.

3.  **Integrate with Python**:
    Move the `layout.json` file into your Python project. Use a script to load and parse this file, then use your NVLib library to dynamically generate the user interface.

    ```python
    import json
    # import nvlib # Your GUI library

    # Load the layout from the JSON file
    with open('layout.json', 'r') as f:
        layout_data = json.load(f)

    # Get canvas dimensions
    canvas_width = layout_data['canvas']['width']
    canvas_height = layout_data['canvas']['height']

    # Create the main window
    # window = nvlib.create_window(width=canvas_width, height=canvas_height)

    # Create components dynamically
    for component in layout_data['components']:
        component_type = component['type']
        properties = component['properties']
        
        # Example: Create a button using your library's functions
        if component_type == 'Button':
            # nvlib.create_button(
            #     parent=window,
            #     id=component['id'],
            #     x=component['x'],
            #     y=component['y'],
            #     width=component['width'],
            #     height=component['height'],
            #     text=properties.get('text'),
            #     bg_color=properties.get('backgroundColor')
            #     # ... add other properties
            # )
        # ... handle other component types
    
    # window.run()

    ```

## Contributing

We welcome contributions to the NVLib GUI Builder! To contribute:

1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature-name`).
3.  Make your changes.
4.  Commit your changes (`git commit -am 'Add new feature'`).
5.  Push to the branch (`git push origin feature-name`).
6.  Create a new Pull Request.

Please ensure that your contributions align with the project's goals and adhere to the coding standards.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

* **Tailwind CSS**: For providing the utility-first CSS framework.
* **Google Fonts**: For the dynamic font and icon integration.
