В read side приложения с архитектурой CQRS (объект TypedCalculatorReadSide 
в TypedCalculatorReadAndWriteSide.scala) необходимо разделить чтение событий,
бизнес логику и запись в целевой получатель и сделать их асинхронными, т.е.
1) Persistence Query должно находиться в Source
2) Обновление состояния необходимо переместить в отдельный от записи в БД флоу
3) ! Задание со звездочкой: вместо CalculatorRepository создать Sink c любой БД (например Postgres из docker-compose файла).

Для последнего задания пригодится документация - https://doc.akka.io/docs/alpakka/current/slick.html#using-a-slick-flow-or-sink
Результат выполненного д.з. необходимо оформить либо на github gist либо PR к текущему репозиторию.
