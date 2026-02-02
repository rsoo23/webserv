## Webserv Project Overview

This project is a custom web server implementation using C++98 supporting multiple features and technologies. It is designed to handle HTTP requests, serve static and dynamic content, and provide extensible support for CGI scripts and user authentication. Below is a general outline of its main features and components:

### Features

- **Custom HTTP Server**: Implements core HTTP protocol handling, request parsing, and response generation.
- **Static File Serving**: Serves HTML, CSS, JS, and other static assets from the `www/` directory and other configured roots.
- **Directory Listing (AutoIndex)**: Generates directory listings for folders when no index file is present.
- **CGI Support**: Executes CGI scripts (Python, C++) from the `cgi-bin/` and `capitalize/` directories, enabling dynamic content and form handling.
- **Configurable via .conf Files**: Supports multiple configuration files in `config_files/` for flexible server setup (ports, error pages, root directories, etc.).
- **Custom Error Pages**: Returns user-friendly error pages for common HTTP errors (400, 403, 404, 405, etc.) from `www/error_pages/`.
- **User Authentication & Cookies**: Includes a demo authentication system in `cookies_site/` with registration, login, session management, and cookie handling.
- **File Uploads**: Handles file uploads via CGI scripts, storing files in designated directories.
- **Multiple HTTP Methods**: Supports GET, POST, PUT, DELETE, and HEAD methods with custom logic for each.
- **Extensible Architecture**: Modular C++ classes for blocks (server, location, etc.), request handling, and utilities.

### Main Components

- **src/**: Core C++ source files for server logic, HTTP handling, configuration parsing, and utilities.
- **includes/**: Header files defining server blocks, request/response classes, CGI handling, and utility functions.
- **cgi-bin/**: Python CGI scripts for dynamic content, environment display, file upload, and testing.
- **capitalize/**: C++ CGI demo for string manipulation and form handling.
- **cookies_site/**: Demo web app for user authentication, cookie management, and profile handling.
- **www/**: Static website files, including landing page, styles, scripts, and error pages.
- **config_files/**: Example configuration files for different server setups.
- **test/**: Additional HTML/CSS test files.

### How to Use

1. **Clone the Repository**
```bash
git clone https://github.com/rsoo23/webserv.git
```

2. **Build the Server**
```bash
make
```

3. **Configure**: Edit configuration files in `config_files/` to set up ports, roots, error pages, etc.

4. **Run**: Launch the server binary and access via browser or HTTP client.
```bash
./webserv config_files/*.conf

Enter in browser:
localhost:8080
```


### Credits

Developed by Rong Jie (rsoo), Jack (nwai-kea), Ijon (itan).
