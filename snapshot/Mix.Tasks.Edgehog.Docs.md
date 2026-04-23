# `mix edgehog.docs`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.12.0/backend/lib/mix/tasks/edgehog/docs.ex#L21)

A Mix task for generating the full Edgehog documentation suite.

This task orchestrates the generation of three distinct documentation outputs:

- **Interfaces docs** – Markdown documentation generated from Astarte interface definitions
  using the `astarte-docs` CLI tool.
- **Tenant GraphQL API docs** – HTML documentation generated from the Absinthe GraphQL
  schema using `spectaql`.
- **Admin REST API docs** – OpenAPI spec and a SwaggerUI-based HTML viewer, generated
  by cloning the SwaggerUI repository and running `openapi.spec.yaml`.

## Usage

    mix edgehog.docs [options]

## Options

  * `--interfaces` / `--no-interfaces` – Include or skip interface documentation (default: `true`)
  * `--admin-api` / `--no-admin-api` – Include or skip admin REST API docs (default: `true`)
  * `--tenant-api` / `--no-tenant-api` – Include or skip tenant GraphQL API docs (default: `true`)
  * `--output` – Output directory for generated documentation
  * `--interfaces-path` – Path to the directory containing Astarte interface definitions

## Prerequisites

The task checks that all required external programs are available in `$PATH` before running:

  * `astarte-docs` – required for interface documentation
  * `npx` – required for tenant API documentation
  * `git` – required for admin API documentation

