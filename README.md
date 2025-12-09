# AscendOps-Internship-Data-Engineering-Portfolio

> High-fidelity documentation and artifacts from the InnerCord internship. Showcasing proficiency in data pipeline construction, backend development, CI/CD, and professional engineering standards using Python, Pandas, and modular architecture.

<p align="center">
  <a href="https://github.com/chirag127/AscendOps-Internship-Data-Engineering-Portfolio/actions/workflows/ci.yml">
    <img src="https://img.shields.io/github/actions/workflow/status/chirag127/AscendOps-Internship-Data-Engineering-Portfolio/ci.yml?branch=main&style=flat-square&label=CI%2FCD" alt="Build Status">
  </a>
  <a href="https://codecov.io/gh/chirag127/AscendOps-Internship-Data-Engineering-Portfolio">
    <img src="https://img.shields.io/codecov/c/github/chirag127/AscendOps-Internship-Data-Engineering-Portfolio?style=flat-square&label=Coverage" alt="Code Coverage">
  </a>
  <a href="https://github.com/chirag127/AscendOps-Internship-Data-Engineering-Portfolio">
    <img src="https://img.shields.io/github/languages/top/chirag127/AscendOps-Internship-Data-Engineering-Portfolio?style=flat-square&label=Python" alt="Primary Language">
  </a>
  <a href="https://github.com/astral-sh/ruff">
    <img src="https://img.shields.io/badge/Linter%2FFormatter-Ruff-blueviolet?style=flat-square" alt="Ruff Linter/Formatter">
  </a>
  <a href="./LICENSE">
    <img src="https://img.shields.io/github/license/chirag127/AscendOps-Internship-Data-Engineering-Portfolio?style=flat-square&label=License%20(CC%20BY-NC)" alt="License">
  </a>
  <a href="https://github.com/chirag127/AscendOps-Internship-Data-Engineering-Portfolio/stargazers">
    <img src="https://img.shields.io/github/stars/chirag127/AscendOps-Internship-Data-Engineering-Portfolio?style=flat-square" alt="GitHub Stars">
  </a>
</p>

***
<p align="center">
  <a href="https://github.com/chirag127/AscendOps-Internship-Data-Engineering-Portfolio"><img src="https://img.shields.io/badge/Star%20%E2%AD%90%20this%20Repo-211A40?style=for-the-badge&logo=github&logoColor=white" alt="Star this Repository"></a>
</p>
***

## 🚀 The AscendOps Data Engineering Portfolio
This repository serves as the definitive, high-fidelity portfolio artifact from the InnerCord Data Engineering Internship. It rigorously documents professional expertise in constructing robust, scalable data pipelines using Python (Pandas/Polars), applying advanced modular architecture principles, and implementing fully automated DevOps standards (CI/CD). It is a tangible showcase of production-ready data engineering mastery.

### Key Focus Areas
1.  **Modular Python Backend:** Implementation of Clean Architecture principles (Modular Monolith) for data processing services.
2.  **Data Ingestion & Transformation:** Demonstrations using Pandas for complex ETL/ELT flows and data validation.
3.  **CI/CD Pipeline Mastery:** Automated testing, linting (Ruff), and deployment workflows via GitHub Actions.
4.  **Professional Documentation:** Artifacts (Jupyter notebooks, technical designs) detailing architectural decisions and performance optimizations.

## ⚙️ Architecture: Modular Data Monolith
The codebase is structured around a Modular Monolith pattern, ensuring decoupled services for data sources, core processing, and reporting layers, facilitating maintainability and scalability.

mermaid
graph TD
    A[Data Source Adapters] --> B(Extraction Module);
    B --> C{Transformation Engine (Pandas)};
    C --> D[Load & Storage Layer];
    D --> E(Reporting & Visualization);
    subgraph Core Engine
        B & C
    end
    style Core Engine fill:#f9f,stroke:#333,stroke-width:2px


## 📋 Table of Contents
-   [🚀 The AscendOps Data Engineering Portfolio](#%f0%9f%9a%80-the-ascendops-data-engineering-portfolio)
-   [⚙️ Architecture: Modular Data Monolith](#%e2%9a%99%ef%b8%8f-architecture-modular-data-monolith)
-   [🧠 AI Agent Directives (System of Record)](#%f0%9f%a7%a0-ai-agent-directives-system-of-record)
-   [🛠️ Setup and Installation](#%e2%9a%94%ef%b8%8f-setup-and-installation)
-   [✅ Development & Testing Standards](#%e2%9c%85-development--testing-standards)
-   [📜 License](#%f0%9f%93%9c-license)

---

## 🧠 AI Agent Directives (System of Record)
<details>
<summary><strong>SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)</strong></summary>

### 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect operating with absolute precision.
**Context:** Current Date is **December 2025**. Building for the 2026 standard.
**Output Standard:** Deliver **EXECUTION-ONLY** results.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

### 2. CORE TECHNOLOGY STACK (Python Data Engineering)
The Apex standard for this repository relies on the following toolchain:

| Component | Tool/Standard | Purpose |
| :--- | :--- | :--- |
| **Language** | Python 3.10+ | Strict type hinting (mypy compliance required). |
| **Package Management** | `uv` | Used for ultra-fast dependency resolution and environment locking. |
| **Linter/Formatter** | `Ruff` | Mandatory configuration adherence for linting and automatic formatting. |
| **Testing Framework** | `Pytest` | All tests must be unit or integration-level, achieving >90% code coverage. |
| **Data Processing** | `Pandas` / `Polars` | Use vectorized operations; avoid iterative loops where DataFrame operations are possible. |
| **Architecture** | Modular Monolith | Separation into `ingestion`, `core_transform`, and `reporting` modules. |

### 3. ARCHITECTURAL PRINCIPLES (MANDATORY ADHERENCE)
1.  **Separation of Concerns (SoC):** Modules must not have circular dependencies. Input/Output (I/O) handling must be isolated in dedicated adapter layers.
2.  **DRY (Don't Repeat Yourself):** Abstract common utility functions (e.g., logging, validation schemas) into a shared `utils` module.
3.  **SOLID Principles:** All service layers must demonstrate clear adherence to the Single Responsibility Principle (SRP).

### 4. VERIFICATION AND EXECUTION COMMANDS
Agents must use the following commands for development and CI/CD verification:

bash
# 1. Environment Setup (uv mandatory)
uv venv
source .venv/bin/activate
uv sync

# 2. Linting and Formatting (Ruff mandatory)
ruff check .
ruff format .

# 3. Running Tests (Pytest mandatory)
pytest --cov=src --cov-report=xml

</details>

---

## 🛠️ Setup and Installation

This project requires Python 3.10 or higher. We use `uv` for modern dependency management.

### Prerequisites

1.  **Install `uv`:**
    bash
    curl -LsSf https://astral.sh/uv/install.sh | sh
    
2.  **Clone the Repository:**
    bash
    git clone https://github.com/chirag127/AscendOps-Internship-Data-Engineering-Portfolio.git
    cd AscendOps-Internship-Data-Engineering-Portfolio
    

### Installation

Use `uv` to create a virtual environment and synchronize dependencies:

bash
# Create and activate the virtual environment
uv venv
source .venv/bin/activate

# Install required dependencies
uv sync


### Execution Scripts

The primary entry points are defined in the `pyproject.toml` file.

| Script Name | Command | Description |
| :--- | :--- | :--- |
| `run:pipeline` | `python src/main.py --mode production` | Executes the full production data pipeline flow. |
| `test:unit` | `pytest tests/unit` | Runs all unit tests and generates coverage reports. |
| `lint:fix` | `ruff check --fix . && ruff format .` | Automatically fixes all linting and formatting issues. |
| `clean` | `rm -rf .venv .pytest_cache dist build` | Removes environment artifacts. |

## ✅ Development & Testing Standards

### 1. Testing Protocol
All new features require corresponding unit tests using `pytest`. Aim for **100% test coverage** for all core business logic and transformation modules. Integration tests should mock external services but validate adapter contracts.

bash
# Run all tests with coverage reporting
pytest --cov=src


### 2. Code Quality
The `Ruff` linter is enforced strictly through the CI/CD pipeline. Developers must run the linting commands locally before submitting a Pull Request.

### 3. Contributing
Please review the [CONTRIBUTING.md](./.github/CONTRIBUTING.md) document before submitting major changes. All features must be tracked via an Issue, and PRs must reference that Issue.

---

## 📜 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** License. See the [LICENSE](./LICENSE) file for details.