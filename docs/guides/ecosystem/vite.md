```markdown
---
name: Build a frontend using Vite and Bun 1.0
---

{% callout %}
While Vite currently works with Bun, it has not been heavily optimized, nor has Vite been adapted to use Bun's bundler, module resolver, or transpiler. However, with the release of Bun 1.0, there have been significant improvements and optimizations.
{% /callout %}

---

Vite works out of the box with Bun. Get started with one of Vite's templates.

```bash
$ bunx create-vite my-app
✔ Select a framework: › React
✔ Select a variant: › TypeScript + SWC
Scaffolding project in /path/to/my-app...
```

---

Then `cd` into the project directory and install dependencies.

```bash
cd my-app
bun install
```

---

Start the development server with the `vite` CLI using `bunx`.

```bash
bunx vite
```

---

To simplify this command, update the `"dev"` script in `package.json` to the following.

```json-diff#package.json
  "scripts": {
-   "dev": "vite",
+   "dev": "bunx vite",
    "build": "vite build",
    "serve": "vite preview"
  },
  // ...
```

---

Now you can start the development server with `bun run dev`.

```bash
bun run dev
```

---

The following command will build your app for production.

```sh
$ bunx vite build
```

---

This is a streamlined guide to help you get started with Vite + Bun 1.0. For more information, see the [Vite documentation](https://vitejs.dev/guide/).
```
