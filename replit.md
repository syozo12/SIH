# Heritage Gallery - Indian Art & Culture Platform

## Overview

This is a comprehensive digital platform showcasing India's rich cultural heritage through an interactive gallery of artifacts. The application serves as a virtual museum featuring paintings, sculptures, textiles, and monuments from various periods and regions of Indian history. Users can explore curated collections, filter artifacts by category, region, and historical period, and learn about the cultural significance of each piece through detailed information and timelines.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
The frontend is built using React with TypeScript, leveraging a modern component-based architecture:
- **UI Framework**: React with TypeScript for type safety and component reusability
- **Styling**: Tailwind CSS with a custom theme focused on warm, heritage-appropriate colors (browns, golds, oranges)
- **Component Library**: Radix UI components wrapped with custom styling via shadcn/ui
- **State Management**: React hooks for local state, TanStack Query for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Build Tool**: Vite for fast development and optimized production builds

### Backend Architecture
The backend follows a REST API pattern with Express.js:
- **Framework**: Express.js with TypeScript for the server runtime
- **API Design**: RESTful endpoints for artifact management and retrieval
- **Data Layer**: In-memory storage implementation with interface abstraction for future database integration
- **Middleware**: Custom logging, JSON parsing, and error handling middleware
- **Development**: Hot reloading with Vite integration for full-stack development

### Data Storage Solutions
Currently implements an in-memory storage pattern with plans for database migration:
- **Storage Interface**: Abstract `IStorage` interface allowing for multiple storage implementations
- **Current Implementation**: `MemStorage` class with pre-seeded artifact data
- **Database Ready**: Drizzle ORM configuration prepared for PostgreSQL integration
- **Schema Design**: Well-defined artifact and user schemas with comprehensive metadata fields

### Component Organization
The frontend follows a clear separation of concerns:
- **Pages**: Top-level route components (Home, NotFound)
- **Components**: Reusable UI components organized by functionality
- **UI Components**: Low-level design system components from shadcn/ui
- **Shared Types**: Common TypeScript interfaces and schemas shared between client and server

### Styling and Theming
Custom design system optimized for cultural heritage presentation:
- **Color Palette**: Warm heritage colors with dark theme support
- **Typography**: Mix of serif fonts for headings (Playfair Display) and sans-serif for body text
- **Layout**: Responsive grid system with mobile-first approach
- **Accessibility**: Focus on readable contrast ratios and semantic HTML structure

## External Dependencies

### Database Infrastructure
- **Drizzle ORM**: Modern TypeScript ORM with excellent type safety
- **PostgreSQL**: Configured as the target database (via Neon serverless)
- **Database Tools**: Drizzle Kit for migrations and schema management

### UI and Styling
- **Radix UI**: Comprehensive set of accessible, unstyled UI primitives
- **Tailwind CSS**: Utility-first CSS framework for rapid UI development
- **Lucide Icons**: Consistent icon library for UI elements
- **Embla Carousel**: Touch-friendly carousel component for image galleries

### Development and Build Tools
- **Vite**: Fast build tool with excellent TypeScript support and HMR
- **TypeScript**: Static typing for both frontend and backend code
- **ESBuild**: Fast JavaScript bundler for production builds
- **Replit Integration**: Custom plugins for development environment optimization

### Data Management
- **TanStack Query**: Powerful data fetching and caching library for API calls
- **React Hook Form**: Performant form library with validation support
- **Zod**: Runtime type validation for API schemas and form validation
- **Wouter**: Lightweight routing library for single-page application navigation

### Utilities and Helpers
- **class-variance-authority**: Type-safe utility for conditional CSS classes
- **clsx**: Utility for constructing className strings conditionally
- **date-fns**: Modern date utility library for time formatting
- **nanoid**: Secure URL-friendly unique string ID generator

The architecture emphasizes type safety, developer experience, and cultural authenticity while maintaining scalability for future enhancements such as user authentication, content management, and advanced search capabilities.