# Django-CRUD-MySQL
Simple CRUD menggunakan Django dengan MySql

## Installation

1. Buatlah folder root misalkan djocrud

- masuk ke folder djocrud lalu buatlah virtualenv

```bash
virtualenv venv
```
- kalau sudah ketik di commandline 
```bash 
venv\Script\Activate
```
- masih difolder djocrud dan buat lagi folder dengan nama empset.

- Setelah masuk folder empset, download repo ini lalu masukan semua sourcecode yang sudah didownload dan copy paste ke dalam folder emset.

- Maka urutan folder menjadi : djocrud > empset > empset, employee dan code manage.py

2. Buat database
```bash
# disini kita memakai mysql
CREATE DATABASE db_emp
```

3. Install Konektor MySQL
```bash
pip install mysqlclient
``` 

4. Settings djocrud

- Buka settings.py pada empset, dan pastikan seperti ini

```bash
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'db_emp',
        'USER': 'root',
        'PASSWORD': '',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```

- selanjutnya pindah directory djocrud > empset, lalu run command berikut ini
```bash
python manage.py makemigrations  
```
```bash
python manage.py migrate  
```
- masih di folder yang sama, saatnya running appsnya
```bash
python manage.py runserver
```
