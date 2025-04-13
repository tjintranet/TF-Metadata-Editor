# XML Editor

A browser-based XML editor optimized for T&F metadata files, allowing users to view, edit, and download XML files while maintaining their original structure. The editor displays only relevant nodes based on an XSLT template while preserving the complete XML structure.

## Features

- **Smart Node Selection**: Displays only relevant XML nodes based on XSLT guidance
- **Instant XML Parsing**: Automatically parses XML files upon selection
- **In-Browser Editing**: Edit XML content directly in the browser with an intuitive interface
- **Preserve Structure**: Maintains the original XML structure while allowing content modifications
- **Download Support**: Download edited XML files with original formatting and filename
- **Bootstrap UI**: Clean, responsive interface using Bootstrap 5
- **No Server Required**: Runs entirely in the browser with no backend dependencies

## Getting Started

1. Clone this repository or download the HTML file
2. Open the HTML file in a modern web browser
3. No additional setup or installation required

## Usage

1. **Upload XML**
   - Click the file input or drag and drop an XML file
   - The file will be automatically parsed and displayed
   - Only relevant nodes (as defined in the configuration) will be shown for editing

2. **Edit Content**
   - Click on any value to edit it
   - Changes are saved automatically in memory
   - Only displayed fields can be edited
   - All other XML nodes are preserved unchanged

3. **Download**
   - Click the "Download XML" button to save your changes
   - The downloaded file will maintain the original filename and complete XML structure
   - All nodes (including non-displayed ones) are preserved in the output

4. **Clear**
   - Use the "Clear" button to reset the editor and start over

## Customization

### Adding or Removing Editable Nodes

The editor can be customized to show different XML nodes by modifying the `editableFields` array in the code:

```javascript
const editableFields = [
    { path: '//product/production_class', label: 'Production Route' },
    { path: '//product/title', label: 'Title' },
    // Add or remove fields here
];
```

To add a new field:
1. Locate the `editableFields` array in the code
2. Add a new object with:
   - `path`: The XPath to the XML node
   - `label`: The display label for the field

### Customizing Display Format

The display format can be modified in the `displayEditableXML` function:
- Field layout and styling
- HTML structure
- Input field appearance

## Currently Displayed Fields

The editor currently displays and allows editing of:
- Production Route
- Title
- ISBN
- Binding
- Page Extent
- Format (Width and Height)
- Spine Size
- Text Colour
- Text Paper
- Lamination

## Browser Compatibility

The editor is compatible with modern browsers that support:
- FileReader API
- DOMParser
- XMLSerializer
- Blob API
- XPath Evaluation
- Bootstrap 5

Tested on:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Technical Details

The editor uses several key technologies:
- `DOMParser` for parsing XML
- `XMLSerializer` for generating output
- `FileReader` for handling file uploads
- `Blob` for file downloads
- XPath for precise node selection
- contenteditable for in-place editing

## File Size Limitations

The editor works with XML files of any size that the browser can handle, typically up to several megabytes. However, very large files may impact performance.

## Known Limitations

- Does not support editing XML attributes (only element content)
- Does not support adding or removing XML nodes
- Does not validate XML schema
- Basic XML formatting (simple indentation)
- Can only edit pre-configured nodes

## Future Improvements

- Add support for editing XML attributes
- Add XML validation
- Add support for adding/removing nodes
- Improve XML formatting options
- Add search functionality
- Add undo/redo support
- Add support for custom XSLT templates
- Add validation rules for specific fields
