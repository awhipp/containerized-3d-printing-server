
# Containerized 3D Printing Server

This repository contains a Docker Compose configuration for deploying a 3D printing suite of services, specifically OctoPrint and OrcaSlicer. These services are fully backed up to volumes that are reflected in a backup folder within the repository.

## Overview

- **OctoPrint**: A powerful open-source 3D printer management tool.
- **OrcaSlicer**: A slicing software for preparing 3D models for printing.

## Description

This setup uses Docker Compose to manage the deployment of OctoPrint and OrcaSlicer. Both services are configured to use persistent volumes for data storage, ensuring that all data is backed up to the `backup` folder in the repository.

## Getting Started

### Prerequisites

- Docker
- Docker Compose

### Installation

1. Clone this repository:

    ```sh
    git clone https://github.com/yourusername/containerized-3d-printing-server.git
    cd containerized-3d-printing-server
    ```

2. Create the backup directories:

    ```sh
    mkdir -p backup/octoprint backup/orcaslicer
    ```

3. Start the services:

    ```sh
    docker-compose up -d
    ```

### Accessing the Services

- **OctoPrint**: Open your browser and go to `http://localhost:5000`
- **OrcaSlicer**: Open your browser and go to `http://localhost:3000` (Orca Slicer desktop gui) or `http://localhost:3001/web` (Orca Slicer desktop gui HTTPS).

### Backup

All data is stored in the `backup` folder within the repository. This ensures that your data is safe and can be easily backed up or restored.

## Contributing

Feel free to submit issues or pull requests if you have any improvements or suggestions.

## License

This project is licensed under the MIT License.
