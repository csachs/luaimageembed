# luaimageembed

LuaTeX using LaTeX package to embed images directly as Base64 encoded versions of theirselves into the document.
The image files will be decoded, written to a temporary directory, and cleaned up afterwards.

Warning: Alpha quality! No warranty! 

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

## License

MIT
