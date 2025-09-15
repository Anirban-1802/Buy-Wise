# BuyWise - AI-Powered Product Comparison Platform

## Overview

BuyWise is a mobile-first product comparison platform designed to empower Gen Z and budget-conscious buyers to make confident purchase decisions. The application provides AI-powered insights, real user proof, and instant price comparisons across multiple e-commerce platforms including Amazon, Flipkart, and Meesho. The platform features smart search capabilities (text, link, and image-based), personalized recommendations, and comprehensive product analysis with user-centric reviews categorized by personas like "College Student" and "First-Jobber".

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript using Vite as the build tool
- **Routing**: Wouter for lightweight client-side routing
- **UI Framework**: Shadcn/ui components built on Radix UI primitives with Tailwind CSS
- **State Management**: TanStack Query (React Query) for server state management
- **Design System**: Mobile-first responsive design with custom CSS variables and Inter font family
- **Component Structure**: Modular components with strict TypeScript typing and accessibility features

### Backend Architecture
- **Runtime**: Node.js with Express.js REST API
- **Language**: TypeScript with ES modules
- **API Design**: RESTful endpoints for products, search, wishlist, reviews, and price history
- **Middleware**: Custom logging, error handling, and request/response transformation
- **Development Setup**: Hot module replacement with Vite integration for development

### Data Storage Solutions
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Database Provider**: Neon Database (serverless PostgreSQL) - **ACTIVE AND CONNECTED**
- **Schema Management**: Drizzle Kit for migrations and schema management
- **Data Models**: Structured schemas for products, searches, wishlist, reviews, and price history with JSON fields for flexible data storage
- **Storage Implementation**: DatabaseStorage class replacing MemStorage for persistent data operations
- **Database Status**: Successfully deployed and populated with sample data (August 13, 2025)

### Authentication and Authorization
- **Authentication System**: Custom session-based authentication with bcrypt password hashing - **ACTIVE AND DEPLOYED**
- **Session Management**: PostgreSQL-based session storage using connect-pg-simple
- **User System**: Complete signup/login flow with custom forms replacing Replit OAuth redirect screens
- **API Endpoints**: /api/auth/signup, /api/auth/login, /api/auth/logout, /api/auth/user
- **Security**: Password hashing, session management, and request validation middleware

### External Service Integrations
- **Price Data Sources**: Category-appropriate platform assignments (Electronics: Amazon/Flipkart/Croma, Fashion: Myntra/Amazon/Ajio, Beauty: Nykaa/Amazon/Flipkart, etc.) - **IMPLEMENTED AND DEPLOYED**
- **Platform Coverage**: 23 products across 10+ categories with realistic platform price comparisons
- **AI Services**: Placeholder for AI-powered product verdict generation
- **Image Processing**: Foundation for image-based product search functionality
- **Real-time Updates**: Infrastructure for price monitoring and alerts

### Key Architectural Decisions

**Database Design**: Chose PostgreSQL with Drizzle ORM for type safety and complex querying capabilities needed for product comparisons and filtering. JSON fields enable flexible storage of platform-specific data and product attributes.

**API Architecture**: RESTful design with clear separation of concerns, enabling easy scaling and maintenance. Express.js provides mature ecosystem support with TypeScript for type safety.

**Frontend State Management**: TanStack Query handles server state with caching and synchronization, reducing complexity compared to global state solutions while providing excellent developer experience.

**Component Architecture**: Shadcn/ui provides pre-built accessible components while maintaining customization flexibility. Tailwind CSS enables rapid styling with consistent design tokens.

**Mobile-First Design**: Architecture prioritizes mobile experience with responsive breakpoints and touch-friendly interfaces, aligning with target Gen Z demographic preferences.