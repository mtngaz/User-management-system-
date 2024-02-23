# User Management System

User Management System - это веб-приложение для управления пользователями, разработанное с использованием Spring Framework и JDBC.

## Описание

Этот проект реализует CRUD-операции (create, read, update, delete) для сущности "User" в базе данных с помощью Spring JDBC. В приложении также присутствует сервис UsersService для работы с пользователями и интерфейс UsersRepository, который содержит методы для выполнения основных операций с пользователями, таких как поиск по идентификатору и адресу электронной почты.

## Технологии

- Java
- Spring Core
- Spring JDBC
- JDBC
- PostgreSql

## Структура проекта

- `src`
  - `main`
    - `java`
      - `school21.spring.service`
        - `config`
          - `ApplicationConfig`: Конфигурация приложения.
        - `models`
          - `User`: Модель пользователя.
        - `repositories`
          - `CrudRepository`: Интерфейс, определяющий основные CRUD-операции.
          - `UsersRepository`: Интерфейс, содержащий методы для работы с пользователями.
          - `UsersRepositoryJdbcImpl`: Реализация репозитория с использованием стандартных JDBC-механизмов.
          - `UsersRepositoryJdbcTemplateImpl`: Реализация репозитория с использованием JdbcTemplate.
        - `services`
          - `UsersService`: Интерфейс сервиса для работы с пользователями.
          - `UsersServiceImpl`: Реализация сервиса для работы с пользователями.
        - `application`
          - `Main`: Основной класс, демонстрирующий работу с сервисами пользователей.
    - `resources`
      - `db.properties`: Файл с данными для подключения к базе данных.
  - `test`
    - `java`
      - `school21.spring.service`
        - `config`
          - `TestApplicationConfig`: Тестовая конфигурация приложения.
        - `services`
          - `UsersServiceImplTest`: Тесты для UsersServiceImpl.
    - `pom.xml`: Файл конфигурации Maven.

## Использование

Для запуска приложения необходимо выполнить метод `main` класса `Main`.
