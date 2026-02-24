
IDMC CI/CD Repository
Overview

This repository contains all Informatica Intelligent Data Management Cloud (IDMC) assets related to:

Cloud Data Integration (CDI)

Cloud Application Integration (CAI)

The repository is integrated with the DEV, QA, and PROD environments and supports automated CI/CD deployment across these environments.

Purpose

The purpose of this repository is to:

Maintain version control for all IDMC assets

Enable structured promotion of assets across environments

Support automated CI/CD deployments

Ensure consistency between DEV, QA, and PROD

Maintain auditability and traceability of changes

Environment Architecture

The deployment flow follows this structure:

Informatica Org (Source)
        ↓
       DEV
        ↓
       QA
        ↓
      PROD
Environment Details
Environment	Purpose
DEV	Development and initial testing
QA	System integration and validation testing
PROD	Production deployment
Deployment Process
1️⃣ Development

Assets are created/modified in the Informatica DEV organization

Assets include mappings, mapping tasks, workflows, connections, parameters, CAI processes, etc.

2️⃣ Export & Commit

IDMC assets are exported from the Informatica organization

Assets are committed and version-controlled in this Git repository

3️⃣ CI/CD Pipeline Execution

The CI/CD pipeline:

Pulls assets from the repository

Validates structure and dependencies

Deploys to target environments (QA / PROD)

4️⃣ Promotion

Promotion from QA to PROD occurs only after successful validation

Repository Structure (Recommended)
/CDI
    /Mappings
    /Mapping_Tasks
    /Workflows
    /Connections
    /Parameters

/CAI
    /Processes
    /Connections

/Environment_Config
    /DEV
    /QA
    /PROD

/Pipeline
    cicd-config.yml
Key Features

Version-controlled IDMC assets

Structured environment promotion

Automated deployment

Reduced manual intervention

Environment-specific configuration handling

Rollback capability via Git history
