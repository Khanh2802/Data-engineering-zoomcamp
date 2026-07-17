# Start with slim Python 3.13 image
#FROM python:3.13.14-slim

# Copy uv binary from official uv image (multi-stage build pattern)
#COPY --from=ghcr.io/astral-sh/uv:latest /uv /bin/

# Set working directory
#WORKDIR /app

# Add virtual environment to PATH so we can use installed packages
#ENV PATH="/app/.venv/bin:$PATH"

# Copy dependency files first (better layer caching)
#COPY "pyproject.toml" "uv.lock" ".python-version" ./
# Install dependencies from lock file (ensures reproducible builds)
#RUN uv sync --locked

# Copy application code
#COPY pipeline.py pipeline.py

# Set entry point
#ENTRYPOINT ["uv", "run", "python", "pipeline.py"]

#docker run -it --rm \
#  --name Adventureworks2025_pg
#  -e POSTGRES_USER="root" \
#  -e POSTGRES_PASSWORD="root" \
#  -e POSTGRES_DB="Adventureworks2025" \
#  -v Adventureworks2025_postgres_data:/var/lib/postgresql \
#  -p 5432:5432 \
#  postgres:18

  docker run -d \
  --name adventureworks2025-pg \
  -e POSTGRES_USER=root \
  -e POSTGRES_PASSWORD=root \
  -e POSTGRES_DB=Adventureworks2025 \
  -v Adventureworks2025_postgres_data:/var/lib/postgresql \
  -p 5432:5432 \
  postgres:18