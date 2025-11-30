# UniversalAction

**UniversalAction** is a strict, modular framework for managing game actions in Roblox. It decouples logic from execution, providing a unified way to run code on the Server, Client, or both, with built-in validation and lifecycle management.

Inspired by modern web frameworks, UniversalAction uses a centralized registry and middleware pattern to keep your codebase clean.

## Why UniversalAction?

* **⚡ Type Strict:** Built with `--!strict` Luau for robust type checking.
* **📦 Modular:** Actions are isolated modules, making them easy to reuse and test.
* **🛡️ Scoped:** Automatically enforces execution scope (`Server`, `Client`, or `Any`).
* **🔗 Middleware:** Hook into the execution pipeline for logging, analytics, or permission checks.
* **📡 Network Bridge:** Simple API to trigger actions across the network without manually creating Remotes for every feature.
* **🧹 Lifecycle Managed:** Built-in `Cleanup` table for handling connections and loops within actions.

[Get Started](./installation.md)
