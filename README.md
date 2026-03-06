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
{{< github-code-embed url="https://github.com/nbr23/bunny-pack/blob/master/contentScript.js" lang="javascript" >}}
```

#### Parameters

- `url` (required): The regular GitHub file URL
- `lang` (optional): Language for syntax highlighting (e.g., `javascript`, `python`, `go`)
- `title` (optional): Display title shown in the embed header
- `copy` (optional): Set to `true` to render a copy-to-clipboard button in the header

#### Examples

Display a JavaScript file with syntax highlighting:
```
{{< github-code-embed url="https://github.com/nbr23/bunny-pack/blob/master/manifest.json" lang="json" >}}
```

Display a file without syntax highlighting:
```
{{< github-code-embed url="https://github.com/nbr23/bunny-pack/blob/master/README.md" >}}
```

Display with a copy button:
```
{{< github-code-embed url="https://github.com/nbr23/bunny-pack/blob/master/manifest.json" lang="json" title="My file" copy=true >}}
```

> The `copy` feature requires the consumer theme to provide `.github-embed-copy` CSS styling.

### GitHub Gist Embed

Use the `github-gist-embed` shortcode to display content from GitHub Gists:

```
{{< github-gist-embed url="https://gist.github.com/username/gist-id" lang="javascript" >}}
```

#### Parameters

- `url` (required): The GitHub Gist URL
- `lang` (optional): Language for syntax highlighting (e.g., `javascript`, `python`, `go`)
- `title` (optional): Display title shown in the embed header
- `copy` (optional): Set to `true` to render a copy-to-clipboard button in the header

#### Examples

Display a JavaScript gist with syntax highlighting:
```
{{< github-gist-embed url="https://gist.github.com/nbr23/abc123def456" lang="javascript" >}}
```

Display a gist without syntax highlighting:
```
{{< github-gist-embed url="https://gist.github.com/nbr23/abc123def456" >}}
```

Display with a copy button:
```
{{< github-gist-embed url="https://gist.github.com/nbr23/abc123def456" lang="python" title="My script" copy=true >}}
```

> The `copy` feature requires the consumer theme to provide `.github-embed-copy` CSS styling.

## License

MIT License
