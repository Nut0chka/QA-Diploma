# Дипломный проект по профессии «Тестировщик»
## Документация
1. [План тестирования](https://github.com/Nut0chka/QA-Diploma/blob/main/docs/Plan.md)
2. [Отчёт по итогам тестирования](https://github.com/Nut0chka/QA-Diploma/blob/main/docs/Report.md)
3. [Отчет по итогам автоматизации](https://github.com/Nut0chka/QA-Diploma/blob/main/docs/Summary.md)

## О проекте
Дипломный проект — автоматизация тестирования комплексного сервиса, взаимодействующего с СУБД и API Банка.

Приложение — это веб-сервис, который предлагает купить тур по определённой цене двумя способами:
1. Обычная оплата по дебетовой карте.
2. Уникальная технология: выдача кредита по данным банковской карты.
![service.png](docs%2Fpic%2Fservice.png)

## Цели
В рамках проекта необходимо автоматизировать тестирование комплексного сервиса покупки тура, взаимодействующего с СУБД и API Банка.
## Инструкция по запуску тестов:
1. Запустить "IntelliJ IDEA";
2. Запустить "Docker Desktop";
3. Скопировать с "Github" [репозиторий](https://github.com/Nut0chka/QA-Diploma).
4. Открыть проект в "IntelliJ IDEA".
5. В терминале "IntelliJ IDEA" запустить контейнеры `docker-compose up`
## Запуск тестового приложения:
### MySQL:
1. В новой вкладке терминала ввести `java -jar ./artifacts/aqa-shop.jar -P:jdbc.url=jdbc:mysgl://localhost:3306/app`
2. Проверить доступность приложения в браузере по адресу - http://localhost:8080/
3. Для запуска тестов нужно ввести в новом терминале `./gradlew clean test "-Ddb.url=jdbc:mysql://localhost:3306/app"`
4. Создать отчёт Allure и открыть в браузере `.\gradlew allureServe`
### PostgresQL:
1. В новой вкладке терминала ввести `java -jar ./artifacts/aqa-shop.jar -P:jdbc.url=jdbc:postgresql://localhost:5432/app `
2. Проверить доступность приложения в браузере по адресу - http://localhost:8080/
3. Для запуска тестов нужно ввести в новом терминале `./gradlew clean test "-Ddb.url=jdbc:postgresql://localhost:5432/app"`
4. Создать отчёт Allure и открыть в браузере `.\gradlew allureServe`