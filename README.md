# Simple Bibliography Parser

*from frontmatter to bibliographic reference*

This tool will parse a directory of markdown files and read the YAML frontmatter properties to create standardized bibliographic data from it.


## Documentation

01. [Introduction and Goals](docs/01_introduction_and_goals.md)
02. [Architecture Constraints](docs/02_architecture_constraints.md) 
03. [System Scope and Context](docs/03_system_scope_and_context.md)
04. [Solution Strategy](docs/04_solution_strategy.md)
05. [Building Block View](docs/05_building_block_view.md)
06. [Runtime View](docs/06_runtime_view.md)
07. [Deployment View](docs/07_deployment_view.md)
08. [Crosscutting Concepts](docs/08_crosscutting_concepts.md)
09. [Architecture Decisions](docs/09_architecture_decisions.md)
10. [Quality Requirements](docs/10_quality_requirements.md)
11. [Risks & Technical Debt](docs/11_risks_and_technical_debt.md)
12. [Glossary](docs/12_glossary.md)


## Project Structure

```
├── docs                        # arc42 based documenation
│   └── assets/                 # image and diagram files used in docs
├── src/
│   ├── python/
│   │   ├── functions/          # Custom analysis functions
│   │   └── utils/              # Database connections, helpers
│   └── sql/
│       ├── ddl_statements/     # Data definition language
│       └── transactional_sql/  # Queries and analysis SQL
├── notebooks/                  # Jupyter notebooks
├── pyproject.toml              # Poetry configuration
├── LICENSE
├── README.md                   # this document                     
└── .env.template               # Environment variables template
```

## Setup

1. **Clone and install dependencies**:
   ```bash
   git clone <repository-url>
   cd simple_bibliography_parser
   poetry install
   ```

2. **Configure environment**:
   ```bash
   cp .env.template .env
   # Edit .env with your database credentials
   ```

3. Make poetry kernel available in Jupyter for usage within VSCode:
   ```bash
   poetry run ipython kernel install --user --name=simple_bibliography_parser
   ```

## License

MIT License - see [LICENSE](LICENSE) for details.
