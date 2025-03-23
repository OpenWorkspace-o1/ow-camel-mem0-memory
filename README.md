# CamelAI Agents Integrated With Mem0 As Memory Layer

A Python package that integrates Mem0's memory capabilities with CamelAI agents, providing a robust and persistent memory storage solution.

## Overview

This package implements a Mem0-based storage backend for CamelAI agents, allowing them to store, retrieve, and manage their conversation history and memories using Mem0's powerful text storage and search capabilities.

## Requirements

- Python 3.10 or higher (< 3.13)
- camel-ai==0.2.36
- mem0ai==0.1.74

## Installation

```bash
pip install openworkspace-o1-camel-mem0
```

## Usage

Here's a basic example of how to use the Mem0 storage with CamelAI:

```python
from ow-camel-mem0-memory import Mem0Storage

# Configure Mem0 storage, read more at: https://github.com/mem0ai/mem0/tree/04d7f2e48c8fc06b29f791f97052419c459f1c05/docs/components/vectordbs
config = {
    "vector_store": {
        "provider": "pgvector",
        "config": {
            "dbname": "postgres",
            "user": "test",
            "password": "123",
            "host": "127.0.0.1",
            "port": "5432",
            "collection_name": "mem0",
            "embedding_model_dims": 1536,
            "diskann": True,
            "hnsw": False
        }
    }
}

# Initialize storage
storage = Mem0Storage(
    config_dict=config_dict,
    agent_id="my-agent",
    user_id="user-123",  # Optional
    metadata={"custom": "metadata"},  # Optional
    limit=100  # Optional, default memory retrieval limit
)

# Storage operations
storage.save(records)  # Save memory records
records = storage.load()  # Load memory records
storage.clear()  # Clear all memories
```

## Features

- **Seamless Integration**: Works as a drop-in storage solution for CamelAI agents
- **Persistent Memory**: Stores conversation history and agent memories in Mem0's reliable storage
- **Flexible Configuration**: Supports custom metadata, user IDs, and retrieval limits
- **Error Handling**: Robust error handling and logging for all storage operations
- **Type Safety**: Full type hints support for better development experience

## API Reference

### Mem0Storage

The main storage class that implements `BaseKeyValueStorage` from CamelAI.

#### Constructor Parameters

- `config_dict` (Dict[str, Any]): Mem0 configuration dictionary
- `agent_id` (str): Default agent ID for memory association
- `user_id` (Optional[str]): Default user ID for memory association
- `metadata` (Optional[Dict[str, Any]]): Default metadata for all memories
- `limit` (int): Maximum number of memories to return (default: 100)

#### Methods

- `save(records: List[Dict[str, Any]]) -> None`: Save memory records
- `load() -> List[Dict[str, Any]]`: Load stored memory records
- `clear() -> None`: Remove all stored records

## License

Apache License 2.0 - See [LICENSE](LICENSE) for details.

## References

- [Mem0 Documentation](https://docs.mem0.ai)
- [CamelAI Documentation](https://github.com/camel-ai/camel)
