# Подробное описание проекта - Исследование надежности заемщиков

##  Описание данных 🗂

 * `children` — количество детей в семье
 * `days_employed` — общий трудовой стаж в днях
 * `dob_years` — возраст клиента в годах
 * `education` — уровень образования клиента
 * `education_id` — идентификатор уровня образования
 * `family_status` — семейное положение
 * `family_status_id` — идентификатор семейного положения
 * `gender` — пол клиента
 * `income_type` — тип занятости
 * `debt` — имел ли задолженность по возврату кредитов
 * `total_income` — ежемесячный доход
 * `purpose` — цель получения кредита

## Цель исследования 🎯

Выполнить предобработку данных и ответить на вопросы:

  * Есть ли зависимость между количеством детей и возвратом кредита в срок?

  * Есть ли зависимость между семейным положением и возвратом кредита в срок?

  * Есть ли зависимость между уровнем дохода и возвратом кредита в срок?

  * Как разные цели кредита влияют на его возврат в срок?

## Ответы на вопросы 📝

 1. Зависимостью таковой нет. По данным видно, что доли должников почти одинаковыВыделяется только у кого есть 5 детей, в этой категории нет должников, но это больше похоже на аномалию, так как имеет маленькое количество детей

 2. Зависимость имеется, но небольшая. По данным видно, что категории 0, 1 и 3 имеют меньше должников по кредитам, чем категории 1 и 4

 3. Зависимость наблюдается, но очень маленькая. По данным видно, что категории B и D имееют чуть меньше должников, чем остальные категории

 4. Цели кредита почти никак не влияют на количесвто должников. По данным видно, что все доли почти одинаковы, можно выделить категории: операции с недвижимостью и проведение свадьбы, но их различие между другими данными не существенное
