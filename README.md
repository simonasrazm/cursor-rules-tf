# Cursor Rules for Terraform Infrastructure

Cloud-agnostic Terraform best practices and workflow guidelines for Cursor IDE. These rules help AI assistants provide better guidance when working with infrastructure as code.

## What is this?

This repository contains [Cursor IDE rules](https://docs.cursor.com/context/custom-rules) that guide AI assistants on Terraform best practices. The rules are:

- **Cloud-agnostic** - Works with GCP, Azure, AWS, and other cloud providers
- **Pattern-focused** - Emphasizes universal infrastructure patterns, not cloud-specific implementations
- **Modular** - Pick only the rule files you need for your project

## Quick Start

1. Copy the `.cursor` folder to your project root:

   ```bash
   cp -r .cursor /path/to/your/project/
   ```

2. That's it! Cursor will automatically load these rules.

## Rule Files

| File | Description |
|------|-------------|
| `infrastructure.mdc` | General infrastructure rules (sequential operations, no background agents) |
| `terraform.mdc` | Core Terraform workflow patterns (targeted operations, state management) |
| `terraform-patterns.mdc` | Core patterns (provider config, dependencies, common issues) |
| `terraform-container.mdc` | Container service best practices (lifecycle management, deployment strategy) |
| `terraform-iam.mdc` | Identity and access management patterns |
| `terraform-secrets.mdc` | Secrets vault integration patterns |
| `terraform-api-gateway.mdc` | API Gateway configuration (for public-facing services) |
| `terraform-storage.mdc` | Cloud storage best practices |

## Usage

Most rules are set to `alwaysApply: false` with glob patterns matching `terraform/**/*.tf` files, meaning they activate when editing Terraform files. The `infrastructure.mdc` rule is set to `alwaysApply: true` for general infrastructure guidance.

To change this behavior, edit the `alwaysApply` setting in any rule file.

## License

MIT License - see [LICENSE](LICENSE) file for details.

## Contributing

Contributions welcome! If you have improvements or additional patterns, please open an issue or pull request.

## Credits

Created by [@simonasrazm](https://github.com/simonasrazm) and Contributors.
