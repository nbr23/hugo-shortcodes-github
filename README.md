# hugo-shortcodes-github

Hugo shortcodes for displaying GitHub content with syntax highlighting and links back to the source.

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

### GitHub File Embed

Use the `github-code-embed` shortcode to display file content from GitHub repositories:

```
{{< github-code-embed "https://github.com/nbr23/bunny-pack/blob/master/contentScript.js" "javascript" >}}
```

#### Parameters

1. **GitHub URL** (required): The regular GitHub file URL (e.g., `https://github.com/nbr23/bunny-pack/blob/master/manifest.json`)
2. **Language** (optional): The programming language for syntax highlighting (e.g., `javascript`, `python`, `go`)

#### Examples

Display a JavaScript file with syntax highlighting:
```
{{< github-code-embed "https://github.com/nbr23/bunny-pack/blob/master/manifest.json" "json" >}}
```

Display a file without syntax highlighting:
```
{{< github-code-embed "github.com/nbr23/bunny-pack/blob/master/README.md" >}}
```

### GitHub Gist Embed

Use the `github-gist-embed` shortcode to display content from GitHub Gists:

```
{{< github-gist-embed "https://gist.github.com/username/gist-id" "javascript" >}}
```

#### Parameters

1. **Gist URL** (required): The GitHub Gist URL (e.g., `https://gist.github.com/username/abc123`)
2. **Language** (optional): The programming language for syntax highlighting (e.g., `javascript`, `python`, `go`)

#### Examples

Display a JavaScript gist with syntax highlighting:
```
{{< github-gist-embed "https://gist.github.com/nbr23/abc123def456" "javascript" >}}
```

Display a gist without syntax highlighting:
```
{{< github-gist-embed "https://gist.github.com/nbr23/abc123def456" >}}
```

## License

MIT License
