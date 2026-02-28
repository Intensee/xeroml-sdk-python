# xeroml-sdk

Python SDK for [XeroML](https://xeroml.com) — intent parsing and drift detection for AI apps.

## Installation

```bash
pip install xeroml-sdk
```

## Quickstart

```python
from xeroml import XeroML

client = XeroML(api_key="xml_...")
graph = client.parse("Help me plan a trip to Tokyo")

print(graph.root_goal)
print(graph.sub_goals)
```

### Async

```python
from xeroml import AsyncXeroML

client = AsyncXeroML(api_key="xml_...")
graph = await client.parse("Help me plan a trip to Tokyo")
```

### Sessions (multi-turn)

```python
session = client.create_session()
graph = session.parse("Refactor my auth module")
session.update("Here's the current code: ...")
drift = session.drift()
session.end()
```

## Links

- [Documentation](https://docs.xeroml.com)
- [Dashboard](https://app.xeroml.com)
- [GitHub](https://github.com/Intensee/xeroml-sdk-python)
