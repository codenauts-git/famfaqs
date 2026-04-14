# Did You Know? - Barnachea Edition

A clean, minimal display of Barnachea family facts and trivia.

## Overview

This project serves a rotating set of curated family facts from a simple JSON file.  
Facts are displayed one at a time with smooth transitions and no repetition until all have been shown.

## Tech Stack

- nginx (alpine) via Docker
- Static HTML, CSS, and JavaScript
- Caddy (reverse proxy + HTTPS)

## Running Locally

Run:
docker compose up -d

Then open:
http://localhost:8089

## Editing Facts

All facts are stored in:
facts.json

Each fact follows this structure:

{
  "id": 1,
  "text": "Example fact",
  "type": "category",
  "tags": ["tag1", "tag2"],
  "active": true,
  "priority": 2
}

### Guidelines

- Keep facts specific and meaningful
- Avoid vague wording ("some", "many", etc.)
- Ensure all `id` values are unique
- Do not reuse IDs
- Set `"active": false` to disable a fact without deleting it

## Deployment

This project is served behind Caddy with automatic HTTPS.

Example domains:
- https://barnachea.fyi
- https://dyk.nautsfw.com

## Notes

This is a curated project. Facts are intentionally reviewed before being added to maintain quality and consistency.