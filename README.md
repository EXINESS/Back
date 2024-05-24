<div dir="rtl" align="justify">

# راهنمایی برای اجرای برنامه

## نصب و راه‌اندازی دیتابیس

1. نصب PostgreSQL:

قبل از شروع به هر کاری، باید PostgreSQL را بر روی سیستم خود نصب کنید. می‌توانید PostgreSQL را از [اینجا](https://www.postgresql.org/download/) دانلود و نصب کنید.

2. ایجاد superuser:

پس از نصب، باید یک superuser با دسترسی ورود به نام admin و رمز عبور 123 ایجاد کنید. این کار می‌تواند از طریق رابط کاربری PostgreSQL یا از طریق دستورات SQL انجام شود.

مراحل:

<div align="center">

<img alt="create superUser" src="readmeIamge/createSuperUser.PNG">

<img alt="superUser name" src="readmeIamge/superUserName.PNG">

<img alt="superUser password" src="readmeIamge/superUserPassword.PNG">

<img alt="superUser privileges" src="readmeIamge/superUserPrivileges.PNG">

</div>

3. ایجاد دیتابیس:

سپس به کمک superuser admin وارد PostgreSQL شوید و یک دیتابیس به نام exin ایجاد کنید. این دیتابیس باید با superuser admin به عنوان owner ایجاد شود.

<div align="center">

<img alt="create DB" src="readmeIamge/createDB.PNG">

<img alt="DB name and user" src="readmeIamge/DBName&user.PNG">

</div>

## ایجاد و راه‌اندازی محیط مجازی (Virtual Environment)

برای اجرای پروژه بهتر است، روی یک محیط مجازی آن را اجرا کنید تا مشکلی در اجرای برنامه روی سیستم اصلی شما پیش نیاید. [دلیل اجرای برنامه روی محیط مجازی](https://stackoverflow.com/questions/44392159/should-i-always-use-virtualenvs-in-django)

برای ایجاد محیط مجازی، دستور زیر را در دایرکتوری پدر پروژه اجرا کنید:

```bash
python -m venv env
```

با اجرای دستور بالا، یک محیط مجازی به نام `env` ساخته می‌شود. برای اطمینان، یک دایرکتوری با نام `env` در محل اجرای دستور باید ایجاد شود.

حال که محیط مجازی را ساختید، برای فعال‌سازی آن یکی از دو تا دستور زیر را اجرا کنید:

```bash
source env/bin/activate

env/Scripts/Activate.ps1
```

بعد از اجرا این دستور باید عبارت `(env)` پشت هر خط ترمینال اضافه شود.

ممکن است دسترسی اجرای اسکریپت در سیستم فعال نباشد که در این صورت خطایی مشاهده خواهید کرد و باید این دسترسی را فعال کنید. [اضافه کردن دسترسی اجرا اسکریپت](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-7.4)

## نصب پکیج‌ها

در ترمینالی که محیط مجازی را فعال کردید، به دایرکتوری پروژه بروید و دستور زیر را اجرا کنید تا پکیج‌های مورد استفاده در پروژه نصب شوند:

```bash
pip install -r requirements.txt
```

همیشه این دستور را قبل از اجرای برنامه اجرا کنید تا اگر در پکیج‌های استفاده شده تغییری داشته باشد، پکیج‌های جدید نصب شود و برنامه بدون خطا اجرا شود.

## به‌روزرسانی ساختار پایگاه داده و اجرای برنامه

برای بهترین اجرای برنامه، ابتدا ساختار پایگاه داده را به‌روزرسانی کنید. برای این کار دو دستور زیر را اجرا کنید:

```bash
python manage.py makemigrations
python manage.py migrate
```

سپس برای اجرای برنامه، دستور زیر را اجرا کنید:

```bash
python manage.py runserver
```

</div>
