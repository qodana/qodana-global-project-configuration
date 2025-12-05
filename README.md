# Qodana Global Project Configuration Example

This repository demonstrates a minimal, working setup for Qodana Global Project Configuration repository.

Use this repo as a reference for your organization’s Global Configurations repository.

## Repository structure

- `qodana-global-configurations.yaml` - the file describing global configurations structure
- `base/qodana.yaml` - default configuration used for all other configuration
- `backend/qodana.yaml` - example configuration for backend projects
- `frontend/qodana.yaml` - example configuration for frontend projects
- `.github/workflows/upload-global-configuration.yml` - CI workflow to update configuration on server on repository changes

## Configuration files

This repository contains two main parts of global configuration:

- `qodana-global-configurations.yaml` - the file describing global configurations structure and files relations
- `*/qodana.yaml` files - configurations for whole organization / specific projects. These files could reference each other to inherit common settings.

## CI: Uploading configurations

This repository includes a workflow that uploads the catalog and referenced `qodana.yaml` files to Qodana whenever you push to main or dev, or manually trigger it.

Requirements:
- Secret `QODANA_CONFIGURATIONS_TOKEN` must be configured in your repository/organization settings.

## Useful links

For more information, see our documentation: https://www.jetbrains.com/help/qodana/global-configuration.html

## Usage

Please note that this repository should be used as a reference only. Feel free to suggest improvements or changes to the configurations provided here.