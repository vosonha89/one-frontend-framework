# SKILLS: one-frontend-framework

## 1. Framework Architecture
- Strictly Object-Oriented Programming (OOP) throughout the codebase.
- All code follows SOLID principles: Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion.
- Abstract base classes for extensibility (e.g., AbstractLanguageService, AbstractType)
- Interface-driven design for contracts and type safety
- Dependency injection using `tsyringe` for all services
- Singleton pattern for shared data services (e.g., SharingDataService)
- Use of experimental decorators for service registration
- Favor encapsulation, inheritance, and polymorphism where appropriate.

## 2. TypeScript Patterns
- Strict typing enforced via `tsconfig.json`
- Use of generics for reusable logic in services and helpers
- Type aliases for flexibility (e.g., AnyType, UndefinedType)
- Abstract classes define contracts, not implementations

## 3. Service Layer
- Abstract services for language, loading, logging, and storage (define contracts only, no business logic)
- Data sharing services (real-time and standard) with singleton scope
- All services injectable and extendable via dependency injection

## 4. Utilities & Helpers
- Common utilities: currency formatting, UUID generation, random numbers, async sleep
- Helper functions for object and UI manipulation

## 5. Constants & Enums
- Centralized constants for language codes, message types, HTTP methods, status codes, and storage keys

## 6. Code Quality & Tooling
- ESLint with TypeScript plugin for code linting and style enforcement
- All code must pass linting and TypeScript compilation before merging
- JSDoc required for all public classes and methods

## 7. Build & Testing
- Build process: `npm run build` (runs lint and TypeScript compiler)
- Prepare script ensures build consistency
- Testing placeholder present; extend as needed

## 8. Contribution Guidelines
- Extend abstract services by subclassing, not by modifying base classes
- Prefer composition over inheritance
- Follow naming conventions and documentation standards