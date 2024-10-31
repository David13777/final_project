Задание
Нам необходимо разработать интернет-ресурс для фанатского сервера одной известной MMORPG — что-то вроде доски объявлений. 
Пользователи нашего ресурса должны иметь возможность зарегистрироваться в нём по e-mail, получив письмо с кодом подтверждения 
регистрации. После регистрации им становится доступно создание и редактирование объявлений. Объявления состоят из заголовка
и текста, внутри которого могут быть картинки, встроенные видео и другой контент. Пользователи могут отправлять отклики 
на объявления других пользователей, состоящие из простого текста. При отправке отклика пользователь должен получить e-mail
с оповещением о нём. Также пользователю должна быть доступна приватная страница с откликами на его объявления, внутри которой
он может фильтровать отклики по объявлениям, удалять их и принимать (при принятии отклика пользователю, оставившему отклик,
также должно прийти уведомление). Кроме того, пользователь обязательно должен определить объявление в одну из следующих 
категорий: Танки, Хилы, ДД, Торговцы, Гилдмастеры, Квестгиверы, Кузнецы, Кожевники, Зельевары, Мастера заклинаний.

Также мы бы хотели иметь возможность отправлять пользователям новостные рассылки.

В проекте применены фреймворк Django регистрация по e-mail с помощью allauth библиотека celery сервер и библиотека redis 
Установка и запуск среды разработки клонировать репозиторий
git clone https://github.com/David13777/final_project
В консоли перейти в папку проекта и создать виртуальное окружение:
python -m venv venv
Активировать его:
venv\Scripts\activate - Windows
source venv/bin/activate - MacOs

В виртуальное окружение установить:
Python version 3.9.9
Django version 4.0.1

1.Установить библиотеку bootstrap4
pip install django-bootstrap4
2.Установить пакет allauth
pip install django-allauth
3.Установить ckeditor
pip install django-ckeditor
4.Установить библиотеку celery
pip install celery
5.Установить библиотеку redis
pip install redis
6.Установить сервер redis на локальной машине
brew install redis (MacOS)
redis-server /usr/local/etc/redis.conf (Запустить сервер)
7.Установить поддержку Redis в Celery
pip install -U "celery[redis]"
celery -A MMORPG_board worker -l INFO -B // - команда запуска Celery
python manage.py runserver //Запустить сервер приложения Django

Автор: Сокушев Давид#   f i n a l _ p r o j e c t 
 
 