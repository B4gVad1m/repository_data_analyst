# Подробное описание проекта - Выявление профиля потребления в интернет-магазине «Пока всё ещё тут»

## Презентация 📕

Ссылка: https://disk.yandex.ru/i/Dz8TyvAP3L-5aw

## Дашборд 📊

Ссылка - https://public.tableau.com/app/profile/vadim7938/viz/Dashboard_16603949769430/Dashboard1

## Описание данных 🗂

- `date` — дата заказа;
- `customer_id` — идентификатор покупателя;
- `order_id` — идентификатор заказа;
- `product` — наименование товара;
- `quantity` — количество товара в заказе;
- `price` — цена товара

Датасет описывает транзакции интернет-магазина товаров для дома и быта «Пока все ещё тут»

## Основная задача ⚠️

Сегментировать покупателей по профилю потребления

## Цель исследования 🎯

Нужно проанализировать поведение покупателей в интернет магазине «Пока всё ещё тут» и сегментировать профили потребления на основе истории их покупок

## Вывод 📝

### Исследовательский анализ данных

**Общий анализ данных**

* 2399 покупателя
* 2692 заказа
* 2329 товара

**Подробный анализ данных**
 
* Покупатель с идентификатор - c971fb21-d54c-4134-938f-16b62ee86d3b всех больше заказывал товаров и имел самую большую выручку среди других покупателей
* Самый большой заказ имеет 51 товар
* Самый дорогой заказ стоит 22056 рублей
* Самые популярные товары относятся к категории «Сад и Дача»
* Cумка-тележка 2-х колесная Gimi Argo синяя является самой прибыльным товаром. Её заказали 47 раз на общую сумму 50405 рублей
* Всех больше заказов с 1 количеством товара
* Заказы с 10 количеством товара оформяли 69 раз на сумму 79510
* Средняя цена заказа 607 рублей
* Минимальная цена заказа 9 рублей
* Максимальная цена заказа 8832 рублей
* Данные расположены в период с 1 октября 2018 года по 31 октября 2019 года

**Топ-5 популярных товаров:**

* пеларгония розебудная red pandora укорененный черенок
* пеларгония розебудная prins nikolai укорененный черенок
* пеларгония зональная диам. 12 см сиреневый полумахровый
* сумка-тележка 2-х колесная gimi argo синяя                           
* пеларгония розебудная mary укороченный черенок

**Топ-5 товаров по общей выручки:**

* сумка-тележка 2-х колесная gimi argo синяя
* сумка-тележка хозяйственная andersen scala shopper plus, lini, синяя 133-108-90
* сумка-тележка 3-х колесная gimi tris floral синяя
* сумка-тележка хозяйственная andersen treppensteiger scala shopper, hera, черная 119-004-80
* сумка-тележка 2-х колесная складная gimi flexi зеленая 

### Категоризация товара

* Товары были поделены на разные категории: "Дача и Сад", "Дом и ванна", "Кухня и еда", "Сумки и чемоданы"
* Категория "Дача и Сад" является самой популярной категорией - 61%
* В основном самая большая выручка по товарам приходится на осень, а средняя выручка на зиму

### Сегментация покупателей

**Кластер 0**

* Имеет в среднем 3 товара в заказе
* Средняя цена товара 506 рублей
* Средняя выручка заказа 597 рублей

**Кластер 1**

* Имеет в среднем 1 товар в заказе
* Средняя цена товара 3459 рублей
* Средняя выручка заказа 3870 рублей

**Кластер 2**

* Имеет в среднем 2 заказа
* Имеет в среднем 7 товаров в заказе
* Средняя цена товара 425 рублей
* Средняя выручка заказа 483 рублей

### Проверка гипотез

* Не получилось отвергнуть первую гипотезу: **есть различие в средних чеках от общей выручки по кластерам**

* Не получилось отвергнуть вторую гипотезу: **есть различие в цене от одного товара по кластерам**

## Рекомнедации 🔍

0 кластер - обычные покупателию. Нужно сначала обратить внимание на обычных покупателей, которые совершают по 1 заказу. Эти покупатели имеют наибольшую выручку по категории "Дача и сад" во время весны, когда все дачники закупаются к летнему сезону. Стоит рассылать рекламные предложения именно в это время

1 кластер - обычные покупатели с большой выручкой. Что касается покупателей с большой выручкой, то они имеет в заказе от 1 или 2 дорогих товаров категорих "Дом и ванна",  "Сумки и Чемоданы". Достаточно, чтобы этим клиентам предлогали купить ещё какие-нибудь недорогие товары по рекламным рассылкам

2 кластер - оптовики с 2 и более заказами. С оптовиками дела идут немного сложнее. У них, как и обычных покупателей категория "Дача и сад" имеет наибольшую выручку среди других категорий. Но утвержать, что они являются оптовиками нельзя, ведь некоторые покупатели могут спокойно покупать в таком объёме для своей дачи. Имеет смысл тоже рассылать рекламные предложения, как обычным покупателям

## Общая рекомендация 🔎

Следует повысить средний чек для обычных покупателей и оптовиков в категории "Дача и сад". Можно привлекать разными рекламными акциями и предлогать определённые скидки на эти товары, чтобы покупатели в дальнейшем возвращались. Ещё есть смысл добавить новую фунцкию (если её нет) - доставка прямо до дачи, так покупателям будет легче забирать товары и соответственно они смогут оформлять заказы в более большом объёме
