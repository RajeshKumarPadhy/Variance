# Variance

<a alt="Nx logo" href="https://nx.dev" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/nrwl/nx/master/images/nx-logo.png" width="45"></a>

✨ Your new, shiny [Nx workspace](https://nx.dev) is almost ready ✨.

[Learn more about this workspace setup and its capabilities](https://nx.dev/getting-started/intro#learn-nx?utm_source=nx_project&amp;utm_medium=readme&amp;utm_campaign=nx_projects) or run `npx nx graph` to visually explore what was created. Now, let's get you up to speed!

## Finish your CI setup

[Click here to finish setting up your workspace!](https://cloud.nx.app/connect/FStUKiVaQI)

## Run tasks

To run tasks with Nx use:

```sh
npx nx <target> <project-name>
```

For example:

```sh
npx nx build myproject
```

These targets are either [inferred automatically](https://nx.dev/concepts/inferred-tasks?utm_source=nx_project&utm_medium=readme&utm_campaign=nx_projects) or defined in the `project.json` or `package.json` files.

[More about running tasks in the docs &raquo;](https://nx.dev/features/run-tasks?utm_source=nx_project&utm_medium=readme&utm_campaign=nx_projects)

## Add new projects

While you could add new projects to your workspace manually, you might want to leverage [Nx plugins](https://nx.dev/concepts/nx-plugins?utm_source=nx_project&utm_medium=readme&utm_campaign=nx_projects) and their [code generation](https://nx.dev/features/generate-code?utm_source=nx_project&utm_medium=readme&utm_campaign=nx_projects) feature.

To install a new plugin you can use the `nx add` command. Here's an example of adding the React plugin:

```sh
npx nx add @nx/react
```

Use the plugin's generator to create new projects. For example, to create a new React app or library:

```sh
# Genenerate an app
npx nx g @nx/react:app demo

# Generate a library
npx nx g @nx/react:lib some-lib
```

You can use `npx nx list` to get a list of installed plugins. Then, run `npx nx list <plugin-name>` to learn about more specific capabilities of a particular plugin. Alternatively, [install Nx Console](https://nx.dev/getting-started/editor-setup?utm_source=nx_project&utm_medium=readme&utm_campaign=nx_projects) to browse plugins and generators in your IDE.

[Learn more about Nx plugins &raquo;](https://nx.dev/concepts/nx-plugins?utm_source=nx_project&utm_medium=readme&utm_campaign=nx_projects) | [Browse the plugin registry &raquo;](https://nx.dev/plugin-registry?utm_source=nx_project&utm_medium=readme&utm_campaign=nx_projects)

[Learn more about Nx on CI](https://nx.dev/ci/intro/ci-with-nx#ready-get-started-with-your-provider?utm_source=nx_project&utm_medium=readme&utm_campaign=nx_projects)

## Install Nx Console

Nx Console is an editor extension that enriches your developer experience. It lets you run tasks, generate code, and improves code autocompletion in your IDE. It is available for VSCode and IntelliJ.

[Install Nx Console &raquo;](https://nx.dev/getting-started/editor-setup?utm_source=nx_project&utm_medium=readme&utm_campaign=nx_projects)

## Useful links

Learn more:

- [Learn more about this workspace setup](https://nx.dev/getting-started/intro#learn-nx?utm_source=nx_project&amp;utm_medium=readme&amp;utm_campaign=nx_projects)
- [Learn about Nx on CI](https://nx.dev/ci/intro/ci-with-nx?utm_source=nx_project&utm_medium=readme&utm_campaign=nx_projects)
- [Releasing Packages with Nx release](https://nx.dev/features/manage-releases?utm_source=nx_project&utm_medium=readme&utm_campaign=nx_projects)
- [What are Nx plugins?](https://nx.dev/concepts/nx-plugins?utm_source=nx_project&utm_medium=readme&utm_campaign=nx_projects)

And join the Nx community:

- [Discord](https://go.nx.dev/community)
- [Follow us on X](https://twitter.com/nxdevtools) or [LinkedIn](https://www.linkedin.com/company/nrwl)
- [Our YouTube channel](https://www.youtube.com/@nxdevtools)
- [Our blog](https://nx.dev/blog?utm_source=nx_project&utm_medium=readme&utm_campaign=nx_projects)

<pre>

```txt

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
├── infra                                     # Infrastructure as Code (IaC)
│   ├── terraform                             # Terraform scripts
│   ├── k8s                                   # Kubernetes configurations
│   ├── docker                                # Docker setups
│   └── cloud                                 # Cloud provider configurations
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
├── .env.example                              # Environment variables template
├── nx.json                                   # Nx configuration
└── package.json                              # Root package configuration
```
</pre>
