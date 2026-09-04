# ERD — Цифровой онбординг

## Что это
Диаграмма сущность-связь (ERD) для 4 таблиц, лежащих в основе SQL-кейсов в [`06-sql-portfolio`](../06-sql-portfolio).

## Структура
- **users** — клиенты (id, name, email, phone_number, birth_date, created_at)
- **applications** — заявки на онбординг (channel, verification_method, status, risk_score, created_at, completed_at), FK на users
- **verification_checks** — отдельные проверки внутри заявки (check_type, status, attempt_number), FK на applications
- **products** — выданные продукты (product_type, product_name, issued_at), FK на applications

Связи: один клиент может подать несколько заявок; одна заявка проходит несколько проверок и может завершиться выдачей продукта.

## Инструменты
draw.io

## Файл
[`erd-diagram.jpg`](./erd-diagram.jpg)
