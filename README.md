# Житловий Комплекс — Flask Проєкт

## 🔍 Опис
Веб-сайт житлового комплексу, розроблений з використанням Flask (Python) та JavaScript. Мета проєкту — полегшити взаємодію мешканців із керівництвом ЖК та між собою.

## 📦 Технології
- Flask
- Flask-SQLAlchemy
- Flask-Login
- SQLite
- HTML/CSS + JavaScript

## 🔧 Функціонал
- Реєстрація мешканця
- Авторизація
- Перевірка/підтвердження акаунту адміністратором
- Адмін-панель
- Внесення показників (газ, світло, вода тощо)
- Перегляд параметрів квартири
- Виклик майстра
- Замовлення продуктів
- Продаж / оренда квартири

# Дані для входу в адмінку
- Email: admin@example.com
- Пароль: adminpass

## 🧪 Встановлення
1. Клонуйте репозиторій:
   ```bash
   git clone <your_repo_url>
   cd <project_folder>
   
2. Встановіть залежності

pip install -r requirements.txt

3. 🛠 Ініціалізація бази даних
В інтерпретаторі Python або окремим файлом:

>>> from app import db
>>> db.create_all()
>>> exit()
4. Адмінка
Створення адміністратора вручну:
   flask shell

>>> from app import db, User

   >>>from werkzeug.security import generate_password_hash
   >>>admin = User(
   >>>    full_name="Адмін",
   >>>    email="admin@example.com",
   >>>    password=generate_password_hash("пароль"),
   >>>    phone="+380000000000",
   >>>    apartment="ADMIN",
   >>>    is_admin=True,
   >>>    is_approved=True
   >>>)
   >>>db.session.add(admin)
   >>>db.session.commit()
