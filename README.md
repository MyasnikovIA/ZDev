# ZDev
Инструмент обмена данными между серверами Cache' , через прямое Socket соединение
1) Реализован запуск команд на удалённом компьютере и получение результата в виде строки
2) Запуск класс-метода с локального БД на удаленной.
3) Получение объекта с удаленной БД
4) Воплотить SQL запрос на удаленной БД
5) Копировать глобал с удаленной БД(UTF8 to UNICODE)
6) Копировать класс с удаленной БД на Локальную (в разработке...)
7) Копировать бинарный файл с локального компьютера на удаленный через Cache'

Запуск сервера:
<pre> d ##class(%ZDev.Server).Start(6030) </pre>
Остановка сервера
<pre> d ##class(%ZDev.Server).Stop(6030) </pre>

Пример использования находится в пакете %ZDev.Demo (%ZDev.XML)

<h3>Копировать глобал с удаленной БД(UTF8 to UNICODE)</h3>
 <pre>
   s ConnectObject=##class(%ZDev.Client).%New()
   if ConnectObject.Connect("SrcServer1234",6030,"_SYSTEM","SYS","USER",.Error)=1 {
      d ConnectObject.ImportGlobal( "^Refs.AllBazeD", .Error ,1)
   } else{
      zw Error	
   }
   d ConnectObject.DisConnect()
   s ConnectObject=""
  </pre>
