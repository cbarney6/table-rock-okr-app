# Table Rock OKR App

## Project Overview
**Project Name**: table-rock-okr  
**Framework**: Next.js 15.5.2 with React 19.1.0 and TypeScript  
**Database**: Supabase (PostgreSQL)  
**Deployment**: Vercel  

This is the primary OKR (Objectives and Key Results) application for Table Rock management.

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

## Development Setup

### Prerequisites
- Node.js 18+ 
- npm or yarn
- Supabase account
- Vercel account

### Environment Variables
Create a `.env.local` file with the following variables:
```env
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
SUPABASE_SERVICE_ROLE_KEY=your_service_role_key
SUPABASE_PROJECT_REF=your_project_ref
SUPABASE_ACCESS_TOKEN=your_access_token
```

### Development Commands
```bash
# Install dependencies
npm install

# Development server with Turbopack
npm run dev

# Production build with Turbopack  
npm run build

# Start production server
npm start

# Linting
npm run lint
```

## Tech Stack
- **Frontend**: Next.js 15.5.2 with React 19.1.0
- **Styling**: Tailwind CSS 4.0
- **Language**: TypeScript 5.0
- **Database**: Supabase (PostgreSQL)
- **Deployment**: Vercel
- **Build Tool**: Turbopack (enabled for dev and build)

## File Structure
```
table-rock-okr-app/
├── src/app/                 # Next.js 13+ app directory
├── public/                  # Static assets
├── .env.local              # Environment variables (not committed)
├── package.json            # Dependencies and scripts
└── README.md               # This file
```

## Development Process
1. **Local Development**: `npm run dev` for hot reloading
2. **Code Quality**: Run `npm run lint` before commits
3. **Build Validation**: Always test `npm run build` before deployment
4. **Deployment**: Use the Go Time workflow for production releases

## Contributing
1. Create a feature branch from `main`
2. Make your changes
3. Run tests and linting
4. Follow the Go Time workflow for deployment
5. Create a pull request

---

For detailed development instructions and project-specific configurations, see the local documentation files.
