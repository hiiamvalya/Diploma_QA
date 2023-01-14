### Для начала работы
Необходимо загрузить на свой ПК репозиторий с проектом. Для этого либо воспользуйтесь командой git clone и вставьте ссылку https://github.com/hiiamvalya/Diploma_QA в поле URL, нажмите "Clone".

Для запуска тестов на вашем ПК должно быть установлено следующее ПО:

1. IntelliJ IDEA
2. Git
3. Docker Desktop
4. Любой браузер

### Установка и запуск
1. Запускаем контейнеры из файла docker-compose.yml командой в терминале:   
`docker-compose up -d`

2. Запускаем SUT командой в терминале:   
для MySQL:   
`java "-Dspring.datasource.url=jdbc:mysql://localhost:3306/app" -jar artifacts/aqa-shop.jar`   
для PostgreSQL:   
`java "-Dspring.datasource.url=jdbc:postgresql://localhost:5432/app" -jar artifacts/aqa-shop.jar`

3. Запускаем авто-тесты командой в терминале:   
для MySQL:   
`./gradlew clean test "-Ddb.url=jdbc:mysql://localhost:3306/app"`   
для PostgreSQL:   
`./gradlew clean test "-Ddb.url=jdbc:postgresql://localhost:5432/app"`   

Приложение запускается в браузере по адресу: http://localhost:8080/
