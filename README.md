# Консольное приложение для подачи показаний.
При запуске приложения создается пользователь "admin" с паролем "admin" и правами администратора.
Данные хранятся только в памяти приложения.
Показания можно ввести только один раз.

Пока пользователь не вошел в систему доступны команды: 
    - login - войти в систему
    - reg   - зарегистрироваться в системе
    - exit  - завершить работу приложения

Для пользователя без прав администратора доступны команды:
    - input             - ввести показания
    - show              - отобразить все показания
    - show 2024 JANUARY - отобразить показания за январь 2024 (возможно задать любой другой месяц и год)
    - logout            - завершить сеанс работы пользователя

Для администратора доступны дополнительные команды:
    - show_users    - показать всех пользователей
    - role_admin    - назначить пользователя администратором
    - log           - вывести лог
    - new_ind       - добавить новый показатель
    - show_user_ind - отобразить показания пользователя


# ЗАДАНИЕ:
Monitoring-Service
Разработайте веб-сервис для подачи показаний счетчиков отопления, горячей и холодной воды

Описание
Показания можно подавать один раз в месяц.
Ранее поданые показания редактировать запрещено.
Последние поданые показания считаются актуальными.
Пользователь может видеть только свои показания, администратор может видеть показания всех пользователей.
Создайте реализацию, которая соответствует описанным ниже требованиям и ограничениям.

Требования
- предусмотреть расширение перечня подаваемых показаний
- данные хранятся в памяти приложения
- приложение должно быть консольным (никаих спрингов, взаимодействий с БД и тд, только java-core и collections)
- регистрация пользователя
- авторизация пользователя
- реализовать эндпоинт для получения актуальных показаний счетчиков
- реализовать эндпоинт подачи показаний
- реализовать эндпоинт просмотра показаний за конкретный месяц
- реализовать эндпоинт просмотра истории подачи показаний
- реализовать контроль прав пользователя
- Аудит действий пользователя (авторизация, завершение работы, подача показаний, получение истории подачи показаний и тд)

Нефункциональные требования
Unit-тестирование

Доп. материалы: https://drive.google.com/drive/folders/1rZaq58yAAcBKZqBeNSfpc6kb-GkuqHs0?usp=sharing
