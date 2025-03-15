**I. Nginx Fundamentals**

*   Understanding Nginx Architecture
    *   Master process and worker processes
    *   Event-driven architecture
    *   Modules: Core, standard, and third-party
*   Installing and Configuring Nginx
    *   Installation from source vs. package manager (e.g., `apt`, `yum`, `brew`)
    *   Directory structure: `/etc/nginx/`, `/var/log/nginx/`, `/usr/share/nginx/`
    *   Configuration file syntax: blocks, directives, and contexts
*   Basic Configuration Directives
    *   `worker_processes`, `worker_connections`
    *   `include` for modular configuration
    *   `user` directive
    *   `error_log` and `access_log` directives
*   Serving Static Content
    *   `root` directive
    *   `index` directive
    *   `location` blocks for defining URL mappings
    *   Example: Configuring Nginx to serve HTML, CSS, and JavaScript files

**II. HTTP Server Features**

*   Virtual Hosts
    *   Name-based virtual hosts
    *   IP-based virtual hosts
    *   `server` blocks configuration: `server_name`, `listen` directives
    *   Example: Configuring multiple websites on a single server
*   Request Processing
    *   `location` block modifiers: `=`, `~`, `~*`, `^~`
    *   `try_files` directive for handling missing files
    *   `error_page` directive for custom error pages
    *   Example: Handling 404 errors and redirecting requests
*   Access Control
    *   `allow` and `deny` directives for IP-based restrictions
    *   `ngx_http_auth_basic_module` for basic authentication
    *   Creating `.htpasswd` files using `htpasswd` utility
    *   Example: Restricting access to specific directories
*   Logging and Monitoring
    *   Customizing access log formats
    *   Using `ngx_http_stub_status_module` for basic server statistics
    *   Integration with monitoring tools (e.g., Prometheus)

**III. Reverse Proxy and Load Balancing**

*   Reverse Proxy Fundamentals
    *   Understanding the reverse proxy concept
    *   `proxy_pass` directive for forwarding requests to backend servers
    *   `proxy_set_header` directive for modifying request headers
    *   `proxy_buffering` and `proxy_cache` for performance optimization
    *   Example: Configuring Nginx as a reverse proxy for an application server (e.g., Node.js, Python)
*   Load Balancing Algorithms
    *   `upstream` block for defining backend servers
    *   `round-robin` load balancing (default)
    *   `least_conn` load balancing
    *   `ip_hash` load balancing
    *   `backup` server configuration
    *   Example: Distributing traffic across multiple backend servers
*   Health Checks
    *   `ngx_http_upstream_module` directives for health checks
    *   `max_fails` and `fail_timeout` directives
    *   `slow_start` directive for gradual server recovery
    *   Example: Configuring health checks to automatically remove unhealthy servers from the load balancer

**IV. Caching and Performance Tuning**

*   Nginx Caching
    *   `proxy_cache_path` directive for defining cache storage
    *   `proxy_cache` directive for enabling caching
    *   `proxy_cache_key` directive for customizing cache keys
    *   `proxy_cache_valid` directive for setting cache expiration times
    *   Purging the cache using `ngx_cache_purge` module
    *   Example: Caching static content and dynamic content with appropriate expiration policies
*   Gzip Compression
    *   `gzip` directive for enabling gzip compression
    *   `gzip_types` directive for specifying MIME types to compress
    *   `gzip_comp_level` directive for setting compression level
    *   Example: Configuring gzip compression to reduce bandwidth usage
*   SSL/TLS Configuration
    *   Obtaining SSL/TLS certificates from Let's Encrypt or other providers
    *   `listen` directive with `ssl` parameter
    *   `ssl_certificate` and `ssl_certificate_key` directives
    *   `ssl_protocols` and `ssl_ciphers` directives for security hardening
    *   Redirecting HTTP traffic to HTTPS
    *   Example: Configuring secure HTTPS connections with strong ciphers and protocols
*   Tuning for Performance
    *   Optimizing `worker_processes` and `worker_connections` based on server resources
    *   Using `epoll` or `kqueue` for efficient event handling
    *   Increasing buffer sizes for request and response headers
    *   Minimizing disk I/O by using memory caching
    *   Using PageSpeed module for automatic optimization

**V. Advanced Topics**

*   Nginx Plus Features
    *   Dynamic reconfiguration
    *   Advanced monitoring and analytics
    *   Session persistence
    *   Active health checks
*   Lua Scripting with Nginx (ngx_lua module)
    *   Embedding Lua code in Nginx configuration files
    *   Accessing Nginx variables and functions from Lua scripts
    *   Implementing custom authentication and authorization logic
    *   Building dynamic web applications with Lua and Nginx
*   Microservices and API Gateway
    *   Using Nginx as an API gateway for routing requests to microservices
    *   Implementing authentication and authorization for APIs
    *   Rate limiting and throttling
    *   Request transformation and aggregation
*   Module Development
    *   Understanding the Nginx module API
    *   Creating custom Nginx modules in C
    *   Example: Building a simple module that modifies request headers.
