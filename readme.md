# PoveCloud 🌥️

PoveCloud is a platform for hosting websites and managing cloud file storage. It provides a secure environment for hosting your website along with a cloud file structure for efficient file management. The project is built in Go, designed with a clean architecture, and features both frontend and backend components to manage authentication, file uploads, and website hosting.

## Features ✨

- **Website Hosting**: Host your static and dynamic websites with ease.
- **Cloud File Storage**: Manage files securely in the cloud with a well-organized structure.
- **User Authentication**: Secure login and user management via Firebase.
- **File Management**: Upload, download, and organize files in the cloud.

## Project Structure 📁

The project is organized into several folders, each with its own responsibility:

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


<div class="highlighter-rouge"><div class="highlight"><pre class="highlight"><code>argon/
|-- frontend
    |-- App.vue
    |-- main.js
    |-- router.js
    |-- assets
    |   |-- scss
    |   |   |-- argon.scss
    |   |   |-- bootstrap
    |   |   |-- custom
    |   |-- vendor
    |       |-- font-awesome
    |       |   |-- css
    |       |   |   |-- font-awesome.css
    |       |   |   |-- font-awesome.min.css
    |       |   |-- fonts
    |       |       |-- FontAwesome.otf
    |       |       |-- fontawesome-webfont.eot
    |       |       |-- fontawesome-webfont.svg
    |       |       |-- fontawesome-webfont.ttf
    |       |       |-- fontawesome-webfont.woff
    |       |       |-- fontawesome-webfont.woff2
    |       |-- nucleo
    |           |-- css
    |           |   |-- nucleo-svg.css
    |           |   |-- nucleo.css
    |           |-- fonts
    |               |-- nucleo-icons.eot
    |               |-- nucleo-icons.svg
    |               |-- nucleo-icons.ttf
    |               |-- nucleo-icons.woff
    |               |-- nucleo-icons.woff2
    |-- components
    |   |-- Badge.vue
    |   |-- BaseButton.vue
    |   |-- BaseCheckbox.vue
    |   |-- BaseInput.vue
    |   |-- BaseNav.vue
    |   |-- BaseRadio.vue
    |   |-- BaseSlider.vue
    |   |-- BaseSwitch.vue
    |   |-- Card.vue
    |   |-- CloseButton.vue
    |   |-- Icon.vue
    |   |-- NavbarToggleButton.vue
    |-- layout
    |   |-- AppFooter.vue
    |   |-- AppHeader.vue
    |-- plugins
    |   |-- argon-kit.js
    |   |-- globalComponents.js
    |   |-- globalDirectives.js
    |-- views
        |-- Components.vue
        |-- Landing.vue
        |-- Login.vue
        |-- Profile.vue
        |-- Register.vue
        |-- components
            |-- BasicElements.vue
            |-- Carousel.vue
            |-- CustomControls.vue
            |-- DownloadSection.vue
            |-- Examples.vue
            |-- Hero.vue
            |-- Icons.vue
            |-- Inputs.vue
            |-- JavascriptComponents.vue
            |-- Navigation.vue

</code></pre></div></div>
## Requirements 🛠️

Before running PoveCloud, ensure that you have the following tools installed:

- Go (version 1.18 or later)
- Firebase account for authentication setup
- A local environment to test the application (or cloud setup)
- soon

## Installation 🔧

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/povecloud.git
   cd povecloud
   ```

2. **Install Go dependencies**:
   ```bash
   go mod tidy
   ```

3. **Set up Firebase Authentication**:
   - Go to the [Firebase Console](https://console.firebase.google.com/).
   - Create a new project and enable Firebase Authentication.
   - Download your Firebase credentials and set them up in the environment variables or `config.go`.

4. **Configure the app**:
   Edit the `config/config.go` file to set any necessary environment-specific configurations (e.g., port, Firebase settings, etc.).
## Contributing 🤝

Contributions are welcome! If you would like to improve this project, feel free to open an issue or submit a pull request. Here’s how you can contribute:

1. Fork the repository
2. Create a new branch (`git checkout -b feature-branch`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature-branch`)
5. Open a pull request
