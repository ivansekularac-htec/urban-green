# Urban Green Analytics Platform

The in-house data platform of Urban Green, a fictional indoor farming company
with 75 farms across seven German cities. It takes sensor telemetry, harvest logs and farm
metadata and turns them into dashboards for the people running the farms, a daily written
summary, and answers to questions asked in plain language.

The platform is built during the Fusion Internship, one service at a time, and every
service runs locally in Docker.

## Running the platform

```
docker compose up -d
```

This starts every service defined in `docker-compose.yaml`. The file starts out empty, and
each module adds its services to it.

## Repository layout

```
docker-compose.yaml   every service, grows from Module 1
pyproject.toml        one Python project for the whole platform
.github/              CI workflows, code owners and the contribution guide
docs/                 how to run each part, and notes on decisions
data/                 the seed data
api/                  Module 1: the FastAPI app, its tests, migrations and seed step
  bruno/              the API collections
etl/
  dags/               Module 2 onward: Airflow DAGs
  ingestion/          Module 2: the Spark streaming job
  transformations/    Module 3: the Spark transformation jobs
ai/
  mcp/                Module 5: the ClickHouse MCP server
  automations/        Module 5: the LangChain automations, including the daily report
services/             one folder per running service, with its configuration
```

The layout is fixed from the start and stays the same for the whole project. Each folder
fills up when its module arrives.

## Contributing

Read [.github/CONTRIBUTING.md](.github/CONTRIBUTING.md) before your first pull request.
