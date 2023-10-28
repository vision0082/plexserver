# Plex Media Server Setup

## Requirements

Before setting up Plex Media Server, make sure you have the following prerequisites:

- Docker installed
- Docker Compose installed
- Internet connection (Initially only)

## Setup

To set up Plex Media Server, follow these steps:

1. Edit the `docker-compose.yml` file.
2. Update the `PLEX_CLAIM` environment variable by adding your Plex claim token after signing in to Plex first.
3. Adjust the volume mounts as needed. By default, Docker will create two directories in the same working directory where `docker-compose.yml` file exists on your host machine. Feel free to change the first entries of each of the following to any other directory of your choice:

    - `./config`: This directory stores Plex's configuration data and metadata.
    - `./media`: This directory is used to store your media files, such as movies and TV shows.

4. Run Docker Compose to start Plex Media Server:

   ```bash
   docker-compose up -d