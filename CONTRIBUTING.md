# Contributing to nginx-recipes

Thank you for your interest in contributing to **nginx-recipes**   
This project is built to provide clean, modular, production-ready NGINX configurations for developers and DevOps engineers. Your contributions are highly valued.

---

## 🧱 What You Can Contribute

- 🔧 New configuration templates (`templates/`)
- 🔒 Security enhancements (`security/`)
- ⚙️ App-specific examples (`examples/`)
- 📚 Guides or documentation improvements (`guides/`)
- 🐞 Bug fixes or corrections in current configurations
- 🧪 Performance optimizations or benchmarks
- 🌍 Internationalization/localization of guides (future)

---

## 📁 File Naming & Folder Rules

- Use lowercase, hyphenated filenames: `reverse_proxy.conf`
- Keep reusable snippets small and isolated (`security/headers.conf`)
- Group complete setups under a folder:  
  e.g., `examples/flask_app/nginx.conf`

---

## ✅ Configuration Standards

All configuration files should:

- Follow official NGINX syntax (test using `nginx -t`)
- Use `include` for modularization where appropriate
- Include **comments** explaining non-obvious directives
- Prioritize **security**, **performance**, and **readability**
- Use relative paths or clearly document required absolute paths
- Avoid hardcoded sensitive values (e.g., domain names, secrets)

---

## 🧪 Testing Your Contribution

Please ensure you:

1. Test configs locally with `nginx -t`
2. Reload NGINX to confirm no runtime errors (`nginx -s reload`)
3. Use an actual service (Node.js, Flask, etc.) if contributing to `/examples`

Optional tools for advanced validation:
```bash
# syntax check
nginx -t

# benchmark test
wrk http://localhost:80
