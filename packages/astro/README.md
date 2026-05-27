# @vellum/astro

Astro components and layouts that render the [@vellum/theme](https://www.npmjs.com/package/@vellum/theme) classes. Drop them into any Astro v5+ project.

## Install

```sh
npm install @vellum/astro @vellum/theme tailwindcss
```

In your Tailwind v4 entry CSS:

```css
@import "tailwindcss";
@import "@vellum/theme";
```

## Use

```astro
---
import BaseLayout from "@vellum/astro/layouts/BaseLayout.astro";
import { Button, Badge, Card } from "@vellum/astro";
---

<BaseLayout title="Hello">
  <Card>
    <h2>A note</h2>
    <p>With <Badge>tags</Badge> and a <Button variant="primary">button</Button>.</p>
  </Card>
</BaseLayout>
```

## Components

- `Button` — `variant: "primary" | "secondary" | "link"`, `as?: "button" | "a"`, `href?`
- `Badge` — `variant?: "default" | "mono"`
- `Card` — slotted surface
- `NavItem` — `href`, `active?`, `icon` slot + default slot
- `PanelLabel` — tiny mono caption
- `SectionLabel` — accent display heading
- `Hairline` — single-pixel divider
- `Prose` — long-form article wrapper, `dropcap?: boolean`
- `Checkbox` — styled checkbox input
- `Progress` — `value: number` (0–100)

## Layouts

- `BaseLayout` — `<html>`, font links, sidebar slot, main slot
- `PostLayout` — three-column with TOC right rail, post frontmatter

## License

MIT
