# ZDev
Инструмент обмена данными между серверами Cache' , через прямое Socket соединение
1) Реализован запуск команд на дулаенном компьютере и получение результата в виде строки
2) Запуск класс-метода с локального БД на удаленной.
3) Получение объекта с удаленной БД
4) Выполтить SQL pапрос на удаленной БД
5) Копировать глобал с удаленной БД(UTF8 to UNICODE)
6) Клпировать класс с удаленной БД на Локальную (в разработке...)
7) Копировать бинарный файл с локального компьютера на удаленный через Cache'

Запуск сервера:
<pre> d ##class(%ZDev.Server).Start(6000) </pre>
Остановка сервера
<pre> d ##class(%ZDev.Server).Stop(6000) </pre>
