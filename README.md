# AnarchyWorld

The public, append-friendly world state for AnarchyWorld.

This repository is **data only**. It must never contain executable application code, scripts, package manifests, CI workflows, or secrets. The private `anarchy-engine` validates and renders this data.

## Core idea

Every route is represented by JSON under `world/`. Users edit the world through the engine; the engine validates each operation and commits the resulting JSON here.

## Safety boundary

Allowed: JSON world documents and inert assets/metadata.

Forbidden: JavaScript/TypeScript, HTML with executable content, shell scripts, workflows, packages, secrets, server configuration, or any instruction that the engine could execute.

## Initial route

`/` -> `world/index.json`

The format is versioned by `schema/world.schema.json`.
