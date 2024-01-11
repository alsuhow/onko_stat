## Интенсив Антона Ермолина по работе с файлами
# Состояние онкопомощи в России (2021 год)

Достаточно частая задача практически в любой фирме — это работа с множеством однотипных файлов (например, периодических отчетов), из которых надо сделать сводную информацию для руководства: отчет или дашборд. Если такого рода задача носит постоянный характер, то есть смысл этот процесс автоматизировать: сделать универсальный обработчик, который будет обрабатывать файлы без участия человека и сохранять обработанный результат в том или ином виде: обработанная таблица или дашборд.

Первоисточник всех данных - Отчет (ежегодный) главного онколога Министерства Здравоохранения России академика Каприна А. Д.


Вот этот отчет в двух файлах

- [Состояние онко помощи в РФ](https://drive.google.com/file/d/1x6wjJ2k8ZNCaIFusbcH6Zkt8a8xOdxhW/view?usp=drive_link)
- [Злокачественные новообразования в РФ (заболеваемость и смертность)](https://drive.google.com/file/d/19sN2INNs4Pz9HfwTDkhVYdXlWR49RcS-/view?usp=drive_link)

  ## **Загрузка и обработка данных**

[ipynb](https://github.com/alsuhow/onko_stat/blob/main/Project%20Onko-GH.ipynb)   [HTML](https://github.com/alsuhow/onko_stat/blob/main/Project%20Onko-GH.html)
- Загрузить данные:
    - Подключиться к Яндекс диску;
    - Создать список файлов для загрузки через списочное выражение: использование os.chdir(), os.listdir(), str.endswith();
    - Определить количество типов таблиц в файлах (2-3 типа в каждой группе было);
    - Определить методы извлечения необходимых данных;
    - Написать обработчик (1-2) в зависимости от навыков и здравого смысла для загрузки файлов (попробовать по максимуму решить все проблемы в обработчике);
    - использование библиотеки tqdm для отслеживания прогресса выполнения обработки (для пижонства - красиво выглядит когда работает);
    - Получить на выходе список датасетов;
    - Проверить корректность загрузки;
    - Слить датасеты в один;
    - Дообработать данные (при необходимости): колонки, типы данных, пробелы и прочие недочеты


- добавил колонки с координатами регионов. Отдельно вынес название ФО
- обработал сводные файлы
- добавил выгрузку на Яндекс.Диск
- добавил в репозитарий архив фалов с первичной информацией
