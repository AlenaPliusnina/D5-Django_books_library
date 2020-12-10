# Приложение "Библиотека" на Django v2

* Первая версия приложения - https://github.com/AlenaPliusnina/Django_books_library_v1

      Django, Sqlite3
      
Описание:

      Приложение — личная библиотека. Это простая система, в которой храниться и отображаться информация о книгах, 
      которые в нее добавлены, а также есть возможность эти данные создавать, удалять и редактировать.

      Новое в v2:

         - появилась возможность через приложение (при помощи страниц с формаими) создавать книги и авторов в библиотеку
         - добавлен список друзей и взятых ими книг (управление через панель админмстратора Django)


Разворачиваем проект локально:

1. Создайте виртуальное окружение: 

       python3 -m venv env
       
2. Активируйте виртуальное окружение: 

       source env/bin/activate
       
3. Чтобы установить требуемые зависимости выполните команду: 

       pip install -r requirements.txt
   
   Если у вас macOS и при установке зависимостей возникает ошибка:  error: command 'gcc' failed with exit status 1.   
   Попробуйте команду: env LDFLAGS="-I/usr/local/opt/openssl/include -L/usr/local/opt/openssl/lib" pip install psycopg2==2.8.4
       
4. Чтбы запустить сервер введите команду: 

       python manage.py runserver

5. Для входа в администравтивную панель проекта создайте суперпользователя при помощи команды: 

       python manage.py createsuperuser

Список роутов проекта:

1. http://127.0.0.1:8000/admin/ - панель администратора Django

2. http://127.0.0.1:8000/index/ - таблица книг в билиотеке (есть также кнопки позволяющие увеличить/уменьшить колличество экземпляров)

![Список книг в библиотеке](https://github.com/AlenaPliusnina/Django_books_library_v2/blob/master/screenshots/screen_1.png)

3. http://127.0.0.1:8000/publishers/ - вывод списка издательств и их книг

![Список издательств](https://github.com/AlenaPliusnina/Django_books_library_v2/blob/master/screenshots/screen_2.png)

4. http://127.0.0.1:8000/author/create/ - создать нового автора (формы)

![Список издательств](https://github.com/AlenaPliusnina/Django_books_library_v2/blob/master/screenshots/screen_3.png)

5. http://127.0.0.1:8000/author/create_many/ - создать несколько авторов за один раз (формы)

![Список издательств](https://github.com/AlenaPliusnina/Django_books_library_v2/blob/master/screenshots/screen_4.png)

6. http://127.0.0.1:8000/authors/ - список авторов, книги которых есть в библиотеке

![Список издательств](https://github.com/AlenaPliusnina/Django_books_library_v2/blob/master/screenshots/screen_5.png)

7. http://127.0.0.1:8000/author_book/create_many/ - добавить несколько авторов и несколько книг одновременно (формы);

![Список издательств](https://github.com/AlenaPliusnina/Django_books_library_v2/blob/master/screenshots/screen_6.png)

8. http://127.0.0.1:8000/friends/ - вывод списка друзей и книг, взятых ими из библиотеки

![Список издательств](https://github.com/AlenaPliusnina/Django_books_library_v2/blob/master/screenshots/screen_7.png)
