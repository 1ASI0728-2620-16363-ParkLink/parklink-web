# Owner dashboard

Read-only web interface for owners to monitor ParkLink activity.

## Responsibilities

- Connects through the Gateway to retrieve owner-facing information.
- Does not replace the mobile publication and booking flows.

## Technology

React, TypeScript, Vite.

## C4 architecture

The diagram is a C4 **container view** focused on this repository and its relevant neighbors. It is generated from [Structurizr DSL](docs/architecture/workspace.dsl) using default styles, without custom colors. Arrows show the direction of an interaction; the full model also records message flows.

![C4 container view: Owner dashboard](docs/architecture/containers.svg)

To inspect or regenerate the diagram, open `docs/architecture/workspace.dsl` in Structurizr. With the Structurizr CLI and Graphviz installed:

```sh
structurizr.sh validate -workspace docs/architecture/workspace.dsl
mkdir -p /tmp/parklink-diagram
structurizr.sh export -workspace docs/architecture/workspace.dsl -format dot -output /tmp/parklink-diagram
dot -Tsvg /tmp/parklink-diagram/structurizr-Containers.dot -o docs/architecture/containers.svg
```

## Build in the integrated workspace

```sh
npm ci
npm run build -w @parklink/owner-dashboard
```

## Repository boundary

This repository is a snapshot of `apps/owner-dashboard` from [parklink-platform](https://github.com/1ASI0728-2620-16363-ParkLink/parklink-platform). Use the integrated workspace for the root npm configuration, shared dependencies, Docker build context, tests and local infrastructure. The repositories do not automatically synchronize.
