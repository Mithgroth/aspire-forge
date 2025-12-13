# Aspire Forge

Forge new .NET 10 projects with Aspire 13 orchestration, TUnit testing, and a clean project structure.

## What You Get

```
my-project/
├── MyProject.slnx
├── global.json
├── .editorconfig
├── aspire/
│   ├── AppHost/           # Aspire orchestration
│   └── ServiceDefaults/   # OpenTelemetry, health checks, resilience
├── src/
│   ├── Api/               # Minimal Web API
│   └── Domain/            # Domain logic (empty, ready for your code)
└── tests/
    └── Unit/              # TUnit test project with sample tests
```

## Prerequisites

- [.NET 10 SDK](https://dotnet.microsoft.com/download)
- [Aspire CLI](https://aspire.dev)
- `uuidgen` (pre-installed on Linux)

## Quick Start

Run directly from GitHub:

```bash
cd /path/to/your/projects
curl -fsSL https://raw.githubusercontent.com/mithgroth/aspire-forge/main/forge | bash -s -- MySuperDuperAwesomeProject
```

## What's Included

### Aspire 13
- AppHost with health check configuration
- ServiceDefaults with OpenTelemetry, resilience, and service discovery

### API Project
- Minimal API setup
- OpenAPI support
- Health endpoints (`/health`, `/alive`)
- References Domain and ServiceDefaults

### Domain Project
- Empty class library for your domain logic
- No dependencies, pure domain code

### TUnit Tests
- Modern .NET testing framework
- Sample test with Before/After hooks
- Assembly hooks for setup/teardown
- References Domain project

### EditorConfig
Opinionated C# formatting:
- 4 spaces, LF line endings
- Always use `var`
- File-scoped namespaces
- Allman brace style
- Always require braces (no single-line if/for/foreach)
- camelCase private fields
- No `this.` qualifier
- No `#region` blocks

## After Creation

```bash
cd my-super-duper-awesome-project
aspire run
```

The Aspire dashboard opens in your browser. Your API runs with full observability.

## License

MIT
