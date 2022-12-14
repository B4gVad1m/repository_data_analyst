# Подробное описание проекта - А/B-тест

## Описание данных 🗂

Файл `ab_project_marketing_events.csv` — календарь маркетинговых событий на 2020 год

* `name` — название маркетингового события;
* `regions` — регионы, в которых будет проводиться рекламная кампания;
* `start_dt` — дата начала кампании;
* `finish_dt` — дата завершения кампании

Файл `final_ab_new_users.csv` — все пользователи, зарегистрировавшиеся в интернет-магазине в период с 7 по 21 декабря 2020 года

* `user_id` — идентификатор пользователя;
* `first_date` — дата регистрации;
* `region` — регион пользователя;
* `device` — устройство, с которого происходила регистрация

Файл `final_ab_events.csv` — все события новых пользователей в период с 7 декабря 2020 по 4 января 2021 года

* `user_id` — идентификатор пользователя;
* `event_dt` — дата и время события;
* `event_name` — тип события;
* `details` — дополнительные данные о событии. Например, для покупок, purchase, в этом поле хранится стоимость покупки в долларах

Файл `final_ab_participants.csv` — таблица участников тестов

* `user_id` — идентификатор пользователя;
* `ab_test` — название теста;
* `group` — группа пользователя

## Техническое задание 📂

* Название теста: `recommender_system_test`;
* Группы: `А` (контрольная), `B` (новая платёжная воронка);
* Дата запуска: 2020-12-07;
* Дата остановки набора новых пользователей: 2020-12-21;
* Дата остановки: 2021-01-04;
* Аудитория: 15% новых пользователей из региона `EU`;
* Назначение теста: тестирование изменений, связанных с внедрением улучшенной рекомендательной системы;
* Ожидаемое количество участников теста: 6000
* Ожидаемый эффект: за 14 дней с момента регистрации в системе пользователи покажут улучшение каждой метрики не менее, чем на 10%:
    * конверсии в просмотр карточек товаров — событие `product_page`
    * просмотры корзины — `product_cart`
    * покупки — `purchase`

## Постановка задачи 🎯

Задача — провести оценку результатов A/B-теста. В распоряжении есть датасет с действиями пользователей, техническое задание и несколько вспомогательных датасетов:

* Оценить корректность проведения теста;
* Проанализировать результаты теста

Чтобы оценить корректность проведения теста, нужно проверить:

* Пересечение тестовой аудитории с конкурирующим тестом;
* Совпадение теста и маркетинговых событий, другие проблемы временных границ теста

## Вывод 📝

**Несоответствие теста условиям ТЗ**

* Данные теста заканчивается **30 декабря**, а не 4 января
* Доля от новых пользователей региона EU - **7.52%**, заместо 15%
* Имеем **3481 пользователя**, вместо ожидаемых 6000

**Вывод по прудуктовой воронки между группами**

**Группа A**

* 100% пользователей авторизируются
* 65% заходят на страницу продукта
* 30% добовляют товар в корзину
* 32% покупают товар

**Группа B**

* 100% пользователей авторизируются
* 56% заходят на страницу продукта
* 27% добовляют товар в корзину
* 28% покупают товар

Заметна большая разница по размерам групп. В группе А наблюдается намного больше активности

Группа А лучше конвертируется по переходом, чем группа B. Из этого можно сделать вывод, что внедрение рекомендательной системы никак не повлияло на конверсию каждого события. Даже наоборот результаты ухудшились по сравнению с контрольной группы

**Результаты теста**

По данному тесту достоверных выводов не сделать, многие данные не совпадают условиям **ТЗ**. В этом случае нужно перезапустить тест, но только с обновлёнными данными
