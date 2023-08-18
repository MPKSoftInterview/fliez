# Житие мух

_Жили-были мухи. Как вдруг... начали дохнуть._

## Задача

Разработать приложение, моделирующее поведение мух в замкнутом пространстве.

### Настройки, доступные пользователю

* `M` - размер поля в клетках (квадрат `M x M`).
* `N` - максимальное количество мух помещающееся в одной клетке (мухоёмкость).
* `T` - степень врождённой тупости мух.
* Начальное расположение мух в клетках (должна быть возможность задания вручную).

### Алгоритм полёта мухи

1. Муха появляется на поле в произвольной клетке с учетом мухоёмкости.
2. Затем муха выбирает соседнюю клетку в которую она полетит. Время принятия решения определяется врождённой тупостью и не должно превышать `T`.
3. Если в выбранной клетке превышена мухоёмкость, то муха остается в своей клетке, и опять тупит, выбирая куда полететь.
4. Если в выбранной клетке мухоёмкость не превышена, то муха мгновенно оказывается в заданной клетке.
5. Если возраст превышает `T*M` - то муха дохнет, и остаётся в последней занимаемой клетке навсегда.

### Обязательные условия

* Мухи должны летать асинхронно (т.е. каждая муха летает в своем потоке).
* По каждой мухе собирается полётная информация: скорость, пробег и возраст.
* Необходимо помечать мёртвых мух, чтобы можно было различать их на поле.
* После нажатия кнопки "Стоп" должна выводиться статистика по каждой мухе: средняя скорость и пробег, сдохла или жива.
* Муха должна быть иконкой.

### Дополнительные условия

* Анимация перемещения мух - приветствуется.
* Подкрашивать иконку в зависимости от степени тупости мухи.
* Возможность динамически изменять параметры поля (размер и/или мухоёмкость).
* Индивидуальные прикольные иконки мух - приветствуются.
* Любые усовершенствования делающие поведение мух более жизненным - приветствуется.

### Средства разработки

* Ядро программы: C++, желательно стандарта 17 и выше.
* GUI программы: QML.
* Система сборки: CMake.
