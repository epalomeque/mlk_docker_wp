## WordPress + MySQL + phpMyAdmin (Docker)

This project runs a WordPress site, a MySQL database, and phpMyAdmin using Docker Compose.

### 1. Install Docker & Docker Compose

Docker Desktop includes Docker Compose, so you only need to install Docker Desktop:

- **Windows**
  - Download and install Docker Desktop from the official site (`https://www.docker.com/products/docker-desktop`).
  - During installation, ensure **"Use WSL 2 based engine"** is enabled (recommended).
  - After installation, open a new terminal (PowerShell) and verify:
    ```bash
    docker --version
    docker compose version
    ```

- **macOS**
  - Download Docker Desktop for Mac from the same page.
  - Install and start Docker Desktop, then verify:
    ```bash
    docker --version
    docker compose version
    ```

- **Linux**
  - Install Docker Engine following the official docs (`https://docs.docker.com/engine/install/`).
  - Then install Docker Compose plugin (`https://docs.docker.com/compose/install/linux/`).
  - Verify:
    ```bash
    docker --version
    docker compose version
    ```

Once these commands work, you are ready to use this project.

### 2. Configure environment variables

1. Copy the example env file:
   ```bash
   cp env.example .env
   ```
   On Windows PowerShell:
   ```powershell
   Copy-Item env.example .env
   ```
2. Open `.env` and adjust:
   - `MYSQL_ROOT_PASSWORD`, `MYSQL_PASSWORD`
   - Optionally `MYSQL_DATABASE`, `MYSQL_USER`
   - Leave host/port values as-is unless you know you need to change them.

### 3. Start the stack

From the project folder:

```bash
docker compose up -d
```

Then open:
- **WordPress**: `http://localhost:8070` (or the port you configured)
- **phpMyAdmin**: `http://localhost:8071` (or the port you configured)

