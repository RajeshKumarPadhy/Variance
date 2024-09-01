# Variance

An Nx monorepo with sensible defaults for building full stack apps.

Learn more about this [workspace setup and its capabilities](https://nx.dev/getting-started/intro#learn-nx?utm_source=nx_project&amp;utm_medium=readme&amp;utm_campaign=nx_projects) or run `npx nx graph` to visually explore what was created.

Now, let's get you up to speed on the monorepo structure

## Nx tasks

To run tasks with Nx use:

```sh
npx nx <target> <project-name>
```

For example:

```sh
npx nx run web:dev: # to run the nextjs app in dev mode
```

These targets are either [inferred automatically](https://nx.dev/concepts/inferred-tasks?utm_source=nx_project&utm_medium=readme&utm_campaign=nx_projects) or defined in the `project.json` or `package.json` files.

### Nx Project tasks

```js
// Web

nx run web:build
nx run web:dev
nx run web:lint
nx run web:serve-static
nx run web:start
nx run web:test

// Native
nx run native:build
nx run native:export
nx run native:install
nx run native:lint
nx run native:pre-build
nx run native:run-android
nx run native:run-ios
nx run native:serve
nx run native:start
nx run native:submit
nx run native:test

// Server
nx run server:build
nx run server:lint
nx run server:preview
nx run server:serve
nx run server:serve-static
nx run server:test

// CMS
nx run cms:build
nx run cms:dev
nx run cms:start

// Control Center
nx run control-center:build
nx run control-center:lint
nx run control-center:preview
nx run control-center:serve
nx run control-center:serve-static
nx run control-center:test
nx run control-center:typecheck

```

## Monorepo Structure

The monorepo consists of the following apps:

| App            | Project         | Type                | Description                                           |
|----------------|-----------------|---------------------|-------------------------------------------------------|
| Web            | web             | Frontend            | A Next.js app that can be deployed via Vercel or Netlify |
| Native         | native          | Mobile              | An Expo app for Android and iOS                      |
| Server         | server          | Backend/API         | A NestJS app for the backend and API server          |
| CMS            | cms             | Content Management  | A KeystoneJS app that can serve as the CMS           |
| Control Center | control-center  | Admin Dashboard     | A React app to serve as the admin dashboard          |

<pre>

```md

/variance
├── apps                                      # Main user-facing applications
│   ├── web (Next.js)                         # Web application *
│   ├── native (Expo)                         # Mobile application using Expo *
│   ├── server (NestJS)                       # Backend API server *
│   ├── cms (KeystoneJS)                      # Content management system *
│   ├── control-center (React)                # Internal admin dashboard *
├── services                                  # Non-user-facing services
│   ├── gateway                               # API Gateway (e.g., Apollo Gateway, NGINX)
│   └── jobs                                  # Background jobs and workers
├── libs                                      # Shared libraries and modules
│   ├── ui                                    # Shared UI components
│   │   ├── web                               # Components for web
│   │   └── native                            # Components for native
│   ├── state                                 # State management (Mobx)
│   ├── api                                   # API clients and logic
│   ├── graphql                               # GraphQL utilities
│   ├── config                                # Configuration management
│   ├── types                                 # Shared TypeScript types
│   ├── hooks                                 # Shared hooks
│   ├── utils                                 # Utility functions
│   ├── auth                                  # Auth and authorization modules
│   ├── caching                               # Caching utilities
│   ├── db                                    # Database utilities and ORM
│   ├── i18n                                  # Internationalization
│   ├── analytics                             # Analytics integrations
│   ├── error-handling                        # Error handling and logging
│   ├── monitoring                            # Monitoring tools
│   ├── feature-flags                         # Feature flag management
│   ├── payment                               # Payment processing
│   ├── notifications                         # Notifications
│   ├── migrations                            # Data migrations
│   └── observability                         # Observability tools (e.g., logs, metrics)
├── tools                                     # Developer tools and scripts
│   ├── scripts                               # Custom scripts
│   ├── devops                                # DevOps utilities
│   ├── ci                                    # CI configurations
│   ├── security                              # Security checks
│   └── infrastructure                        # Infrastructure management
├── docs                                      # Documentation
│   ├── api                                   # API documentation
│   ├── developer                             # Developer guides
│   ├── user                                  # User manuals
│   ├── architecture                          # Architecture documentation
│   └── testing                               # Testing guides
├── tests                                     # Testing configurations
│   ├── e2e                                   # End-to-end tests
│   ├── unit                                  # Unit tests
│   └── integration                           # Integration tests
├── configs                                   # Environment configurations
│   ├── dev                                   # Development configs
│   ├── staging                               # Staging configs
│   └── prod                                  # Production configs
├── monitoring                                # Monitoring and observability
│   ├── prometheus                            # Prometheus setup
│   ├── grafana                               # Grafana dashboards
│   ├── tracing                               # Tracing tools
│   └── alerting                              # Alerting rules
├── .github                                   # GitHub-specific configurations
│   └── workflows                             # GitHub Actions workflows
├── .husky                                    # Git hooks
│   ├── pre-commit                            # Pre-commit hooks
│   └── pre-push                              # Pre-push hooks
├── .lintstagedrc                             # Lint-staged configuration
├── .eslintrc                                 # ESLint configuration
├── .prettierrc                               # Prettier configuration
├── nx.json                                   # Nx configuration
└── package.json                              # Root package configuration
```
</pre>
