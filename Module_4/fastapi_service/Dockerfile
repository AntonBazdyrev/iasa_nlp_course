# 1. Use a more recent FastAPI image with Python 3.11
FROM tiangolo/uvicorn-gunicorn-fastapi:python3.11

# 2. Speed up pip and disable cache
ENV \
    PIP_DEFAULT_TIMEOUT=100 \
    PIP_DISABLE_PIP_VERSION_CHECK=1 \
    PIP_NO_CACHE_DIR=1 \
    POETRY_VERSION=1.7.1 \
    POETRY_HOME=/opt/poetry

# 3. Install Poetry
RUN curl -sSL https://install.python-poetry.org | python3 - --version ${POETRY_VERSION} && \
    ln -s ${POETRY_HOME}/bin/poetry /usr/local/bin/poetry && \
    poetry config virtualenvs.create false

# 4. Copy only dependencies to leverage Docker cache
WORKDIR /app
COPY pyproject.toml poetry.lock* /app/

# 5. Install dependencies (no dev, no root package)
RUN poetry install --no-root --no-dev

# 6. Copy the application code
COPY service /app/service