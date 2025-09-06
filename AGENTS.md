## AI vector Forge: SVG Authoring Guide

This section provides guidelines for creating and contributing SVGs to the AI vector Forge project. The goal is to maintain a high-quality, consistent, and accessible collection of "remixable seeds."

### Core Principles

1.  **Show, Don't Tell**: We provide real, working examples, not placeholders.
2.  **No Fluff**: Content should be direct and technical, without marketing language.
3.  **Self-Contained**: Every SVG must be a single file with no external dependencies or JavaScript. All CSS must be inline.
4.  **Accessible**: All SVGs must include `<title>` and `<desc>` tags for accessibility.
5.  **Remixable**: Code should be clean, commented, and easy for others to build upon.

### Project Structure

The project is organized into "namespaces," which are top-level directories. Each namespace is a collection of "workshops," and each workshop is dedicated to a single SVG.

```
/
├── logos/
│   ├── README.md (Describes the 'logos' namespace)
│   └── my-cool-logo/
│       ├── README.md (Describes this specific logo, with a preview)
│       ├── my-cool-logo.svg (The SVG file, name must match directory)
│       ├── AGENTS.md (Optional, for AI instructions for this logo)
│       └── source.png (Optional, source material for the SVG)
│
└── gallery/
    └── ... (similar structure for gallery workshops)
```

### How to Contribute

1.  **Choose a Namespace**: Decide if your SVG is a `logo`, a `gallery` piece, or a `ui-component`.
2.  **Create a Workshop**: Create a new directory for your SVG inside the appropriate namespace (e.g., `/logos/my-new-logo/`).
3.  **Add Your SVG**: Create your SVG file inside the workshop directory. The file name must match the directory name (e.g., `my-new-logo.svg`).
4.  **Add a README**: Create a `README.md` inside the workshop directory with a preview of your SVG and some information about it.
5.  **Follow the Rules**: Ensure your SVG is self-contained and accessible.
6.  **Submit a Pull Request**: No contribution is too small.

### Advanced Techniques & Best Practices

This section provides a more detailed technical guide to working with SVG XML.

#### SVG Optimization

- **Minimize Paths**: Use tools like [SVGOMG](https://jakearchibald.github.io/svgomg/) to optimize your SVG paths and remove unnecessary data.
- **Use `<defs>` and `<use>`**: For repeated shapes, define them once in the `<defs>` section and reuse them with the `<use>` element. This can significantly reduce file size.
- **Group Elements**: Use the `<g>` element to group related shapes. This makes the SVG easier to read and allows you to apply transformations or styles to the whole group.

#### Advanced CSS

- **CSS Variables**: Use CSS custom properties (variables) within your `<style>` tag to make your SVGs more themeable and easier to modify.
  ```css
  :root {
    --primary-color: #3498db;
  }
  .shape {
    fill: var(--primary-color);
  }
  ```
- **Keyframe Animations**: Use `@keyframes` to create complex, multi-step animations. Animate properties like `transform`, `opacity`, and `fill`.
- **Filters and Effects**: Explore SVG filters (`<filter>`) to apply effects like blurs, drop shadows, and color transformations directly in the XML.

#### Advanced Accessibility

- **`role` attribute**: Add `role="img"` to the main `<svg>` tag to explicitly identify it as an image to assistive technologies.
- **`aria-labelledby`**: To create a more robust connection between the SVG and its title and description, use `aria-labelledby`.
  ```xml
  <svg role="img" aria-labelledby="title desc">
    <title id="title">My SVG Title</title>
    <desc id="desc">A detailed description.</desc>
    ...
  </svg>
  ```
