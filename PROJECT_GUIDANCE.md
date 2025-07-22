# Project: LLM-Helped Cheating Detection for Competitive Programming

## 1. Problem Statement
Competitive programming contests face challenges with participants using Large Language Models (LLMs) to solve problems, leading to unfair advantages and compromising contest integrity. The goal is to develop an application to detect such LLM-helped cheating.

## 2. Application Overview
A full-stack web application designed to receive code submissions, analyze them for patterns indicative of LLM generation, and present potential cheating incidents to contest organizers.

## 3. Technology Stack
*   **Frontend:** React (JavaScript/TypeScript) with Material Design principles for a clean and intuitive user interface.
*   **Backend:** Rust (using a framework like Axum or Actix-web) for its performance, memory safety, and concurrency, making it ideal for complex code analysis.
*   **Database:** SQLite for initial prototyping, with an easy upgrade path to PostgreSQL for production environments.

## 4. Core Features
*   **Code Submission Interface:** An API endpoint for submitting code files (e.g., `.cpp`, `.java`, `.py`).
*   **LLM Detection Engine:** The core backend module responsible for analyzing submissions and flagging potential LLM-generated code.
*   **Admin Dashboard:** A web interface for contest organizers to:
    *   View all submissions.
    *   Identify and review flagged submissions with a "suspicion score."
    *   Perform manual verification of suspicious code.
    *   (Future) Manage contest settings and user roles.

## 5. LLM Detection Strategy
Instead of solely relying on a general-purpose external LLM, the detection will employ a multi-faceted, heuristic-based approach primarily implemented in the Rust backend. This strategy addresses concerns regarding reliability, cost, latency, explainability, and data privacy.

Key detection methods will include:
*   **Heuristic-Based Analysis:**
    *   **Code Style Metrics:** Analyzing indentation, variable naming, comment density, and adherence to competitive programming idioms vs. generic LLM boilerplate.
    *   **Abstract Syntax Tree (AST) Analysis:** Identifying structural patterns common in LLM-generated code (e.g., verbose function names, unusual control flow).
    *   **Code Similarity/Plagiarism Detection:** Comparing submissions against known LLM outputs or other submissions.
    *   **Statistical Analysis:** Examining token frequencies, code complexity metrics (e.g., cyclomatic complexity), and other statistical properties.
*   **Complementary LLM Use (Optional/Future):** Consideration for fine-tuning a smaller, local LLM specifically for this domain, or using external LLMs as a secondary check for human reviewers, but not as the primary automated detection mechanism.

## 6. Implementation Strategy
1.  Scaffold the basic project structure for both the React frontend and the Rust backend.
2.  Implement the code submission API endpoint.
3.  Develop a basic placeholder for the LLM detection engine.
4.  Iteratively design and refine the core detection algorithms within the Rust backend.
5.  Build out the Admin Dashboard for reviewing submissions.

This document serves as a guiding principle for the development of the LLM-helped cheating detection application.

## 7. Current Status
**Last Updated:** 2025-07-23

*   **Project Scaffolding:**
    *   [x] Created `backend` and `frontend` directories.
    *   [x] Initialized a Rust project in `backend` using Cargo.
    *   [x] Initialized a React + TypeScript project in `frontend` using Vite.
    *   [x] Installed frontend dependencies via `npm install`.
*   **Backend Development:**
    *   [x] Added `axum`, `tokio`, and `serde` dependencies to `Cargo.toml`.
    *   [x] Implemented a basic "Hello, World!" web server in `backend/src/main.rs`.
*   **Next Step:**
    *   Run the backend development server using `cargo run` from the `backend` directory.
    *   Confirm the server is running by accessing it.
    *   **Note:** The user needs to start a new shell session for the `cargo` command to be available in the system's PATH.