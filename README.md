
# 🛒 Django Product Catalog

This is a Django take-home assignment project that models **products**, **categories**, and **tags** with proper relationships, search and filter functionality, and a basic user interface. It demonstrates your ability to work with Django models, querysets, and views.

---

## ✅ Features

- Models for `Product`, `Category`, and `Tag` with correct Django relationships
- Django admin interface for populating the database
- Filter products by category and tags
- Search products by description
- Combine search + filter on a single HTML page
- Simple HTML frontend using Django templates (no JS frameworks)

---

## 🗂 Models and Relationships

### Product
- `name` (CharField)
- `description` (TextField)
- `category` (ForeignKey to Category)
- `tags` (ManyToManyField to Tag)

### Category
- `name` (CharField)

### Tag
- `name` (CharField)

✅ Each product belongs to **one category** and can have **multiple tags**.

---

## 📌 Assignment Requirements & How They’re Met

### ✅ Step 1: Create Django models with correct relationships
Implemented `Product`, `Category`, and `Tag` models with ForeignKey and ManyToManyField.

### ✅ Step 2: Populate the database using Django admin
Admin enabled via:
```python
admin.site.register(Product)
admin.site.register(Category)
admin.site.register(Tag)
```
Sample data was added manually:
- 5+ Categories
- 10+ Tags
- 20+ Products

### ✅ Step 3: Implement search and filter functionality
Implemented in `catalog/views.py`:
- Search by `description__icontains`
- Filter by `category__id` and `tags__id`

### ✅ Step 4: Build an HTML page for user interaction
Template at `catalog/templates/catalog/product_list.html` with form controls and product display.

### ✅ Step 5: Demonstrate proficiency in Django queries
Querysets filtered dynamically based on user input using `request.GET`.

### ✅ Step 6: Submit complete project + README
This README includes:
- Setup instructions
- Assumptions
- Project structure
- Usage

---

## ⚙️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/rohithbadri1011/Django_assignment.git
cd Django_assignment
```

### 2. (Optional) Create a Virtual Environment
```bash
python -m venv env
source env/bin/activate  # Windows: env\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Apply Migrations
```bash
python manage.py makemigrations
python manage.py migrate
```

### 5. Create Admin User
```bash
python manage.py createsuperuser
```

### 6. Run the Server
```bash
python manage.py runserver
```

Visit:
- [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/) — Admin Panel
- [http://127.0.0.1:8000/](http://127.0.0.1:8000/) — Product Search Page

---

## 🧪 Data Population

Log in to the Django admin and add:
- ✅ At least 5 categories
- ✅ At least 10 tags
- ✅ At least 20 products (each linked to one category and multiple tags)

---

## 🔍 Product Search & Filter Page

Users can:
- Search products by description
- Filter by category
- Filter by tag
- Combine all filters for refined results

---

## 📁 Project Structure

```
Django_assignment/
├── catalog/
│   ├── admin.py
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   └── templates/
│       └── catalog/
│           └── product_list.html
├── product_catalog/
│   ├── settings.py
│   ├── urls.py
├── db.sqlite3
├── manage.py
├── requirements.txt
└── README.md
```

---

## 📄 Sample `requirements.txt`

```txt
Django>=4.0,<5.0
```

To generate:
```bash
pip freeze > requirements.txt
```

---

## 🧠 Assumptions

- Frontend design is not the focus — styling is kept basic.
- Users will use the admin panel to populate data.
- Filtering assumes single category and single tag per filter (not multi-select).
- Tags and categories must be created before assigning them to products.

---

## 🧱 Front-End Framework

No frontend frameworks were used. This project is built with:
- Django templating system
- HTML forms
- Plain CSS (if any)

---

## 👤 Author

Rohith Badri  
GitHub: [@rohithbadri1011](https://github.com/rohithbadri1011)

---

## 📬 Submission

- All code is committed and pushed to GitHub: [https://github.com/rohithbadri1011/Django_assignment](https://github.com/rohithbadri1011/Django_assignment)
- This README serves as complete documentation.
