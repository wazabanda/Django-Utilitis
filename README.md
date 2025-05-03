# Django-Utilitis

A repository containing apps, templates, and other functions that can be used in different projects.

---

## Overview

**Django-Utilitis** is a modular and reusable collection of tools for Django developers. This includes:

- Reusable Django apps that can be dropped into multiple projects
- Base templates and component partials for consistent UI
- Utility functions and mixins for views, forms, models, etc.
- Miscellaneous helpers and features that speed up Django development

Some parts of this repository may eventually be turned into Python packages and published to PyPI.

---

## Features

- 🧱 **Pluggable Django apps** (e.g. audit logs, user profiles)
- 🧩 **Reusable templates** for layout, forms, and components
- ⚙️ **Utility functions** for emails, files, querysets, etc.
- 📦 **Custom mixins** for class-based views, models, and forms
- 📁 Well-structured for maintainability and packaging

---

## Project Structure

```

django-utilitis/
├── apps/                  # Independent Django apps
│   ├── auditlog/
│   ├── user\_profiles/
│   └── ...
│
├── templates/             # Reusable templates
│   ├── base.html
│   ├── components/
│   │   ├── navbar.html
│   │   ├── footer.html
│   │   └── ...
│   └── ...
│
├── utils/                 # General-purpose utility code
│   ├── mixins/            # Mixins split by context
│   │   ├── view\_mixins.py
│   │   ├── form\_mixins.py
│   │   ├── model\_mixins.py
│   │   └── ...
│   ├── email.py
│   ├── file\_helpers.py
│   └── ...
│
├── static/                # Shared static files (if any)
│   └── ...
│
├── tests/                 # App-level or global tests
│   └── ...
│
└── README.md              # You’re reading it

````

---

## Getting Started

Clone the repository:

```bash
git clone https://github.com/wazabanda/Django-Utilitis
````

Include a desired app in your Django project:

```python
# settings.py
INSTALLED_APPS = [
    ...
    'apps.auditlog',
]
```

Import mixins or utils wherever needed:

```python
from utils.mixins.view_mixins import LoginRequiredMixin
from utils.email import send_custom_email
```

Use shared templates by setting the template directories:

```python
# settings.py
TEMPLATES = [
    {
        ...
        'DIRS': [BASE_DIR / "templates"],
        ...
    },
]
```

---

## Example Use Case

Say you're building a new project and need:

* User activity tracking → use `apps.auditlog`
* A consistent base UI → extend from `templates/base.html`
* View-level access control → import from `utils.mixins.view_mixins`

This repo provides all that and more.

---

## Future Plans

* Publish stable apps as standalone pip packages
* Add more form widgets, template tags, and filters
* Include tests and CI/CD pipeline
* Document each module in detail

---

## Contributing

Pull requests and issue submissions are welcome! If you have utilities or apps you’ve found useful across projects, feel free to contribute them to this repo.

---

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for full details.

---

## Author

Built and maintained by \[Your Name]
Email: [1wazabanda@gmail.com](mailto:1wazabanda@gmail.com)

---


