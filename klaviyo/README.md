# Klaviyo — email-маркетинг

Набір md-файлів для створення, налаштування та ведення email-маркетингу Butterflarium (Shopify-магазин вітражних комах/сувенірів) через Klaviyo. Як і в розділі [`google-ads/`](../google-ads/README.md), файли розраховані на те, що ними користується і людина, і Claude у майбутніх сесіях — кожен файл одразу дає контекст без переказування.

## Файли та коли їх відкривати

| Файл | Коли використовувати |
|---|---|
| [`account-overview.md`](account-overview.md) | Загальний контекст: бізнес, цілі email-каналу, тариф, інтеграції, доступи. Відкривати першим у будь-якій новій розмові про email. |
| [`setup-checklist.md`](setup-checklist.md) | Покроковий чекліст запуску Klaviyo з нуля: акаунт → домен → Shopify → трекінг → форми → флоу → перша кампанія. Відмічати пройдені кроки. |
| [`deliverability.md`](deliverability.md) | Доставлюваність: DNS (SPF/DKIM/DMARC), брендований домен відправки, прогрів, вимоги Gmail/Yahoo, гігієна бази. |
| [`lists-segments.md`](lists-segments.md) | Довідник списків і сегментів: точні умови, призначення, де використовуються. |
| [`signup-forms.md`](signup-forms.md) | Форми підписки (popup / flyout / embed): оффер, тригери, таргетинг, результати тестів. |
| [`flows.md`](flows.md) | Реєстр автоматизацій (Welcome, Abandoned Checkout, Browse Abandonment, Post-Purchase, Win-back, Sunset…) — структура листів, таймінги, фільтри, статус. |
| [`campaigns-calendar.md`](campaigns-calendar.md) | Контент-календар розсилок на рік: сезонні приводи для США, частота, плани по місяцях. |
| [`campaign-log.md`](campaign-log.md) | Журнал відправлених кампаній з результатами (open/click/revenue) і висновками. |
| [`content-guidelines.md`](content-guidelines.md) | Тон голосу, структура листа, дизайн-шаблони, правила для subject line / preheader, UTM. |
| [`ab-testing-log.md`](ab-testing-log.md) | Журнал A/B-тестів (тема листа, оффер, час відправки, форма) з гіпотезою і результатом. |
| [`kpi-benchmarks.md`](kpi-benchmarks.md) | Визначення метрик, орієнтири по галузі, наші цілі, правила "добре/погано". |
| [`troubleshooting.md`](troubleshooting.md) | Технічні проблеми: листи в спамі, не спрацьовує флоу, не синхронізуються замовлення, форма не показується тощо. |

## Як користуватись (робочий процес)

1. **Перший запуск** → йдемо по [`setup-checklist.md`](setup-checklist.md) зверху вниз; паралельно заповнюємо [`account-overview.md`](account-overview.md) і [`deliverability.md`](deliverability.md).
2. **"Налаштуй/перевір автоматизацію"** → [`flows.md`](flows.md) + [`lists-segments.md`](lists-segments.md) + [`content-guidelines.md`](content-guidelines.md).
3. **"Сплануй розсилки на місяць/сезон"** → [`campaigns-calendar.md`](campaigns-calendar.md); після відправки — запис у [`campaign-log.md`](campaign-log.md).
4. **"Проаналізуй, як працює email"** → [`kpi-benchmarks.md`](kpi-benchmarks.md) + дані Klaviyo (можна через Windsor.ai, конектор `klaviyo`) → висновки в [`campaign-log.md`](campaign-log.md) / [`flows.md`](flows.md).
5. **Будь-який тест** → спочатку гіпотеза в [`ab-testing-log.md`](ab-testing-log.md), потім запуск.
6. **Технічна проблема** → [`troubleshooting.md`](troubleshooting.md), новий кейс дописуємо в історію.

## Пріоритет запуску (якщо робимо з нуля)

Email для e-commerce окуповується насамперед **автоматизаціями**, а не разовими розсилками. Порядок запуску:

1. Технічна база: домен відправки + DNS + інтеграція Shopify + onsite tracking
2. Форма підписки (без неї база не росте)
3. Флоу №1 — **Welcome Series**
4. Флоу №2 — **Abandoned Checkout**
5. Флоу №3 — **Browse Abandonment / Added to Cart**
6. Флоу №4 — **Post-Purchase** (подяка + догляд за виробом + відгук)
7. Регулярні кампанії (1–2/тиждень) за [`campaigns-calendar.md`](campaigns-calendar.md)
8. Win-back, Sunset, VIP — коли база й історія замовлень підростуть

Усі файли — живі документи: історію не переписуємо, нові записи додаємо зверху (найновіше — першим).
