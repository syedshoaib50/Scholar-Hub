# Scholar-Hub
## Complete Setup Guide

---

## STEP 1: Create Laravel Project

```bash
composer create-project laravel/laravel school
cd school
code .
```

---

## STEP 2: Configure Database (.env)

Edit `.env` and set your database credentials:
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=school
DB_USERNAME=root
DB_PASSWORD=
```

Create the database in MySQL:
```sql
CREATE DATABASE school;
```

---

## STEP 3: Copy All Project Files

Copy these files from the downloaded package into your Laravel project:

| Source File | Destination |
|---|---|
| `app/Models/Student.php` | `app/Models/Student.php` |
| `app/Models/Classes.php` | `app/Models/Classes.php` |
| `app/Http/Controllers/StudentController.php` | `app/Http/Controllers/StudentController.php` |
| `app/Http/Controllers/ClassController.php` | `app/Http/Controllers/ClassController.php` |
| `database/migrations/*` | `database/migrations/` |
| `routes/web.php` | `routes/web.php` |
| `resources/views/**` | `resources/views/` |

---

## STEP 4: Run Migration

```bash
php artisan migrate
```

---

## STEP 5: Start the Server

```bash
php artisan serve
```

Open: http://127.0.0.1:8000

---

## FEATURES INCLUDED

✅ Students — List, Add, Edit, Delete  
✅ Classes — List, Add, Edit, Delete  
✅ Student ↔ Class relationship (belongsTo / hasMany)  
✅ Form validation with error messages  
✅ Success/error flash messages  
✅ Student count per class  
✅ Beautiful responsive design (ScholarHub theme)  
✅ Confirmation dialogs before deletion  

---

## ROUTES SUMMARY

| Method | URL | Action |
|---|---|---|
| GET | /students | List all students |
| GET | /students/create | Show add form |
| POST | /students | Save new student |
| GET | /students/{id}/edit | Show edit form |
| PUT | /students/{id} | Update student |
| DELETE | /students/{id} | Delete student |
| GET | /classes | List all classes |
| GET | /classes/create | Show add form |
| POST | /classes | Save new class |
| GET | /classes/{id}/edit | Show edit form |
| PUT | /classes/{id} | Update class |
| DELETE | /classes/{id} | Delete class |
