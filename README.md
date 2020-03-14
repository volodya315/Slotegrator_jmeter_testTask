# Тестовое задание

Необходимо реализовать при помощи JMeter следующий тест-план для нагрузочного
тестирования. Ответы должны валидироваться по коду ответа (200 или 201). По итогам
тестирования должен быть сформирован csv-файл. 


| Запрос | Распределение нагрузки, % |
| --- | --- |
| Получение гостевого токена| однократно для каждого потока |
| Регистрация игрока | однократно для каждого потока |
| Авторизация под игроком | однократно для каждого потока |
| Запрос профиля игрока | 10 |
| Запрос списка игр игроком | 40 |
| Запрос списка игр игроком с сортировкой | 40 |
| Запрос одной игры игроком по id | 10 |

# Результаты выполнения
По результатам тестирования было выяснено, что при нагрузке в 160 7,34% запросов возвращают ошибки, при увеличении количества пользователей процент ошибок выше. При уменьшении нагрузки до 155 пользователей уже всё стабильно. Так же были сформированы 2 отчета в формате csv, которые находятся в этом же репозитории.

Для запуска тест-плана требуется создать в корне диска C папку Jmeter test results а в ней два файла: aggregate_report.csv и results_table.csv. Или же переназначить файлы вручную для listener'ов.
Также все запрос одной игры игроком по id возвращают код 404, так как вместо списка игр на тестируемом сервере пустой массив.
C:\Jmeter test results
C:\Jmeter test results\aggregate_report.csv
C:\Jmeter test results\results_table.csv
