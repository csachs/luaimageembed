# luaimageembed

LuaTeX package to embed images directly as base64-encoded strings into the document. This can be useful, e.g. to package a document with images into a single TeX file, or with automatically generated graphics.

The image files will be decoded, written to a temporary directory, and cleaned up afterwards.

Use at your own risk.

## Commands

Three commands are wrapped to allow for use with base64-encoded images:

- `\includegraphicsembedded` (`\includegraphics`)
- `\pgfdeclareimageembedded` (`\pgfdeclareimage`)
- `\pgfimageembedded` (`\pgfimage`)

Each takes the base64-encoded image data instead of the filename; see the example below. Supported are `png`, `jpg`, `jb2` and `pdf` images.

## Example

```latex
\documentclass{scrartcl}

\usepackage{luaimageembed}
\usepackage{graphicx}

\begin{document}
\includegraphicsembedded[width=4cm]{%
iVBORw0KGgoAAAANSUhEUgAAAAMAAAADCAAAAABzQ+pjAAAAFElEQVQI12P4z/Cf4f9/BgYGBgYA
IOsD/UqPmwUAAAAASUVORK5CYII=
}
\end{document}
```

## Version

0.1 (alpha)

## License

MIT
