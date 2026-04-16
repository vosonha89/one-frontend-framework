# one-frontend-framework

Monorepo for a framework-agnostic frontend architecture with adapters for Angular, React, and Vue.

---

## Structure

```
one-frontend-framework/
├── packages/
│   ├── core/      # Core framework (abstract services, utilities, types)
│   ├── angular/   # Angular adapter (scaffold)
│   ├── react/     # React adapter (scaffold)
│   └── vue/       # Vue adapter (scaffold)
├── package.json   # npm workspaces config
├── tsconfig.json  # TypeScript project references
└── README.md      # This file
```

## Getting Started

1. **Install dependencies:**  
   ```sh
   npm install
   ```

2. **Build core package:**  
   ```sh
   npm run build
   ```

3. **Add your framework adapter implementation in `packages/angular`, `packages/react`, or `packages/vue`.**

## Contributing

- Core framework code is in `packages/core`.
- Each adapter should live in its own package.
- Use npm workspaces for dependency management.

## Roadmap

- [x] Monorepo structure with core and adapter packages
- [ ] Implement Angular, React, Vue adapters
- [ ] Add example/demo apps
- [ ] Add tests and CI