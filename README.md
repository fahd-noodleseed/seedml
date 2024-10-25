# SeedML

[![Project Status: Initial Development](https://img.shields.io/badge/Project%20Status-Initial%20Development-yellow.svg)]()
[![License](https://img.shields.io/badge/license-Dual%20GPL%2FCommercial-blue.svg)](LICENSE.md)

> 🚧 **Early Development**: SeedML is currently in initial development. We're sharing our vision and progress openly, but the implementation is not yet ready for use. Star the repo to follow our progress!

## Vision

SeedML is an LLM-native specification language for describing complete applications in a single, consistent format. It serves as an intermediate representation between natural language requirements and implemented applications.

### The Problem We're Solving

Current software development requires translating business requirements through multiple layers and technologies:
- Business requirements → Technical specifications
- Technical specifications → Multiple implementations
- Changes need updates across all layers
- Different teams speak different languages

### Our Solution

A single, consistent language that can describe entire applications and be generated by LLMs:

```yaml
# Example of our target syntax
app TaskManager {
  entity Task {
    title: string
    status: todo->doing->done
    assigned: User?
    priority: low/medium/high
  }

  screen TaskBoard {
    layout: kanban(status)
    card: [title, assigned.avatar, priority]
    actions: [assign, move, edit]
  }

  rules {
    assign: {
      when: assigned changed
      do: notify@assigned
    }
  }
}
```

This specification will generate a complete, working application.

## Current Status

- [x] Initial language specification
- [x] Basic syntax documentation
- [ ] Parser implementation
- [ ] Basic compiler
- [ ] Development tools
- [ ] Example applications

## Planned Features

- **Complete Application Specification**: Define everything from data models to UI in one place
- **LLM-Native Design**: Optimized for AI generation and modification
- **Technology Agnostic**: Compile to any modern tech stack
- **Production Ready**: Built-in best practices and security patterns
- **Full Stack**: Covers database, backend, frontend, and integrations

## Documentation

- [Language Specification](docs/spec.md)
- [Design Principles](docs/principles.md)
- [Examples](docs/examples/)

## Licensing

SeedML will be available under a dual license:

- [GNU General Public License v3.0](LICENSE-GPL.md) for open source use
- Commercial License for commercial use (coming soon)

The core language specification and parser will be open source, while the compiler and enterprise features will require a commercial license.

## Getting Involved

We're looking for collaborators interested in:
- Language design and specification
- Compiler development
- Developer tools and IDE integration
- Documentation and examples

### How to Contribute
1. Check our [Issues](https://github.com/noodleseed/seedml/issues) for current discussions
2. Share your thoughts through [Discussions](https://github.com/noodleseed/seedml/discussions)

## Contact

- Email: [info@noodleseed.com](mailto:info@noodleseed.com)
- Website: [https://noodleseed.com](https://noodleseed.com)

## Coming Soon

- Development roadmap
- Contributor guidelines
- Alpha release timeline

---

Built with ❤️ by Noodle Seed
