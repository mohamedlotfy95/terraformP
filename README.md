# Terraform Docker Setup

This project uses Terraform to deploy a Docker container running the Nginx web server. The configuration includes:

- **Terraform provider for Docker**: Configured to interact with Docker and manage Docker containers and images.
- **Docker Image**: Pulls the `nginx` image from Docker Hub.
- **Docker Container**: Creates and runs a container from the `nginx` image, exposing port `80` inside the container to port `8000` on the host.

## Prerequisites

Before running this Terraform configuration, ensure you have the following:

- [Terraform](https://www.terraform.io/downloads) installed.
- [Docker](https://www.docker.com/products/docker-desktop) installed and running on your machine.
- Git (optional) for version control.

## Providers

This project uses the following Terraform provider:

- **Docker**: The provider used to manage Docker images and containers.

### Required Provider Version:

```hcl
terraform {
  required_providers {
    docker = {
      source  = "kreuzwerker/docker"
      version = "~> 3.0.1"
    }
  }
}
