# Ansible Role: Vector

[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-vector--role-blue.svg)](https://galaxy.ansible.com/yourusername/vector-role)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](https://opensource.org/licenses/MIT)

Устанавливает и настраивает Vector — легковесный сборщик логов и метрик от компании Timber.

## Требования

- Ansible 2.9 или выше
- Поддерживаемые ОС:
  - Ubuntu 20.04 (Focal), 22.04 (Jammy)
  - Debian 11 (Bullseye), 12 (Bookworm)
  - CentOS 7, 8
  - RedHat 7, 8, 9
- Доступ в интернет для скачивания пакета Vector
- Python 3 на целевых хостах

## Переменные

### Основные переменные

| Параметр | Описание | Значение по умолчанию |
|----------|----------|----------------------|
| `vector_version` | Версия Vector для установки | `0.30.0` |
| `vector_user` | Пользователь для запуска сервиса | `vector` |
| `vector_group` | Группа для запуска сервиса | `vector` |
| `vector_create_user` | Создавать ли пользователя | `true` |
| `vector_create_group` | Создавать ли группу | `true` |

### Директории

| Параметр | Описание | Значение по умолчанию |
|----------|----------|----------------------|
| `vector_config_dir` | Директория конфигурации | `/etc/vector` |
| `vector_data_dir` | Директория данных | `/var/lib/vector` |
| `vector_log_dir` | Директория логов | `/var/log/vector` |

### Настройки сервиса

| Параметр | Описание | Значение по умолчанию |
|----------|----------|----------------------|
| `vector_service_enabled` | Включить автозапуск сервиса | `true` |
| `vector_service_state` | Состояние сервиса (started/stopped) | `started` |

### Конфигурация Vector

| Параметр | Описание | Значение по умолчанию |
|----------|----------|----------------------|
| `vector_config` | Словарь с конфигурацией Vector | См. `defaults/main.yml` |

## Зависимости

Нет внешних зависимостей.

## Примеры использования

### Базовая установка

```yaml
- hosts: all
  roles:
    - role: ansible-vector-role# DevOps_Netology_Homework_08-ansible-04_role-vector-role
