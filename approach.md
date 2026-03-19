graph TB
    subgraph frontend [Frontend - Next.js React]
        Pages[Pages]
        Components[Components]
        Auth[Auth UI]
    end

    subgraph backend [Backend - Supabase BaaS]
        SupaAuth[Authentication]
        Database[(PostgreSQL Database)]
        Storage[File Storage]
        Realtime[Realtime Updates]
    end

    subgraph external [Gaming APIs - Phase 4]
        Steam[Steam Web API]
        PSN[PSN API]
        Xbox[Xbox API]
    end

    Pages --> SupaAuth
    Pages --> Database
    Components --> Storage
    Auth --> SupaAuth
    Database --> Realtime
    backend --> external
