# Day 6 — ConfigMaps and Secrets

## ConfigMap

A ConfigMap stores non-sensitive application settings.

Examples:

- Application environment
- Log level
- API URL
- Feature settings

## Secret

A Secret stores sensitive values.

Examples:

- Passwords
- Tokens
- Usernames
- Private keys

## Difference

ConfigMap = normal settings

Secret = sensitive settings

## How Pods Use Them

Pods can read ConfigMaps and Secrets as:

1. Environment variables
2. Mounted files

## Important Understanding

Environment variables are loaded when the container starts. If a ConfigMap
value changes, an existing container may need to be restarted to receive
the new value.

Base64 encoding is not encryption.

Real Secret values must not be committed to GitHub.