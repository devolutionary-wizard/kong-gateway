# Kong Gateway DB-less Configuration Example

This repository contains an example configuration for setting up Kong Gateway in a DB-less mode. Kong Gateway can run without a database, using a declarative configuration file to define its entities such as Services, Routes, Consumers, Plugins, and more.

## Overview

In DB-less mode, Kong reads its configuration from a `yaml` or `json` file. This approach simplifies operations and reduces latency since there's no database to read from or write to. It's particularly useful for infrastructure as code (IaC) practices, as the configuration can be versioned and deployed alongside your services.

## Getting Started

To use this example, you'll need to have Kong Gateway installed. If you haven't installed Kong yet, please follow the [official installation guide](https://docs.konghq.com/gateway-oss/2.1.x/install/).

### Configuration

The `kong.yml` file in this repository is a sample configuration file for a Kong Gateway running in DB-less mode. It defines a service that proxies to `https://jsonplaceholder.typicode.com`, with routes for accessing posts, comments, and users. It also includes several plugins for authentication, CORS, IP restriction, and rate limiting.

### Running Kong with the DB-less Configuration

1. Clone this repository to your local machine.
2. Navigate to the repository directory.
3. Start docker compose up -d