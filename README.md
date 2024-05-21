# Project_e_commerce
### Задачи проекта:
Перед выполнением основной части проекта необходимо определить, что должно считаться покупкой.
1. Определить пользователей, которые совершили покупку только один раз.
2. Посчитать сколько заказов в месяц в среднем не доставляется по разным причинам и вывести детализацияю.
3. По каждому товару определить, в какой день недели товар чаще всего покупается. 
4. Выявить сколько у каждого из пользователей в среднем покупок в неделю (по месяцам).
5. Выполнить когортный анализ пользователей. В период с января по декабрь выявить когорту с самым высоким retention на 3-й месяц. 
6. Построить RFM-сегментацию пользователей. 
### Этапы работы:
1. В первую очередь необходимо определить, что значит "покупка совершена", анализируя данные. Отсеиваем тех, кто не создал заказ. Так же фильтруем на отмену заказа и доступность. Далее считаем с группировкой по уникальному id пользователя и фильтруем по количеству покупок.
2. Определяем причины, по которым заказы могут быть не доставлены. Фильтруем данные по выявленным причинам и производим расчеты.
3. Определяем данные, которые необходимо использовать и понятие "покупается", производим необходимые расчеты.
4. Не забываем, что внутри месяца может быть не целое количество недель, учитываем это. Подготавливаем данные с помощью функций pandas и проводим расчет.
5. Перед проведением когортного анализа определяем четыре параметра:
- Признак формирования когорты — действие, которое объединяет людей в группу: первый визит, покупка, установка, регистрация и т.п. Размер когорты — временной интервал: день, неделя, месяц. Отчетный период — время исследования поведения групп. Анализируемый ключевой показатель: ROI, - - Retention Rate, LTV и т.д. Retention rate = количество активных пользователей на конец периода / количество активных пользователей на начало периода * 100%
- Признак формирования когорты — создание заказа
- Размер когорты — временной интервал: месяц (берем дату оплаты, приводим к месяцу)
- Отчетный период — с января по декабрь 2017 год
- Анализируемый ключевой показатель: Retention Rate


