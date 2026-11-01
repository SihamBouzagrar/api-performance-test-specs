# API Performance Testing Specifications

**Centralized repository for OpenAPI specifications used in automated API performance testing.**

## Overview

This repository serves as a centralized storage space for API specifications in JSON and YAML formats.

It allows development teams to publish and maintain their API definitions, while DevOps teams can access these specifications to perform automated API performance testing.

The specifications stored in this repository are used as input files by the AI-Powered API Performance Testing solution, which analyzes API definitions and generates Apache JMeter test scenarios.

The objective is to simplify collaboration between development and DevOps teams and facilitate the integration of API performance testing into the development lifecycle.

## Objectives

- Centralize API specifications in a shared Git repository.
- Allow developers to publish and update API definitions.
- Provide DevOps teams with accessible and version-controlled API specifications.
- Support OpenAPI/Swagger specifications in JSON and YAML formats.
- Facilitate automated performance testing using AI-generated JMeter scenarios.

## Repository Structure

```text
api-performance-test-specs/
│
├── apis/
│   ├── petstore/
│   │   ├── openapi.json
│   │   └── README.md
│   │
│   ├── user-service/
│   │   └── openapi.yaml
│   │
│   └── payment-service/
│       └── openapi.yaml
│
├── README.md
└── .gitignore
```

Each API has its own directory containing its specification and, optionally, a short README describing the API.

## Supported Formats

| Format | Extensions |
|---|---|
| JSON | `.json` |
| YAML | `.yaml`, `.yml` |

Specifications should follow the OpenAPI specification format (Swagger/OpenAPI 2.0 or OpenAPI 3.x, depending on the consuming testing service's supported versions).

## How It Works

### 1. Development Team

Developers add or update their API specifications in the corresponding directory.

```text
apis/
└── my-api/
    └── openapi.yaml
```

They then commit and push their changes to GitHub.

### 2. DevOps Team

DevOps engineers retrieve the required API specification from this repository.

The specification is supplied to the AI-powered API performance testing workflow as an input.

### 3. Automated Performance Testing

The main testing solution processes the specification to:

1. Analyze API endpoints and operations.
2. Generate a JMeter test scenario using an LLM.
3. Execute the performance test.
4. Collect execution results and generate performance reports.

## Integration with the Testing Solution

This repository provides the API specification inputs for the main project:

**[AI-Powered API Performance Testing](https://github.com/SihamBouzagrar/ai-performance-testingV2)**

The main solution uses these specifications to automate API performance testing through its AI-powered generation workflow and Jenkins CI/CD integration.

## Contribution Guidelines

To add a new API specification:

1. Create a directory under `apis/` using the API or service name.
2. Add the OpenAPI specification in JSON or YAML format.
3. Use a descriptive filename such as `openapi.json` or `openapi.yaml`.
4. Validate the specification before submitting it.
5. Commit and push your changes.

To update an existing API, modify its specification in the corresponding directory and submit the changes through Git.

## Best Practices

- Use clear and consistent directory names.
- Keep specifications synchronized with the actual API implementation.
- Document authentication requirements and API server URLs.
- Avoid including passwords, API keys, tokens, or other sensitive credentials.
- Use Git commits to track specification changes.
- Validate specifications before making them available for testing.

## Author

**Siham Bouzagrar**

[GitHub](https://github.com/SihamBouzagrar)

---

*Centralized API specifications for collaborative and automated performance testing.*