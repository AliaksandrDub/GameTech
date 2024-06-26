# Отчёт по проекту автоматизации инфраструктуры

Автоматизация развертывания стека технологий с использованием Bash, Ansible и контейнерных технологий Docker и Podman. Задачи включали полную настройку серверной инфраструктуры и CMS для обеспечения гибкости, масштабируемости и удобства управления.

## Задача 1: Развертывание стека с использованием Bash

Bash скрипт для настройки следующих компонентов:

- Apache2 и Nginx как основные веб-серверы.
- MySQL/MariaDB как системы управления базами данных.
- PHP как серверный язык программирования.
- WordPress и Joomla как CMS для основного сайта и субдомена.

В директории Task_1.0 находятся файлы конфигурации, которые играют ключевую роль в настройке и управлении вашими приложениями или системами.

[Bash скрипт](https://github.com/AliaksandrDub/GameTech/blob/main/Task_1.0/Bashskript)

## Задача 2: Миграция на Ansible

Миграция с Bash скриптов на Ansible, что позволило:

- Упростить управление конфигурацией.
- Обеспечить идемпотентность операций.
- Динамично управлять компонентами стека, например, заменять компоненты баз данных.

[Ansible Playbook](https://github.com/AliaksandrDub/GameTech/blob/main/Task_2.0/one.yaml)

В директории Task_2.0 находятся файлы конфигурации, которые играют ключевую роль в настройке и управлении вашими приложениями или системами.

## Задача 3: Контейнеризация с Docker и Podman

Контейнеризацию стека для улучшения портативности и управляемости:

- Контейнеризация каждого сервиса для изоляции зависимостей.
- Docker Compose для оркестрации много-контейнерных приложений.
- Перенос на Podman для использования в средах, где требуется работа без демона Docker.

[Docker Compose](https://github.com/AliaksandrDub/GameTech/blob/main/Task_3.0/docker-compose.yml)

В директории Task_3.0 находятся файлы конфигурации, которые играют ключевую роль в настройке и управлении вашими приложениями или системами.

### Команды 
```
sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt update
sudo apt install docker-ce

sudo curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose

cd path_to_your_compose_file
docker-compose up --build
```

### Комментарий

1. Альтернативный инструмент: Kubernetes. Kubernetes предоставляет более продвинутые возможности управления контейнерами, включая автоматическое масштабирование, самовосстановление и балансировку нагрузки.
2. Оптимизация: Использование облачных сервисов управления контейнерами, таких как Amazon ECS или Azure Container Instances, может существенно упростить развертывание и управление, минимизировать затраты на поддержку инфраструктуры и ускорить масштабирование.
