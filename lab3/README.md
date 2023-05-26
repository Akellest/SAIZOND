# Лабораторная работа №3. Развертывание системы мониторинга ELK Stack (Opensearch)

## Цель работы

1. Освоить базовые подходы централизованного сбора и накопления информации
2. Освоить современные инструменты развертывания контейнирозованных приложений
3. Закрепить знания о современных сетевых протоколах прикладного уровня

## Задание

1. Развернуть систему мониторинга на базе Opensearch
- Opensearch
- Beats (Filebeat, Packetbeat)
- OpenSearch Dashboards
2. Настроить сбор информации о сетевом трафике
3. Настроить сбор информации из файлов журналов (лог-файлов)
4. Оформить отчет в соответствии с шаблоном

## Исходные данные

- Windows 10
- Docker
- WSL2 (Ubuntu 20.04)
- RStudio

## Ход работы

1. Используем последовательность команд:

```
docker pull docker.elastic.co/elasticsearch/elasticsearch:8.8.0
```

```
wsl -d docker-desktop -u root
```

```
sysctl -w vm.max_map_count=262144
```

```
docker run --name es01 --net elastic -p 9200:9200 -it docker.elastic.co/elasticsearch/elasticsearch:8.8.0
```

2. Настраиваем файлы конфигурации: docker-compose.yml, filebeat.yml, packetbit.yml, .env. Все файлы лежат в директории <i>Files</i>, кроме .env

.env:
```
ELASTIC_PASSWORD=username
KIBANA_PASSWORD=username
STACK_VERSION=8.7.0
CLUSTER_NAME=docker-cluster
LICENSE=basic
ES_PORT=9200
KIBANA_PORT=5601
MEM_LIMIT=1073741824
```

3. Запускаем контейнер с использованием настроенных файлов
```
docker-compose up -d
```

4. 
