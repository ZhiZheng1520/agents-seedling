# Agents Seedling

Multi-agent AI system configuration and workspace repository.

## Overview

This repository contains the workspace configurations, memory archives, and operational data for a collaborative AI agent system powered by Claude and other AI models.

## Agent Structure

The repository contains 6 specialized agents, each with their own workspace:

### clawd
- **Role**: Main agent
- **Workspace**: `/Users/zhizheng/clawd`
- **Model**: Google Gemini 2.5 Flash (default)
- **Channel**: WhatsApp

### clawd-manager
- **Role**: Manager/Coordinator
- **Workspace**: `/Users/zhizheng/clawd-manager`
- **Model**: Claude Sonnet 4.5 (claude-sonnet-4-5-20250929)
- **Auth**: anthropic:claude2 token
- **Channel**: Discord (manager account)
- **Heartbeat**: Every 10 minutes

### clawd-dev1
- **Role**: Developer 1
- **Workspace**: `/Users/zhizheng/clawd-dev1`
- **Model**: Claude Opus 4.5
- **Channel**: Discord (dev1 account)
- **Heartbeat**: Every 5 minutes

### clawd-dev2
- **Role**: Developer 2
- **Workspace**: `/Users/zhizheng/clawd-dev2`
- **Model**: Claude Sonnet 4.5 (claude-sonnet-4-5-20250929)
- **Channel**: Discord (dev2 account)

### clawd-qa
- **Role**: Quality Assurance
- **Workspace**: `/Users/zhizheng/clawd-qa`
- **Model**: Claude Sonnet 4.5 (claude-sonnet-4-5-20250929)
- **Auth**: anthropic:claude2 token
- **Channel**: Discord (qa account)

### clawd-secretary
- **Role**: Secretary/Research Assistant
- **Workspace**: `/Users/zhizheng/clawd-secretary`
- **Model**: Claude Sonnet 4.5 (claude-sonnet-4-5-20250929)
- **Channel**: Discord (secretary account)

## Workspace Contents

Each agent workspace typically contains:

- **Configuration Files**: `AGENTS.md`, `IDENTITY.md`, `SOUL.md`, `TOOLS.md`, `USER.md`, `HEARTBEAT.md`
- **Memory Archives**: Daily logs and research notes in `memory/` directory
- **Skills**: Custom skill modules in `skills/` directory
- **Reports**: Generated analysis and reports in `reports/` directory (where applicable)

## System Architecture

This multi-agent system is powered by:

- **Clawdbot**: Multi-agent orchestration framework
- **Claude Models**: Anthropic's Claude 4.5 (Opus, Sonnet variants)
- **Google Gemini**: Gemini 2.5 Flash for general tasks
- **Communication Channels**: Discord, WhatsApp integration
- **Agent-to-Agent Communication**: Enabled for collaborative work

## Features

- Agent-to-agent communication and collaboration
- Session memory and context retention
- Heartbeat monitoring for active agents
- Multiple authentication profiles (OAuth, API tokens)
- Discord and WhatsApp channel bindings
- Custom skills and tools per agent
- Research tracking and failure analysis
- Financial market analysis capabilities (main agent)

## Configuration

Main configuration is managed in `~/.clawdbot/clawdbot.json` with individual agent auth profiles stored in their respective workspace directories.

## Usage

This repository serves as a backup and version control for agent workspaces, configurations, and accumulated knowledge. It enables:

- Tracking agent memory and learning over time
- Sharing configurations across systems
- Reviewing agent research and reports
- Maintaining skill modules and tools

## Authentication

Agents use various authentication methods:
- OAuth profiles for Anthropic, OpenAI, Google services
- Static API tokens for fallback authentication
- Per-agent auth profile selection for load distribution

---

*Generated and maintained by the Manager agent*
