# Web Security Laboratory Exercises

A PHP-based collection of web-security demonstrations centered on cross-site request forgery and cross-site scripting. The project pairs small web applications with captured browser interactions to make request behavior and rendered content observable.

## Lab layout

| Directory | Purpose |
| --- | --- |
| `csrf/` | Comment-oriented target application for the CSRF exercise |
| `csrfattacker/` | Companion page demonstrating a cross-origin request interaction |
| `xss/` | Comment-oriented application for the XSS exercise |

The target applications include PHP page logic, stylesheets, text-backed comment storage, and screenshot collections. Keeping the examples small makes it straightforward to follow input from a browser request to server-side processing and page output.

## Run the demonstrations locally

Use PHP and a browser. Serve the repository as the document root:

```bash
php -S 127.0.0.1:8000
```

Open the relevant exercise:

- `http://127.0.0.1:8000/csrf/`
- `http://127.0.0.1:8000/csrfattacker/`
- `http://127.0.0.1:8000/xss/`

The companion form targets `http://localhost/csrf/index.php`; use a local web-server mapping at that origin when exercising the complete CSRF interaction. Compare request handling and rendered comments with the screenshots stored beneath each target application's `screenshots/` directory. Text files in the lab directories hold the demonstrations' comment data.

## Learning and technical focus

The exercises connect HTTP form submission, browser-origin behavior, server-side file persistence, and HTML rendering. The companion attacker page provides a concrete way to inspect a request initiated outside the target page's normal interaction, while the XSS exercise focuses attention on how submitted text enters rendered output.
