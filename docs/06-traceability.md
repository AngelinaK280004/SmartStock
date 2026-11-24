

```markdown
# Матрица трассировки

| Требование | Проблема | Процесс (BPMN/ARIS) | Сущность (ER) | Критерий приёмки |
|---|---|---|---|---|
| FR-01 Иерархия склада | №1 | IDEF0 A2 (Хранение) | `warehouses`, `racks`, `shelves` | Настройка структуры |
| FR-02 Приёмка | №2 | A1, ARIS приёмка | `products`, `transactions` | Gherkin: брак / несоответствие |
| FR-03 Остатки онлайн | №3 | A2, A3 | `products` | Gherkin: остаток после отгрузки |
| FR-04 Перемещение | №1 | A2 | `products`, `transactions` | Gherkin: перемещение |
| FR-05 Поиск | №4 | A1–A3 | `products` | Gherkin: поиск по SKU |
| FR-06 Визуализация | №4, №6 | A2 | `shelves`, `products` | Отображение ячейки |
| FR-07 Голосовой поиск | №4 | A1–A3 | `products`, `shelves` | Gherkin: голосовой запрос |
| FR-08 Прогноз | №5 | A2 | `products`, `transactions` | Рекомендация по пополнению |
| FR-09 RBAC | — | Все | `users`, `roles` | Gherkin: 403 для рабочего |
| NFR-DATA-01 | — | — | `products.quantity CHECK` | Ограничение в БД |
