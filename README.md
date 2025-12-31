# API Testing with Postman & Newman

![Newman API Tests](https://github.com/Nelli-tol/api-testing-postman-newman/actions/workflows/newman.yml/badge.svg)

This repository demonstrates REST API testing using **Postman collections**, **environment variables**, and **Newman** for CLI execution with **HTML reporting** and **GitHub Actions CI**.

> Demo API: ReqRes (public REST API for testing)

---

## What’s Included

- Postman **collection** with functional + negative tests (assertions in Tests tab)
- Postman **environment** with `base_url`
- Newman CLI runs locally and in **GitHub Actions**
- HTML report generated via `newman-reporter-htmlextra` (uploaded as CI artifact)
- Simple API test strategy document

---

## Project Structure

- `collections/` - Postman collection + environment  
  - `reqres_api.postman_collection.json`  
  - `reqres_environment.postman_environment.json`
- `docs/` - test strategy / notes
  - `api_test_strategy.md`
- `.github/workflows/newman.yml` - CI pipeline running Newman
- `package.json` - Newman + reporter dependencies and scripts

---

## Requirements

- Node.js 18+ (or 20+)
- npm

---

## Setup

```bash
npm install