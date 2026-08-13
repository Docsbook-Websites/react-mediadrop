# Quickstart

## React

```tsx
import { useMediaDrop } from "react-mediadrop";

function Dropzone() {
	const { getRootProps, getInputProps, files } = useMediaDrop({
		restrictions: { accept: ["image/png", "image/jpeg"], maxFiles: 5 },
	});

	return (
		<div {...getRootProps()}>
			<input {...getInputProps()} />
			{files.length} file(s) selected
		</div>
	);
}
```

## Upload (opt-in)

```tsx
import { useMediaDrop } from "react-mediadrop";
import { createXhrUploadTransport } from "react-mediadrop/xhr-upload";

function Uploader() {
	const { files, uploadAll } = useMediaDrop({
		transport: createXhrUploadTransport({ endpoint: "/api/upload" }),
		concurrency: 3,
		retries: 2,
	});

	return (
		<button onClick={() => uploadAll()}>Upload {files.length} file(s)</button>
	);
}
```

Without `transport`, nothing is uploaded — `useMediaDrop` only tracks intake/validation state. See the full guides on [mediadrop.dev/docs](https://www.mediadrop.dev/docs/getting-started/quickstart) for the complete API.
