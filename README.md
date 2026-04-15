# one-frontend-framework

[![vosonha89](https://circleci.com/gh/vosonha89/one-frontend-framework.svg?style=svg)](https://circleci.com/gh/vosonha89/one-frontend-framework)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fvosonha89%2Fone-frontend-framework.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Fvosonha89%2Fone-frontend-framework?ref=badge_shield)

---

## Overview

**one-frontend-framework** is an abstract, framework-agnostic TypeScript base for building scalable frontend applications. It enforces strict OOP, SOLID principles, and dependency injection, and is designed to be extended for Angular, React, and Vue.js.

---

## Features

- Abstract base classes for language, loading, logging, storage, and state
- Singleton data sharing services (standard and real-time with RxJS)
- Strict typing and interface-driven contracts
- Dependency injection via `tsyringe`
- Utilities for currency, UUID, random numbers, async, object/UI helpers
- Centralized constants for codes, messages, HTTP, status, storage
- Ready for extension with framework-specific adapters

---

## Architecture

```
one-frontend-framework/
├── src/
│   ├── constants/
│   ├── functions/
│   ├── services/      # Abstract and concrete services
│   └── types/
├── examples/          # (planned) Example apps for Angular, React, Vue
├── README.md
└── package.json
```

- **Abstract Services:** Define contracts for language, loading, logging, storage, etc.
- **Data Sharing:** Singleton services for shared and real-time data (RxJS)
- **Utilities:** Common helpers for formatting, objects, UI, etc.

---

## Usage Example

```typescript
import { AbstractLanguageService, SharingDataService } from 'one-frontend-framework';

// Extend abstract services for your framework:
class MyLanguageService extends AbstractLanguageService<MyStorageService> {
  public setLanguage(value: string): void { /* ... */ }
  public getLanguageText(value: string): void { /* ... */ }
}
```

---

## Planned Framework Adapters

- **Angular:** Injectable services, RxJS, i18n, Material integration
- **React:** Context providers, hooks, react-i18next, portals
- **Vue:** Composables, plugins, vue-i18n, Teleport

Adapters will be published as separate packages:
- `one-angular`
- `one-react`
- `one-vue`

---

## Contribution Roadmap

- [x] Core abstractions and services
- [ ] Add framework adapter packages
- [ ] Add example apps for Angular, React, Vue
- [ ] Add unit/integration tests
- [ ] Expand utilities and documentation

---

## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fvosonha89%2Fone-frontend-framework.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Fvosonha89%2Fone-frontend-framework?ref=badge_large)
