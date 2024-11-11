# Java-Zoo
Java application for showing how Spring dependencies works.

## Описание
Простое Java приложение для демостарции работы с Spring зависимостями.

## Сборка и запуск

### Требования
- Java 17 (или выше)
- Maven 3.6.0 (или выше)
- 
### Сборка
Чтобы собрать приложение, необходимо выполнить слейдующие действия:
1. Склонируйте репозиторий.
2. Откройте папку с проектом.
3. Откройте консоль в этой папке и введите команду:
```cmd
mvn clean package
```

### Запуск
### Запуск
После выполнения команды откройте папку *target* и выполните команду:
```cmd
java -jar Java-Zoo-1.0-SNAPSHOT.jar
```

## Документация

### Задачи
Необходимо создать приложение, в котором будут объявлены Spring-конфигурации при помощи xml-конструкций; В каждом варианте есть сущность (класс), 
необходимо создать интерфейс (самостоятельно на усмотрение студента) и классы, его имплементирующие;
Объекты классов, имплементирующих данный интерфейс, будут передаваться в качестве зависимостей;
Выполнить связывание и получить объекты из контекста. Продемонстрировать результаты в простейшем консольном приложении.

#### Должно содержать:

1. Внедрение простых значений через конструктор;
2. Внедрение зависимости по ссылке через конструктор;
3. Интерфейс содержит методы;
4. Классы, имплементирующие интерфейс, сожержат как минимум одно поле (у разных классов - разные);
5. Зависимый класс должен содержит метод, который на основе вызова метода у зависимости выводил бы некоторое сообщение в консоль (Например для класса Автомобиля, в который внедряются Двигатели. Они могут выдавать свою мощность, а автомобиль может выводить сообщение, с какой скоростью он может двигаться);
6. Внедрение простых значений из внешнего файла через setter.

### Реализовано
 
#### Описание классов
- **Interface Animal:** Интерфейс, от которого наследуются все классы животных, имеет два метода (<i>animalSound(), getInfo()</i>).
- **Class Elephant:** Класс слона, который имплементирует интерфейс **Animal**. Имеет **уникальное поле:** weight.  
- **Class Lion:** Класс льва, который имплементирует интерфейс **Animal**. Имеет **уникальное поле:** speed.
- **Class ZooKeeper:** Класс отвечает за взаимодействие с животными, получает животное в качестве зависимости и вызывает методы для вывода информации и звуков животных.
- **Class Main:** Главный класс, который демонстрирует работу программы.

### Описание ресурсов
- **zoo-config.xml:** XML-файл конфигурации Spring, который используется для определения и связывания бинов (объектов) приложения.
- **zoo-prop.properties:** файл свойств, используемый для хранения простых значений конфигурации в формате ключ = значение.