# Otus HomeWork [Jenkins]


Jenkins
=======

### Список проектов

![Список проектов](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_01.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_01.JPG>


### Проект с использованием отчетов Allure
Данный проект имеет два теста, один из которых нарочно создан "неудачным" для проверки работы TestListener'а(создание отчётов и перехват трафика)

![Проект с использованием отчетов Allure](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_02.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_02.JPG>


#### Отображение вывода в консоль при запуске задания в Jenkins

Извлечение, сборка, запуск теста
![Отображение вывода в консоль при запуске задания в Jenkins](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_03_01.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_03_01.JPG>

Вывод первого теста (успешный тест)
![Отображение вывода в консоль при запуске задания в Jenkins](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_03_02.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_03_02.JPG>

Вывод второго(неудачного) теста, запуск генерации отчетов Allure
![Отображение вывода в консоль при запуске задания в Jenkins](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_03_03.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_03_03.JPG>



#### Настройки проекта

Git
![Настройки проекта](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_04_01.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_04_01.JPG>

Триггеры сборки, расписание
![Настройки проекта](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_04_02.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_04_02.JPG>

Сборка, Maven
![Настройки проекта](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_04_03.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_04_03.JPG>

Allure
![Настройки проекта](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_04_04.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_04_04.JPG>


#### Настройки инструментов
![Настройки инструментов](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_05.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_05.JPG>

![Настройки инструментов](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_05_02.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_05_02.JPG>

#### Проект с историей

Данный проект при первом запуске имел много проблем:
* В настройках был указан незапущенный Selenium Grid
* Теста запускался c кодировкой отличной от UTF-8
* Была незначительно превышена допустимая разница во времени

После исправления всех проблем все тесты стали успешно проходить, что видно в истории на данном скрине.
![Настройки инструментов](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_06.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_06.JPG>


Allure
======

#### Панель отчёта Allure
![Панель отчётов Allure](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_01.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_01.JPG>


#### Упавший тест в отчёте Allure
Пример "упавшего" теста.<br/>
В отчёт добавлены файл с перехваченным трафиком и скриншот, созданный при падении теста.<br/>
Из отчёта видно, что мы ожидаем увидеть в пункте отправки Бостон, а видим - Мехико, что полностью соответствует коду данного теста:
<https://github.com/MariaOskar/OtusJDI/blob/master/src/test/java/com/blazedemo/test/JDITest.java#L66>
```Java
    @Test
    public void negativeTest(){
        choicePage.open();
        choicePage
                .selectFrom(DepartureEnum.BOSTON.city())
                .selectTo(DestinationEnum.BUENOS_AIRES.city())
                .submit();
        reservePage
                .checkOpenedPage()
                .checkFromPortValue(DepartureEnum.MEXICO_CITY.city())
                .checkToPortValue(DestinationEnum.BERLIN.city())
        ;
    }
```


![Упавший тест в отчёте Allure](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_02.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_02.JPG>


#### Успешный тест в отчёте Allure
Пример успешно прошедшего теста.<br/>
Справа мы видим описание теста, указанное при интеграции Allure, описание шагов и инициализации теста.<br/>
Также в отчёте имеются конкретные значения, которые передавались в методы при запуске данного теста.<br/>
Детально интеграцию отчётов Allure в данный проект можно посмотреть в коммите по ссылке: <https://github.com/MariaOskar/OtusJDI/commit/adabcd5103d9c89c83a291860934951825446ad8>
![Успешный тест в отчёте Allure](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_03.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_03.JPG>


#### Вложения в отчёте Allure
Здесь продемонстрировано наличие добавленных в отчёт вложений (скриншоты и трафик)
![Вложения в отчёте Allure](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_04.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_04.JPG>


#### Графики

![Графики](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_05.JPG)
<https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_05.JPG>
