---
description: This section provides detailed documentation for the main REST API endpoints.
---

# API Reference

The FetchFox API uses JSON for request and response payloads. All requests must be authenticated with an API key.

* Base URL: `https://fetchfox.ai/api/v2`&#x20;
* Authentication: Bearer token via the `Authorization` header
* Response Format: `JSON`&#x20;

## Endpoints

All endpoints are relative to the base URL.

### Workflows

Get all workflows

* Method: `GET`
* Endpoint: `/workflows`
* Example:

```bash
curl "https://fetchfox.ai/api/v2/workflows" \
     -H "Authorization: Bearer YOUR_API_KEY"
```

Get a specific workflow

* Method: `GET`
* Endpoin&#x74;**:** `/workflow/{workflow_id}`&#x20;
* Example:

```bash
curl "https://fetchfox.ai/api/v2/workflows/12345" \
     -H "Authorization: Bearer YOUR_API_KEY"
```

Create a new workflow

* Method: `POST`&#x20;
* Endpoint: `/workflows`&#x20;
* Request Body: JSON representation of a workflow
* Response: Returns a `workflowId`
* Example:

```bash
curl "https://fetchfox.ai/api/v2/workflows" \
    -H "Content-Type: application/json" \
    -H "Authorization: Bearer YOUR_API_KEY" \
    -d '{
        "steps": [
            {
                "name": "const",
                "args": {
                    "items": [
                        {
                            "url": "https://pokemondb.net/pokedex/national"
                        }
                    ],
                    "maxPages": 1
                }
            },
            {
                "name": "extract",
                "args": {
                    "questions": {
                        "name": "What is the name of the Pokémon?",
                        "number": "What is the National Dex number of the Pokémon?",
                        "types": "What are the types of the Pokémon?",
                        "url": "What is the URL of the Pokémon'\''s detailed page?"
                    },
                    "mode": "auto",
                    "view": "html",
                    "maxPages": 1,
                    "limit": 10
                }
            }
        ]
    }'
```

### Running Workflows

Run a workflow

* Method: `POST`&#x20;
* Endpoint: `/workflows/{workflow_id}/run`
* Response: Returns a `jobId`&#x20;
* Example:

```bash
curl --request POST "https://fetchfox.ai/api/v2/workflows/12345/run" \
     -H "Authorization: Bearer YOUR_API_KEY"
```

### Jobs

Get job details

* Method: `GET`&#x20;
* Endpoint: `/jobs/{job_id}`&#x20;
* Response: A JSON containing job details including results, and job completion status.
* Example:

```bash
curl "https://fetchfox.ai/api/v2/jobs/12345" \
     -H "Authorization: Bearer YOUR_API_KEY"
```
