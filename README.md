#  Как работать с репозиторием финального задания

## Что нужно сделать

Настроить запуск проекта Kittygram в контейнерах и CI/CD с помощью GitHub Actions

## Как проверить работу с помощью автотестов

В корне репозитория создайте файл tests.yml со следующим содержимым:
```yaml
repo_owner: ваш_логин_на_гитхабе
kittygram_domain: полная ссылка (https://доменное_имя) на ваш проект Kittygram
taski_domain: полная ссылка (https://доменное_имя) на ваш проект Taski
dockerhub_username: ваш_логин_на_докерхабе
```

Скопируйте содержимое файла `.github/workflows/main.yml` в файл `kittygram_workflow.yml` в корневой директории проекта.

Для локального запуска тестов создайте виртуальное окружение, установите в него зависимости из backend/requirements.txt и запустите в корневой директории проекта `pytest`.

## Чек-лист для проверки перед отправкой задания

- Проект Taski доступен по доменному имени, указанному в `tests.yml`.
- Проект Kittygram доступен по доменному имени, указанному в `tests.yml`.
- Пуш в ветку main запускает тестирование и деплой Kittygram, а после успешного деплоя вам приходит сообщение в телеграм.
- В корне проекта есть файл `kittygram_workflow.yml`.

![example workflow](https://github.com/VanZep/kittygram_final/actions/workflows/Run%20deploy/main.yml/badge.svg)

![example workflow](https://github.com/VanZep/kittygram_final/actions/workflows/%20deploy/badge.svg)

![Build Status](https://travis-ci.org/xdan/jodit.svg?branch=master)(https://travis-ci.org/xdan/jodit)

![Build Status](https://github.com/xdan/jodit/workflows/Run%20tests/badge.svg)(https://github.com/xdan/jodit/actions/workflows/tests.yml)
