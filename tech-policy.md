---
layout: default
title: "Tech - Policy"
nav_order: 7
---

# Texagon Tech Policy

## 1. Technology Stack

Texagon follows a structured technology stack to maintain consistency, security, and efficiency across projects.

### Backend

- **Python Framework**: FAST-API (with requirement.txt and PEP 8 Style Guidelines)
- **TypeScript Framework**: NestJS (TypeScript over vanilla JavaScript)
- **Package Manager**: Bun
- **API Documentation**: Swagger is mandatory for all backend APIs

### Frontend

- **Framework**: Next.js - (Or any other suggested React-based framework)
- **UI Libraries**: shadcn and the like are mandatory for UI components

## 2. Development and Deployment Process

Texagon follows a structured three-stage deployment process:

### Development Stages

1. **Local Development**
2. **Staging**
3. **Production**

- **Staging and Production Environment**: Supabase with a self-hosted Docker container setup is used in both staging and production to ensure uniformity.
- **CI/CD Pipelines**: All deployments are fully containerized and use CI/CD workflows.
- **Release-Based Deployments**: Deployments are created with release versions instead of direct pushes.

## 3. Code Review & Release Management

- **Pull Requests (PRs)**: Must be reviewed by a Team Lead before merging.
- **Staging Releases**: Created daily or as per PM's instructions.
- **Testing**:
  - Local debugging is required before merging to staging.
  - Staging releases are tested before production deployment.

## 4. Security & Best Practices

- **Secure Coding**: Security and all standard software development best practices are followed.
- **Environment Variables**:
  - Not stored in repositories.
  - Managed via GitHub Actions secrets.
  - Team collaboration on environment variables is handled through pinned threads on Slack inside relevant channel (internal channel) Thread name are the like of (e.g., Frontend Staging, Frontend Production, Backend Staging, Backend Production).

## 5. Repository Structure & Naming Conventions

- **Separate Repositories**: Backend and frontend repositories are maintained separately to enable cloning the API repo for customized frontend integrations.
- **Naming Convention**:
  - `{project_name}-frontend`
  - `{project_name}-backend`

By adhering to this policy, Texagon ensures a scalable, maintainable, and secure development environment for all projects.
