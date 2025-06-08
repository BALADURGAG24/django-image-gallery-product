
# 🖼️ Django Image Gallery GUI | Product Catalog Web App

[![Python Version](https://img.shields.io/badge/python-3.10%2B-blue)](https://www.python.org/downloads/)  
[![Django Version](https://img.shields.io/badge/django-5.x-green)](https://www.djangoproject.com/)  
[![License](https://img.shields.io/badge/license-MIT-lightgrey.svg)](LICENSE)  

---

## 📋 Description

**Django Image Gallery GUI** is a beginner-friendly web application that allows users to upload, manage, and display a collection of images through a simple and responsive gallery interface.

It is an ideal project for learning:

✅ How to use Django Models, Views, Templates (MVT)  
✅ How to handle image uploads using `ImageField` + Pillow  
✅ How to configure static & media files  
✅ How to display images dynamically in a responsive layout  
✅ How to use Django Admin for content management  

---

## 🎯 Features

- 🗂 Upload product images with name & description  
- 🖼️ Automatically stores images in `/media/` directory  
- 🌟 Responsive grid gallery display (using CSS Flexbox)  
- 🔒 Secure admin panel for product management  
- 🛠 Simple and modular code structure — easy to extend  

---

## 🚀 Technologies Used

- **Python 3.10+**  
- **Django 5.x**  
- **Pillow** (Python Imaging Library)  
- **SQLite** (default Django database)  
- **HTML / CSS** (basic styles)  

---

## 📂 Project Structure

```text
imagegallery/
├── gallery/
│   ├── admin.py          # Register Product model
│   ├── apps.py
│   ├── __init__.py
│   ├── migrations/
│   │   └── __init__.py
│   ├── models.py         # Product model with ImageField
│   ├── templates/
│   │   └── index.html    # Product gallery template
│   ├── tests.py
│   ├── urls.py           # App-level URLs
│   ├── views.py          # product_list and home views
├── imagegallery/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py       # Project settings
│   ├── urls.py           # Project-level URLs
│   ├── wsgi.py
├── media/                # Uploaded images (auto-created)
├── static/               # Static files (optional, manual create)
├── manage.py
├── db.sqlite3            # SQLite Database
├── README.md             # Project README (this file)
└── requirements.txt      # Project requirements
```

---

## 🛠 Installation & Setup Instructions

### 1️⃣ Clone the repository

```bash
git clone https://github.com/yourusername/django-image-gallery-gui.git
cd django-image-gallery-gui
```

### 2️⃣ Create and activate virtual environment (optional)

```bash
python -m venv venv

# Windows
venv\Scripts\activate

# macOS / Linux
source venv/bin/activate
```

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt

# Or manually:
pip install django pillow
```

### 4️⃣ Apply database migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 5️⃣ Create superuser

```bash
python manage.py createsuperuser
```

### 6️⃣ Run development server

```bash
python manage.py runserver
```

### 7️⃣ Visit your app

- **Home Page:** [http://127.0.0.1:8000/](http://127.0.0.1:8000/)  
- **Admin Panel:** [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/)  

---

## 🖼️ How to Use

1️⃣ Go to Admin Panel → Log in as superuser  
2️⃣ Add a new Product with:  
- Name  
- Description  
- Image upload  

3️⃣ Go to Home Page → The product gallery will display your uploaded products/images.  

---

## 🗄 Media & Static Files Configuration

### `settings.py`

```python
STATIC_URL = '/static/'
STATICFILES_DIRS = [BASE_DIR / "static"]

MEDIA_URL = '/media/'
MEDIA_ROOT = BASE_DIR / "media"
```

### `urls.py`

```python
from django.conf import settings
from django.conf.urls.static import static

if settings.DEBUG:
    urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
```

---

## ✨ Example Screenshot

*(Optional — add a screenshot of your product gallery here)*

---

## 📌 Possible Improvements (Next Steps)

✅ Add product detail page  
✅ Add product categories  
✅ Add pagination  
✅ Add upload validation (image type, size limits)  
✅ Use Bootstrap or TailwindCSS for better design  
✅ Deploy to Heroku / Vercel / PythonAnywhere  

---

## 📜 License

This project is licensed under the MIT License.

---

## 🙌 Acknowledgements

- [Django Documentation](https://docs.djangoproject.com/)  
- [Pillow Documentation](https://pillow.readthedocs.io/en/stable/)  

---

## 🤝 Contributing

1️⃣ Fork the project  
2️⃣ Create your feature branch  
```bash
git checkout -b feature/AmazingFeature
```

3️⃣ Commit your changes  
```bash
git commit -m 'Add some AmazingFeature'
```

4️⃣ Push to the branch  
```bash
git push origin feature/AmazingFeature
```

5️⃣ Open a Pull Request  

---

## 📞 Contact

Created by **HARIHARANS24** → feel free to contact me!
