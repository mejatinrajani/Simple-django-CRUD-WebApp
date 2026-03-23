# AddKijai

A simple Django project for adding and managing products with images and a lightweight businessman panel.

## Overview

This repository contains a small Django app (`addlist`) and a set of templates and static assets for a minimal product-management demo. It uses SQLite for storage and stores product images under `media/product_images/`.

Key files:

- [manage.py](manage.py) — Django project entrypoint.
- [mainproject/settings.py](mainproject/settings.py) — Django settings.
- [addlist/models.py](addlist/models.py) — product models.
- [addlist/views.py](addlist/views.py) — views and business logic.
- [templates/addproduct.html](templates/addproduct.html), [templates/home.html](templates/home.html) — main templates.
- [LICENSE.md](LICENSE.md) — project license.

## Features

- Add, list and delete products
- Upload and serve product images
- Simple businessman/admin panel UI

## Prerequisites

- Python 3.8+ (tested with 3.8–3.11)
- pip

Optional (for virtualenv):

```
python -m venv .venv
.venv\Scripts\activate
```

## Installation

1. Clone the repo and change to the project directory:

```powershell
cd mainproject
```

2. Install dependencies (if you have a `requirements.txt`, otherwise ensure Django is installed):

```powershell
pip install -r requirements.txt
# or
pip install django
```

3. Run migrations and create a superuser:

```powershell
python manage.py migrate
python manage.py createsuperuser
```

4. Collect static files (if you plan to serve static in production):

```powershell
python manage.py collectstatic
```

5. Run the development server:

```powershell
python manage.py runserver
```

Open http://127.0.0.1:8000/ to view the site.

## Media files

Product images are stored in `media/product_images/`. During development Django will serve these files when `DEBUG = True`.

## Project Structure

```
mainproject/
├─ addlist/           # App containing models, views, migrations
├─ mainproject/       # Project settings and WSGI/ASGI
├─ templates/         # HTML templates
├─ demostatic/        # CSS and other static files
└─ media/             # Uploaded media (product_images/)
```

## Tests

If you add tests, run them with:

```powershell
python manage.py test
```

## Contributing

1. Create a branch for your feature or fix.
2. Open a pull request with a clear description.

## License

This project is licensed under the terms in [LICENSE.md](LICENSE.md).

---

If you'd like, I can also:

- Add a `requirements.txt` generated from your environment
- Add badges or a quick demo GIF
- Commit this README to a branch and open a PR

Feel free to tell me which of the above you'd like next.
