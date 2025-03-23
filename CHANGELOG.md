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