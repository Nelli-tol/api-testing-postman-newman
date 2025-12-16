# API Testing with Postman & Newman

This repository contains examples of API testing using Postman collections and Newman CLI execution.

## Scope
- REST API functional testing
- Positive and negative scenarios
- Request validation and response assertions
- Environment-based execution
- Command-line execution using Newman

## Tools
- Postman
- Newman
- REST API
- JSON

## Project Structure
- `collections/` — Postman collections and environments
- `docs/` — API test strategy and notes

## Notes
Public demo APIs are used for testing purposes.

---

## How to Run (Newman)

### Requirements
- Node.js (v18+)
- Newman

### Install Newman
```bash
npm install -g newman

newman run collections/reqres_api.postman_collection.json \
  -e collections/reqres_environment.postman_environment.json

npm install -g newman-reporter-htmlextra

newman run collections/reqres_api.postman_collection.json \
  -e collections/reqres_environment.postman_environment.json \
  -r htmlextra
