# Анализ метрик эффективности рассылок компании, оказывающей профессиональные услуги

Используемые библиотеки: `pandas`, `numpy`, `plotly.express`

## Задача
Расчитать средние метрики и метрики в разрезе групп рассылок: 
- Открываемость (open rate)
- Кликабельность (click-through rate)
- Переходы по отношению к открытиям (click-to-open rate)
- Процент отписок (unsubscribe rate)
- Процент возвратов (bounce rate)

Для сравнения использованы средние для отрасли компании показатели метрик, согласно [US Email Marketing Benchmarks (2020)](https://www.campaignmonitor.com/resources/guides/us-email-marketing-benchmarks-2020-by-day-and-industry/)


![Воронка отправки, доставки, октрытий, переходов](<https://raw.githubusercontent.com/paraseusse/Analysis-of-conversions-from-RFP-via-site-to-won-opportunities/main/%D0%92%D0%B8%D0%B7%D1%83%D0%B0%D0%BB%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D0%B8/%D0%92%D0%BE%D1%80%D0%BE%D0%BD%D0%BA%D0%B0%20%D0%B4%D0%BB%D1%8F%20%D1%83%D1%81%D1%80%D0%B5%D0%BD%D0%B5%D0%BD%D0%BD%D1%8B%D1%85%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85%20%D0%B7%D0%B0%206%20%D0%BC%D0%B5%D1%81%D1%8F%D1%86%D0%B5%D0%B2.png?token=AMTEIGARISIQNHLOXYCUW3K7XZQN6>)

## Рекомендации

- Рассылки имеют высокие показатели метрик: click-through rate и click-to-open rate (они взаимосвязаны).
- Хороший показатель открываемости (open rate): 14%, однако он незначительно ниже, чем в среднем по отрасли (16%).
- Самая большая проблема с процентом возвратов (bounce rate), он составляет 12%, и этот показатель в 10 раз превышает средний по рынку (1.3%). Так как unsubscribe rate низкий, полагаю, что дело в метрвых адресах.

### Открываемость (open rate) чуть ниже, чем по отрасли
- Тема письма очень важна, так как основная доля пользователей теряется на этапе открытия письма, необходимы заклекающие заголовки
- Валидация email адресов, чистка базы
- Выбор времени отправки: согласно US Email Marketing Benchmarks (2020) оптимальное время для финансовых услуг: понедельник и среда

### Процент возвратов (bounce rate) значительно выше, чем в среднем по отрасли
- Валидация email адресов, чистка базы, удаление несуществующих адресов

### Невозможно расчитать конверсию (сколько подписчиков выполнили целевое действие)
- Интегрировать систему рассылок с системой аналитики и отслеживать источники переходов при помощи utm-меток
- Назначить целевое действие: форма запроса
