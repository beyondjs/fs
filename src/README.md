# @beyond-js/fs

An enhanced file system utility package for Node.js, extending the native `fs.promises` module with additional useful
functions.

## Installation

```bash
npm install @beyond-js/fs
```

## Usage

```javascript
const fs = require('@beyond-js/fs');

// Copy a directory recursively
await fs.copy('/source/path', '/destination/path');

// Check if a file exists
const fileExists = await fs.exists('/path/to/file');

// Save content to a file, creating directories if needed
await fs.save('/path/to/file.txt', 'File content', { encoding: 'utf8' });

// Use any native fs.promises method
await fs.readFile('/path/to/file', 'utf8');
```

## API

This package extends the native `fs.promises` module and adds the following methods:

### `copy(source: string, target: string): Promise<void>`

Recursively copies all files from a source directory to a target directory.

### `exists(file: string): Promise<boolean>`

Checks if a file exists.

### `save(file: string, content: string | Buffer, options?: object): Promise<void>`

Saves content to a file, creating the directory structure if it doesn't exist. If the file already exists, it will be
overwritten.

## Features

-   Extends the native `fs.promises` module
-   Recursive directory copying
-   File existence checking
-   Safe file saving with directory creation
-   Asynchronous operations with Promise support

## License

MIT © [[BeyondJS](https://beyondjs.com)]
