# Лабораторная работа №2. Сбор и аналитическая обработка информации о сетевом трафике

## Цель

- Развить практические навыки использования современного стека инструментов сбора и аналитической обработки информации о сетвом трафике
- Освоить базовые подходы блокировки нежелательного сетевого трафика
- Закрепить знания о современных сетевых протоколах прикладного уровня

## Исходные данные

Windows 10
Docker для Zeek
Google Colab для Python
RStudio

## План

1. Собрать сетевой трафик с помощью WireShark
2. Проанализировать трафик с помощью Zeek
3. Найти информацию о нежелательном трафике
4. Проверить соотношение допустимого и недопустимого трафика

## Ход работы

1. Был собран трафик с помощью WireShark

(Файл: traffic.pcap)

2. Была получена информация о собранном трафике путем использования команды в Docker

```
zeek -C -r traffic.pcap
```

3. Были найдены несколько файлов и соединены в один списки hosts

Источник: https://github.com/StevenBlack/hosts

4. С помощью программы на Python был отфильтрован файл dns.log в читаемый вид (Рисунок 1) с использованием кода:

![](/images/logs.png)

Рисунок 1 - Сравнение версий файлов

5. Был найден процент нежелательного трафика путем сравнения строк файлов dns.log и hosts.txt (Рисунок 2)

```
dns_file = open('dns1.txt', 'r')
hosts_file = open('hosts.txt', 'r')

dns_lines = dns_file.readlines()
dns_list = []
for line in dns_lines:
    line = line.strip()
    if line and line != "-":
        dns_list.append(line)

hosts_lines = hosts_file.readlines()
hosts_list = []
for line in hosts_lines:
    line = line.strip()
    if line and line != "-" and line != "#":
        hosts_list.append(line)


percentage = round(len(set(dns_list).intersection(set(hosts_list))) / len(dns_list) * 100, 2)
print("Процент нежелательного трафика: " + str(percentage) + "%")

dns_file.close()
hosts_file.close()
```

![](/images/result.png)

Рисунок 2 - Результат программы

## Вывод

Поставленная задача была выполнена с использованием инструмента Zeek, Docker и Python. В процессе решения задачи был приобрел опыт работы с инструментами для сбора информации о сетевом трафике и аналитической обработки этих данных.
