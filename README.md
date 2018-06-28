# Otus HomeWork [Jenkins]


Jenkins
=======

### Список проектов

![Список проектов](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_01.JPG)
[jenkins_projects_list]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_01.JPG


### Проект с использованием отчетов Allure
Данный проект имеет два теста, один из которых нарочно создан "неудачным" для проверки работы TestListener'а(создание отчётов и перехват трафика)

![Проект с использованием отчетов Allure](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_02.JPG)
[jenkins_project_with_allure]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_02.JPG


#### Отображение вывода в консоль при запуске задания в Jenkins

Извлечение, сборка, запуск теста
![Отображение вывода в консоль при запуске задания в Jenkins](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_03_01.JPG)
[jenkins_output_console_2]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_03_01.JPG

Вывод первого теста (успешный тест)
![Отображение вывода в консоль при запуске задания в Jenkins](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_03_02.JPG)
[jenkins_output_console_2]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_03_02.JPG

Вывод второго(неудачного) теста, запуск генерации отчетов Allure
![Отображение вывода в консоль при запуске задания в Jenkins](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_03_03.JPG)
[jenkins_output_console_3]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_03_03.JPG



#### Настройки проекта

Git
![Настройки проекта](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_04_01.JPG)
[jenkins_project_settings_1]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_04_01.JPG

Триггеры сборки, расписание
![Настройки проекта](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_04_02.JPG)
[jenkins_project_settings_2]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_04_02.JPG

Сборка, Maven
![Настройки проекта](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_04_03.JPG)
[jenkins_project_settings_3]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_04_03.JPG

Allure
![Настройки проекта](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_04_04.JPG)
[jenkins_project_settings_4]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_04_04.JPG


#### Настройки инструментов
![Настройки инструментов](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_05.JPG)
[jenkins_tools_settings_1]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_05.JPG

![Настройки инструментов](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_05_02.JPG)
[jenkins_tools_settings_2]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_05_02.JPG

#### Проект с историей

Данный проект при первом запуске имел много проблем:
* В настройках был указан незапущенный Selenium Grid
* Теста запускался c кодировкой отличной от UTF-8
* Была незначительно превышена допустимая разница во времени

После исправления всех проблем все тесты стали успешно проходить, что видно в истории на данном скрине.
![Настройки инструментов](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_06.JPG)
[jenkins_project_with_history]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_06.JPG


Allure
======

#### Панель отчёта Allure
![Панель отчётов Allure](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_01.JPG)
[allure_dashboard]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_01.JPG


#### Упавший тест в отчёте Allure

![Упавший тест в отчёте Allure](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_02.JPG)
[allure_negative_test]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_02.JPG


#### Успешный тест в отчёте Allure

![Успешный тест в отчёте Allure](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_03.JPG)
[allure_positive_test]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_03.JPG


#### Вложения в отчёте Allure

![Вложения в отчёте Allure](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_04.JPG)
[allure_attachments]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_04.JPG


#### Графики

![Графики](https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_05.JPG)
[allure_graphs]: https://raw.githubusercontent.com/MariaOskar/OtusJenkinsHW/master/Jenkins_Allure_05.JPG
