## [2025-03-23] [PR#20](https://github.com/OpenWorkspace-o1/ow-camel-mem0-memory/pull/20)

### Updated
- Updated package installation command in `README.md` from `openworkspace-o1-camel-mem0` to `ow-camel-mem0-memory`.
- Fixed a typo in the documentation link text from "Read me" to "Read more".

## [2025-03-23] [PR#18](https://github.com/OpenWorkspace-o1/ow-camel-mem0-memory/pull/18)

### Added
- Added documentation for configuring `llm` with `anthropic` provider and `graph_store` with `neo4j` in `README.md`.
- Added full configuration example including `llm` and `graph_store` settings.

## [2025-03-23] [PR#14](https://github.com/OpenWorkspace-o1/ow-camel-mem0-memory/pull/14)

### Added
- Added `MULTI-TENANT-STRATEGY.md` to document multi-tenant naming conventions.

### Updated
- Updated `README.md` with proper code block formatting for configuration examples.
- Updated `pyproject.toml` dependencies to use `>=` for `camel-ai` and `mem0ai` versions.

## [2025-03-23] [PR#12](https://github.com/OpenWorkspace-o1/ow-camel-mem0-memory/pull/12)

### Added
- Added detailed configuration examples for `pgvector` and `openai` embedder in `README.md`.
- Added `sqlalchemy` and `psycopg2-binary` dependencies in `pyproject.toml`.

### Updated
- Updated project name from `openworkspace-o1-camel-mem0` to `ow-camel-mem0-memory` in `pyproject.toml`.
- Bumped version to `0.0.3` in `pyproject.toml`.
- Updated `README.md` with links to external documentation for vector stores and embedders.

## [2025-03-22] [PR#8](https://github.com/OpenWorkspace-o1/ow-camel-mem0-memory/pull/8)

### Added
- Added `__init__.py` to expose `Mem0Storage` directly from the package.

### Updated
- Updated import example in `README.md` to use the new package-level import.
- Bumped version to `0.0.2` in `pyproject.toml`.

## [2025-03-22] [PR#2](https://github.com/OpenWorkspace-o1/ow-camel-mem0-memory/pull/2)

### Added
- Introduced the `Mem0Storage` class for managing memory storage using Mem0.
- Implemented methods for saving, loading, and clearing memory records.
- Added configuration support via `pyproject.toml` for the package.