# Анализ диаграмм Ганта для Vue

## [Elastic Gantt](https://github.com/neuronetio/gantt-elastic)

**Лицензия:** MIT

**Текущая версия:** 0.13.9 (не стабильная)

**Дата последнего релиза:** отсутствует

**Дата последних изменений:** месяц назад

### Плюсы

* Легко подключается.
* Красивая, интерактивная из коробки.
* Внешний вид формируется в виде описания массива с данными (`tasks`) 
и метаописания структуры (`options`).

### Минусы

* Скудная документация.
* Отсутствует стабильная версия библиотеки (отсутствуют релизы).

### Другие особенности

* Есть три типа задач: "проект" (`project`), "этап" (`milestone`), "задача" (`task`).
Каждый из типов задач отрисовывается своей фигурой.
* Для каждой задачи можно определить свой стиль отображения. Но есть небольшой минус: 
стили описываютя для каждой задачи отдельно в массиве с задачами (`tasks`).



## [vue-easy-gantt](https://github.com/mamboer/vue-easy-gantt)

**Лицензия:** MIT

**Текущая версия:** 1.0.0

**Дата последнего релиза:** 03.04.2017

**Дата последних изменений:** 2 года назад

### Плюсы

На предмет плюсов не рассматривалась

### Минусы

* Не сопровождается
* Не красивая
* Документация практически отсутствует



## [Frappe Gantt](https://github.com/FonteSolutions/gantt)

**Лицензия:** MIT

**Текущая версия:** 0.3.0 (не стабильная)

**Дата последнего релиза:** отсутствует

**Дата последних изменений:** 16.02.2019

### Плюсы

* Поддерживает зависимости между задачами


### Минусы

* Очень лаконичный внешний вид.
* 
* 

### Другие особенности

* Является не Vue-компонентом, а чистой JS-библиотекой. Для использования во Vue
приходится оборачивать в компонент.