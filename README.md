# hugo-shortcodes-github

A Hugo shortcode for displaying GitHub file content with syntax highlighting and a link back to the source.

## Installation

Add this theme to your Hugo site's `themes` directory or as a git submodule:

```bash
git submodule add https://github.com/nbr23/hugo-shortcodes-github themes/hugo-shortcodes-github
```

Then add it to your `config.yaml`:

```yaml
theme: ['your-main-theme', 'hugo-shortcodes-github']
```

## Usage

Use the `github-code-embed` shortcode in your markdown files:

```
{{< github-code-embed "https://github.com/nbr23/bunny-pack/blob/master/contentScript.js" "javascript" >}}
```

### Parameters

1. **GitHub URL** (required): The regular GitHub file URL (e.g., `https://github.com/nbr23/bunny-pack/blob/master/manifest.json`)
2. **Language** (optional): The programming language for syntax highlighting (e.g., `javascript`, `python`, `go`)

### Examples

Display a JavaScript file with syntax highlighting:
```
{{< github-code-embed "https://github.com/nbr23/bunny-pack/blob/master/manifest.json" "json" >}}
```

Display a file without syntax highlighting:
```
{{< github-code-embed "github.com/nbr23/bunny-pack/blob/master/README.md" >}}
```

## License

MIT License
