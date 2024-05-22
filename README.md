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

</div>
