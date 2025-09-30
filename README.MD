# Monorepo: manager

Структура репозитория для микросервисов и фронтендов (без реализации функционала).

## Директории

- services/
  - api-gateway/ — шлюз API и единая точка входа для фронтов
  - wb-parser/ — парсинг данных Wildberries, запись в БД
  - telegram-bot/ — отправка данных и новостей в Telegram
  - news-parser/ — парсинг новостей из Telegram
  - admin-backend/ — бэкенд для CRUD-операций в админке
  - common/ — общие библиотеки/клиенты/схемы
- apps/
  - web-client/ — публичный фронтенд
  - admin-panel/ — админ-панель
- infra/
  - docker/ — Dockerfile’ы, docker-compose
  - kubernetes/ — манифесты и helm-чарты
  - ci-cd/ — конфигурации CI/CD
- database/
  - migrations/ — миграции БД
  - seeds/ — сиды данных
- libs/
  - utils/ — утилиты
  - models/ — общие модели/DTO/ORM
- docs/ — документация
- scripts/ — служебные скрипты

## Дальнейшие шаги (предложение)

- Определить стек (например: Node.js/NestJS + PostgreSQL + Redis; фронт — Next.js)
- Вести общие контракты (OpenAPI/AsyncAPI) в `services/common`
- Настроить docker-compose для локальной разработки в `infra/docker`
- Описать CI (линт, тесты, сборки, контейнеризация) в `infra/ci-cd`
- Подготовить схемы БД и миграции в `database`

