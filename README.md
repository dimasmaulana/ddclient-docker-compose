# Docker Compose Configuration for ddclient

This configuration file sets up a Docker container for ddclient using the `lscr.io/linuxserver/ddclient:latest` image.

## Services

### ddclient

* **Image:** `lscr.io/linuxserver/ddclient:latest`
* **Environment Variables:**
    * `PUID`: User ID to run ddclient as.
    * `PGID`: Group ID to run ddclient as.
    * `TZ`: Timezone for ddclient.
* **Volumes:**
    * `./config:/config`: Mounts the `./config` directory from the host machine into the `/config` directory within the container.
* **Restart Policy:** `always`: Ensures the container restarts automatically if it stops.

## Usage

1. **Replace Placeholders:**
    * Replace `$PUID`, `$PGID`, and `$TZ` with your actual values.
2. **Create config Directory:**
    * Create a directory named `config` in the same location as this `docker-compose.yml` file.
3. **Configure ddclient:**
    * Place your ddclient configuration file (`ddclient.conf`) inside the `config` directory.
4. **Start the Container:**
    * Run `docker-compose up -d` to start the ddclient container in detached mode.

**Note:** This configuration assumes you have Docker and Docker Compose installed and configured on your system.

