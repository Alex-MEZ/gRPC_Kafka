# gRPC Kafka Project

Этот проект демонстрирует использование gRPC для межсервисного взаимодействия и Kafka для обмена сообщениями. Он состоит из двух приложений: `UserServiceApp` и `LibraryServiceApp`.

## Требования

- JDK 17
- Docker и Docker Compose
- Maven

## Установка и запуск

1. **Клонирование репозитория:**
    ```bash
    git clone https://github.com/Alex-MEZ/gRPC_Kafka.git
    cd gRPC_Kafka
    ```

2. **Запуск Kafka и PostgreSQL:**
    ```bash
    docker-compose up -d
    ```

3. **Запуск `UserServiceApp`:**
    ```bash
    cd UserServiceApp
    mvn clean install
    java -jar target/UserServiceApp-0.0.1-SNAPSHOT.jar
    ```

4. **Запуск `LibraryServiceApp`:**
    ```bash
    cd ../LibraryServiceApp
    mvn clean install
    java -jar target/LibraryServiceApp-0.0.1-SNAPSHOT.jar
    ```

## Остановка

### Остановка Java-приложения
- Нажмите `Ctrl + C` в терминале, где запущено приложение.
- Или используйте команды:
  ```bash
  tasklist /FI "IMAGENAME eq java.exe"
  taskkill /PID <pid> /F
  ```

### Остановка Docker-контейнеров
- Остановите все контейнеры:
  ```bash
  docker-compose down
  ```

## Используемые технологии

- Java 17
- Spring Boot
- gRPC
- Kafka
- PostgreSQL
- Docker и Docker Compose
