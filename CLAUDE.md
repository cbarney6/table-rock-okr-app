# Table Rock OKR App - Development Guide

## Project Overview
**Project Name**: table-rock-okr  
**Supabase Project ID**: dfcnbctitwqsotcyyvrf  
**Live URL**: https://table-rock-okr-1xh5ai887-chris-barneys-projects.vercel.app  
**Framework**: Next.js 15.5.2 with React 19.1.0 and TypeScript  

This is the primary OKR (Objectives and Key Results) application for Table Rock management, distinct from the original okr-app project (ngudauyrlsdesjqorfnv).

## Go Time Workflow 🚀

The standard 3-step deployment process:

```bash
# Step 1: Build and validate
npm run build

# Step 2: Commit changes
git add . && git commit -m "Your commit message"

# Step 3: Deploy via git push
git push
```

**Always run these commands in sequence** to ensure a clean deployment pipeline. The git push triggers automatic deployment via Vercel.

## Project-Specific Configuration

### Supabase Configuration
- **Project Reference**: `dfcnbctitwqsotcyyvrf`
- **URL**: `https://dfcnbctitwqsotcyyvrf.supabase.co`
- **Environment**: Production database for table-rock-okr-app

### Environment Variables (.env.local)
```env
NEXT_PUBLIC_SUPABASE_URL=https://dfcnbctitwqsotcyyvrf.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImRmY25iY3RpdHdxc290Y3l5dnJmIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NTY4NjA5MjIsImV4cCI6MjA3MjQzNjkyMn0.0pnuGT7Z2fwJyfkmfdQKkj0wAdugRk7qizD4bYvx8f4
SUPABASE_SERVICE_ROLE_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImRmY25iY3RpdHdxc290Y3l5dnJmIiwicm9sZSI6InNlcnZpY2Vfcm9sZSIsImlhdCI6MTc1Njg2MDkyMiwiZXhwIjoyMDcyNDM2OTIyfQ.YOSyOQRy8vNNgkjtvuFy6Nb4vImSnu6H5NolBCNBTkM
SUPABASE_PROJECT_REF=dfcnbctitwqsotcyyvrf
SUPABASE_ACCESS_TOKEN=sbp_ff9f3d2e34322327caefcc1641dc15392503f4cb
```

**Key Points**:
- `NEXT_PUBLIC_*` variables are exposed to the browser
- `SUPABASE_SERVICE_ROLE_KEY` provides admin access for server-side operations
- `SUPABASE_ACCESS_TOKEN` enables CLI operations and migrations

## MCP Server Setup

The following MCP servers are configured for this project:

### Memory Server
- **Purpose**: Stores workflow patterns, deployment steps, and project knowledge
- **Usage**: Persistent memory across Claude Code sessions
- **Key Data**: Go Time workflow, project configurations

### GitHub Server
- **Purpose**: Repository management, PR creation, issue tracking
- **Repository**: Connected to project source control
- **Features**: Automated deployments, code reviews

### Vercel Server  
- **Purpose**: Deployment management and monitoring
- **Project**: `table-rock-okr-app` in chris-barneys-projects
- **Commands**: `vercel deploy`, `vercel list`, `vercel logs`

### Supabase Server
- **Purpose**: Database management, migrations, monitoring  
- **Project ID**: `dfcnbctitwqsotcyyvrf`
- **Features**: Schema management, real-time logs, security advisors

## Vercel Configuration

### Project Settings
- **Project Name**: table-rock-okr-app
- **Team**: chris-barneys-projects
- **Framework Preset**: Next.js
- **Build Command**: `npm run build` (with Turbopack)
- **Output Directory**: `.next`

### Recent Deployments
- **Production**: https://table-rock-okr-1xh5ai887-chris-barneys-projects.vercel.app
- **Build Time**: ~30-40 seconds
- **Status**: Active and healthy

### Environment Variables (Vercel)
The following environment variables should be configured in Vercel dashboard:
- `NEXT_PUBLIC_SUPABASE_URL`
- `NEXT_PUBLIC_SUPABASE_ANON_KEY`
- `SUPABASE_SERVICE_ROLE_KEY`
- `SUPABASE_PROJECT_REF`

## Development Workflow

### Standard Commands
```bash
# Development server with Turbopack
npm run dev

# Production build with Turbopack  
npm run build

# Start production server
npm start

# Linting
npm run lint
```

### Development Process
1. **Local Development**: `npm run dev` for hot reloading
2. **Code Quality**: Run `npm run lint` before commits
3. **Build Validation**: Always test `npm run build` before deployment
4. **Deployment**: Use the Go Time workflow for production releases

### Git Workflow
- **Main Branch**: `main` (clean status)
- **Commit Strategy**: Standard commits with descriptive messages
- **Deployment**: Automatic on push to main via Vercel

## Architecture Notes

### Multi-Project Setup Context
This project is part of a larger development ecosystem:

- **table-rock-okr-app** (this project): Primary production OKR application
- **okr-app**: Original development/testing project (ngudauyrlsdesjqorfnv)
- **Shared Resources**: MCP servers, development workflows, deployment patterns

### Tech Stack
- **Frontend**: Next.js 15.5.2 with React 19.1.0
- **Styling**: Tailwind CSS 4.0
- **Language**: TypeScript 5.0
- **Database**: Supabase (PostgreSQL)
- **Deployment**: Vercel
- **Build Tool**: Turbopack (enabled for dev and build)

### File Structure
```
table-rock-okr-app/
├── src/app/                 # Next.js 13+ app directory
├── public/                  # Static assets
├── documentation/           # Project specs and requirements
├── .env.local              # Environment variables
├── package.json            # Dependencies and scripts
└── CLAUDE.md               # This file
```

## Quick Reference

### Emergency Commands
```bash
# Check deployment status
vercel ls

# View recent logs  
vercel logs

# Rollback deployment
vercel rollback [deployment-url]
```

### Database Operations
```bash
# Connect to Supabase project
npx supabase link --project-ref dfcnbctitwqsotcyyvrf

# Run migrations (if configured)
npx supabase db push

# View database logs
# Use MCP Supabase server through Claude Code
```

### Troubleshooting
1. **Build Failures**: Check `npm run lint` and TypeScript errors
2. **Deployment Issues**: Verify environment variables in Vercel
3. **Database Errors**: Check Supabase logs via MCP server
4. **Performance Issues**: Review Next.js build output and Vercel analytics

---

**Note**: This project uses Supabase project `dfcnbctitwqsotcyyvrf`, not the original `ngudauyrlsdesjqorfnv`. Always verify project context when performing database operations.