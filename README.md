## Getting Started

### Running from Docker

#### Prerequisites

- Docker
- Docker Compose

#### Starting the app

```sh
docker-compose up -d --build
```

#### Stopping the app

```sh
docker-compose down
```

#### Accessing the project

The frontend can be accessed at `http://localhost:3000`, and the backend can be accessed at `http://localhost:8000`.

---

### Running Natively

#### Prerequisites

- Python 3.10+
- Bun (for frontend)

#### Backend

1. **Clone the repository:**

   ```sh
   git clone https://github.com/yourusername/knowledge-table.git
   ```

2. **Navigate to the backend directory:**

   ```sh
   cd knowledge-table/backend/
   ```

3. **Create and activate a virtual environment:**

   ```sh
   python3 -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scriptsctivate`
   ```

4. **Install the dependencies:**

   For basic installation:

   ```sh
   pip install .
   ```

   For installation with development tools:

   ```sh
   pip install .[dev]
   ```

5. **Start the backend:**

   ```sh
   cd src/
   python -m uvicorn app.main:app
   ```

   The backend will be available at `http://localhost:8000`.

#### Frontend

1. **Navigate to the frontend directory:**

   ```sh
   cd ../frontend/
   ```

2. **Install Bun (if not already installed):**

   ```sh
   curl https://bun.sh/install | bash
   ```

3. **Install the dependencies:**

   ```sh
   bun install
   ```

4. **Start the frontend:**

   ```sh
   bun start
   ```

   The frontend will be available at `http://localhost:5173`.

---

### Environment Setup

1. Rename `.env.sample` to `.env`.
2. Add your OpenAI API key to the `.env` file.

> **Note:** This version of this project uses OpenAI as our initial provider, but the system is designed to be flexible and can be extended to support other AI providers. If you prefer a different provider, please create an issue, submit a PR, or check back soon for updates.

3. Configure the vector store in the `.env`. [Milvus](https://milvus.io) and [Qdrant](http://qdrant.tech) are the available as options.

---

## Development

To set up the project for development:

1. Clone the repository
2. Install the project with development dependencies:
   ```sh
   pip install .[dev]
   ```
3. Run tests:
   ```sh
   pytest
   ```
4. Run linters:
   ```sh
   flake8
   black .
   isort .
   ```

---
