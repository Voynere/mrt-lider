# МРТ Лидер

Сеть медицинских центров МРТ и диагностики: мультгородской WordPress-сайт, внутренняя панель мониторинга гелия и инструменты рекламной автоматизации.

**Сайты:**

| Домен | Назначение |
|-------|------------|
| [mrt-lider.ru](https://mrt-lider.ru) | Основной сайт — **30+ городов** в России |
| [mrt-lider.kz](https://mrt-lider.kz) | Казахстан (Алматы, Астана и др.) |
| [helium.mrt-lider.ru](https://helium.mrt-lider.ru) | Helium Monitor — уровень гелия в МРТ-магнитах |

## Что это

Продакшен-монорепозиторий сети МРТ Лидер:

- Кастомная тема WordPress `MRT Lider` — услуги, цены, специалисты, блог, посадочные по городам
- Мультгородская маршрутизация `/{city}/`, SEO (canonical, JSON-LD, sitemap), формы записи и sticky CTA
- **Helium Monitor** — учёт гелия, заправки, алерты, роли admin/manager/engineer, экспорт Excel/PDF, QR магнитов
- Боты полевого ввода: Telegram / MAX / Express
- CLI и CI для Яндекс Директа: аудит объявлений, массовое исправление ссылок, stop-list

## Стек

| Слой | Выбор |
|------|--------|
| Публичный сайт | WordPress, PHP 8.5, Redis Object Cache, Nginx/Apache |
| Тема | ACF, CPT (услуги, статьи, специалисты), multi-city routing |
| Helium Monitor | PHP 8.5+, PostgreSQL 17, Chart.js, Tailwind CSS |
| Реклама | Яндекс Директ API v5 |
| Ops | CI deploy + smoke, systemd-боты |

## Архитектура (обзор)

```
публичный сайт (WP) ──► города / услуги / SEO / конверсия
        │
Helium Monitor ────────► PostgreSQL, CSV/XLSX импорт, алерты, мессенджеры
        │
Yandex Direct tools ───► аудит и правка кампаний RU/KZ
```

## Роль

Разработка, SEO и DevOps: тема, Helium, интеграции мессенджеров, рекламная автоматизация и CI/CD.

## Portfolio note

Этот GitHub-репозиторий — **публичная витрина** продукта. Исходный код, деплой-пайплайн и внутренняя документация живут в **приватном** Gitea-репозитории и сюда не публикуются.

Сделано в [Lighttread](https://lighttread.ru) / Voynere.

## Ссылки

- Сайт: https://mrt-lider.ru
- Helium: https://helium.mrt-lider.ru
- KZ: https://mrt-lider.kz
- Студия: https://lighttread.ru
