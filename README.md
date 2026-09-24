# HTTP-сервер с ThreadPool (Refactoring & MultiThreading)

## 📋 Описание задачи

Реализовать HTTP-сервер на Java, который:
- Принимает входящие подключения на заданном порту;
- Обрабатывает каждое подключение в отдельном потоке из **фиксированного пула на 64 потока**;
- Отдаёт статические файлы из папки `public/`;
- Возвращает корректные HTTP-статусы (`200 OK`, `404 Not Found`);
- Поддерживает специальный шаблон `classic.html` с подстановкой текущего времени.

## 🎯 Цель

Отработать:
- Работу с `ServerSocket` и `Socket` на низком уровне;
- Понимание протокола **HTTP/1.1** (структура запроса и ответа);
- Многопоточную обработку подключений через `ExecutorService` с фиксированным пулом;
- Отдачу статических файлов и определение MIME-типов через `Files.probeContentType()`.

## 🛠️ Используемые технологии

- Java 17+
- `ServerSocket` / `Socket`
- `ExecutorService` (`Executors.newFixedThreadPool`)
- `BufferedReader` / `BufferedOutputStream`
- `java.nio.file.Files` / `Path`
- `LocalDateTime` для подстановки времени
- Maven
