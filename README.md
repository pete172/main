# main
Chart Reader
@'
# CSV Upload Portal

Front-end CSV upload UI with drag-and-drop, file validation messaging, and a finance-style animated background.

## Files
- `index.html` - main UI and structure
- `styles.css` - styling
- `script.js` - upload interactions

## Run
1. Keep all three files in the same folder.
2. Open `index.html` in a browser (or use Live Server).

## Requirements
1. `#browseBtn` opens file picker.
2. Drag over dropzone shows active state.
3. Accept CSV only (`.csv`, `text/csv`).
4. Max file size: 10MB.
5. Show success text in `#upload-status`.
6. Show errors in `#upload-error`.

## TODO
- [ ] Move inline styles from `index.html` into `styles.css`
- [ ] Add full validation in `script.js` (type/size/empty file)
- [ ] Show selected filename
- [ ] Add remove/reset selected file
- [ ] Add reduced-motion support
- [ ] Add backend upload endpoint integration
'@ | Set-Content -Path README.md
