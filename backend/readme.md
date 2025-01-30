
```
backend/
├── cmd/
│   └── server/
│       └── main.go             # Entry point of the application
├── internal/
│   ├── entities/               # Domain objects
│   │   └── user.go             # User entity
│   ├── usecases/               # Business logic for user and file management
│   │   ├── user_usecase.go
│   │   └── file_usecase.go
│   ├── interfaces/             # Interfaces layer to separate concerns
│   │   ├── repositories/       # Data access layer for user data
│   │   │   └── user_repository.go
│   │   └── handlers/           # HTTP request handlers
│   │       ├── auth_handler.go # Handles user authentication
│   │       └── file_handler.go # Handles file uploads and downloads
│   └── infrastructure/         # Framework implementations like Firebase & HTTP
│       ├── firebase/
│       │   └── auth.go         # Firebase authentication logic
│       ├── http/
│       │   ├── router.go       # HTTP router setup
│       │   └── middleware.go   # Middlewares for request handling
│       └── storage/
│           └── local.go       # Local file storage implementation
├── pkg/
│   ├── config/                 # Configuration management
│   │   └── config.go           # App config (e.g., environment variables)
│   └── utils/                  # Shared utility functions
│       ├── validator.go        # Input validation utilities
│       └── logger.go           # Logging utilities
└── go.mod                      # Go module file
```
