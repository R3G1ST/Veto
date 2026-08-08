<p align="center">
  <img src="https://img.shields.io/badge/status-development-yellow?style=for-the-badge" alt="Status: Development"/>
  <img src="https://img.shields.io/badge/version-1.0.0-blue?style=for-the-badge" alt="Version"/>
  <img src="https://img.shields.io/badge/license-MIT-green?style=for-the-badge" alt="License"/>
  <img src="https://img.shields.io/badge/windows-10%2F11-purple?style=for-the-badge" alt="Windows"/>
</p>

<h1 align="center">Veto</h1>

<p align="center">
  <b>DPI Bypass Engine</b><br>
  Лёгкий движок для обхода DPI (Deep Packet Inspection)<br>
  Альтернатива zapret / nfqws
</p>

---

> **⚠️ Статус: В разработке**<br>
> Проект находится на ранней стадии разработки. API и функциональность могут измениться.

## Что это?

Veto — это самописный движок для обхода DPI, разработанный как более лёгкая и быстрая альтеритива [zapret](https://github.com/Flowseal/zapret-discord-youtube). Движок использует WinDivert для перехвата пакетов и применяет различные техники обхода.

## Возможности

- **Fake пакеты** — подмена TTL для обмана DPI
- **Split пакетов** — разделение TCP-сегментов
- **Disorder** — нарушение порядка TCP-сегментов
- **Hostlists** — маршрутизация по спискам доменов
- **Конфигурация** — TOML конфигурация с профилями
- **WinDivert** — перехват пакетов на уровне ядра

## Сборка

```bash
# Требуется CMake 3.10+ и GCC/MinGW
build.bat
```

## Структура

```
veto/
├── include/           # Заголовочные файлы
├── src/
│   ├── core/          # Основной движок
│   ├── protocols/     # Парсинг протоколов
│   ├── attacks/       # Модули атак
│   ├── capture/       # Перехват через WinDivert
│   └── config/        # Конфигурация
├── lib/               # WinDivert библиотеки
├── files/             # Hostlist файлы
├── strategies/        # Стратегии обхода
└── veto.conf          # Конфигурация
```

## Лицензия

MIT License — свободное использование и модификация

## Автор

[R3G1ST](https://github.com/R3G1ST)
