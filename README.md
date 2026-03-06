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
- `wrap` (optional): Set to `true` to add the `github-embed--wrap` modifier class to the container, enabling long-line wrapping via CSS

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

Display with long-line wrapping:
```
{{< github-code-embed url="https://github.com/nbr23/bunny-pack/blob/master/manifest.json" lang="json" wrap=true >}}
```

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
- `wrap` (optional): Set to `true` to add the `github-embed--wrap` modifier class to the container, enabling long-line wrapping via CSS

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

Display with long-line wrapping:
```
{{< github-gist-embed url="https://gist.github.com/nbr23/abc123def456" lang="python" wrap=true >}}
```

## CSS

The shortcodes render HTML using the following classes. Your theme must provide styling for these:

| Class | Element | Notes |
|---|---|---|
| `.github-embed` | Outer container | Always present |
| `.github-embed--wrap` | Outer container modifier | Added when `wrap=true`; apply `white-space: pre-wrap; word-break: break-all;` (or similar) to `pre` descendants to enable line wrapping |
| `.github-embed-header` | Header bar | Contains title and actions |
| `.github-embed-header-left` | Left header section | GitHub icon + title |
| `.github-embed-header-right` | Right header section | Link and copy button |
| `.github-embed-title` | Title text | |
| `.github-embed-body` | Code content area | Wraps the `pre`/`code` block |
| `.github-embed-copy` | Copy button | Only rendered when `copy=true` |
| `.github-embed-error` | Error message | Rendered when the URL is missing or the fetch fails |

## License

MIT License
