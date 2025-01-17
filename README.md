# XML Editor

A simple, browser-based XML editor that allows users to view, edit, and download XML files while maintaining their original structure.

## Features

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

2. **Edit Content**
   - Click on any value to edit it
   - Changes are saved automatically in memory

3. **Download**
   - Click the "Download XML" button to save your changes
   - The downloaded file will maintain the original filename and XML structure

4. **Clear**
   - Use the "Clear" button to reset the editor and start over

## Browser Compatibility

The editor is compatible with modern browsers that support:
- FileReader API
- DOMParser
- XMLSerializer
- Blob API
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
- XPath for tracking XML elements
- contenteditable for in-place editing

## File Size Limitations

The editor works with XML files of any size that the browser can handle, typically up to several megabytes. However, very large files may impact performance.

## Known Limitations

- Does not support editing XML attributes (only element content)
- Does not support adding or removing XML nodes
- Does not validate XML schema
- Basic XML formatting (simple indentation)

## Future Improvements

- Add support for editing XML attributes
- Add XML validation
- Add support for adding/removing nodes
- Improve XML formatting options
- Add search functionality
- Add undo/redo support

## License

MIT License - feel free to use and modify as needed.

## Contributing

Feel free to submit issues and enhancement requests!