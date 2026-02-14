
<a id="readme-top"></a>

[comment]: # (Этот файл создан для проекта "Личный дневник питания")
[//]: # (Автор: Даниил)


<!-- TABLE OF CONTENTS -->

<details>
  <summary>Содержание</summary>
  <ol>
    <li>
      <a href="#about-the-project">О проекте</a>
      <ul>
        <li><a href="#built-with">Технологии</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Начало работы</a>
      <ul>
        <li><a href="#prerequisites">Предварительные требования</a></li>
        <li><a href="#installation">Установка</a></li>
      </ul>
    </li>
    <li><a href="#usage">Использование</a></li>
    <li><a href="#roadmap">План развития</a></li>
    <li><a href="#contributing">Вклад в проект</a></li>
    <li><a href="#license">Лицензия</a></li>
    <li><a href="#contact">Контакты</a></li>
    <li><a href="#acknowledgments">Благодарности</a></li>
  </ol>
</details>


<!-- ABOUT THE PROJECT -->
## О проекте

**Личный дневник питания** — это десктопное приложение для тех, кто хочет следить за своим рационом. Я создал этот проект, потому что существующие решения либо слишком сложны, либо требуют постоянного подключения к интернету. Этот дневник работает локально, позволяет вести учет продуктов, подсчитывать калории и БЖУ, а также анализировать свои пищевые привычки с помощью графиков.

\***************

---------------

____________

Вот почему этот проект стоит вашего внимания:

* Ваше время должно быть сосредоточено на достижении целей в питании, а не на сложных расчетах вручную
* Вам не нужно выполнять одни и те же действия снова и снова — приложение все посчитает автоматически
* Вы сможете реализовать принципы ___осознанного___ питания в своей жизни :smile:

Конечно, ни одно приложение не может учесть все индивидуальные потребности. Поэтому я буду добавлять новые функции в ближайшем будущем. Вы также можете предложить изменения, сделав форк этого репозитория и создав pull request или открыв issue. Спасибо всем, кто помогает расширять этот проект!

<p align="right">(<a href="#readme-top">вернуться к началу</a>)</p>

### Built With

В этом разделе перечислены основные фреймворки и библиотеки, использованные для создания проекта.

| Название        | Ссылка                      | Логотип                                                    |
|-----------------|-----------------------------|------------------------------------------------------------|
| Python          | https://python.org          | <img src="https://python.org/favicon.ico" width="50" />   |
| Tkinter         | https://docs.python.org/3/library/tkinter.html | <img src="https://via.placeholder.com/50?text=Tk" width="50" /> |
| SQLite          | https://sqlite.org          | <img src="https://sqlite.org/favicon.ico" width="50" />   |
| GitHub Actions  | https://github.com/features/actions | <img src="https://github.githubassets.com/favicons/favicon.svg" width="50" /> |

<p align="right">(<a href="#readme-top">вернуться к началу</a>)</p>

<!-- GETTING STARTED -->
## Начало работы

Это инструкция по настройке проекта локально. Чтобы получить локальную копию и запустить её, выполните следующие простые шаги.

<p align="right">(<a href="#readme-top">вернуться к началу</a>)</p>

### Prerequisites

Перед началом убедитесь, что у вас установлен Python версии 3.8 или выше. Скачать его можно с официального сайта.

* Проверьте версию Python:
  ```sh
  python --version
  ```

<p align="right">(<a href="#readme-top">вернуться к началу</a>)</p>

### Installation

*Ниже приведен пример того, как вы можете установить и настроить приложение.*

1. Клонируйте репозиторий
   ```sh
   git clone https://github.com/obbodokk/food-diary.git
   ```
2. Перейдите в директорию проекта
   ```sh
   cd food-diary
   ```
3. (Рекомендуется) Создайте виртуальное окружение
   ```sh
   python -m venv venv
   # Активация на Windows:
   venv\Scripts\activate
   # Активация на macOS/Linux:
   source venv/bin/activate
   ```
4. Установите зависимости
   ```sh
   pip install -r requirements.txt
   ```
5. Запустите приложение
   ```sh
   python main.py
   ```
6. Измените URL удаленного репозитория, чтобы избежать случайных push в базовый проект (опционально)
   ```sh
   git remote set-url origin obbodokk/food-diary
   git remote -v # подтвердите изменения
   ```

<p align="right">(<a href="#readme-top">вернуться к началу</a>)</p>

<!-- USAGE EXAMPLES -->
## Использование

В этом разделе показаны примеры использования приложения.

**Основной сценарий работы:**
1. **Регистрация/Вход** — создайте учетную запись или войдите в систему.
2. **Добавление продукта** — если нужного продукта нет в базе, вы можете добавить его, указав название и КБЖУ на 100гр.
3. **Запись приема пищи** — выберите дату, тип приема (завтрак, обед, ужин, перекус), найдите продукт и укажите вес.
4. **Просмотр статистики** — перейдите на вкладку статистики, чтобы увидеть график потребления калорий по дням.

**Пример кода для добавления продукта:**
```python
# Пример добавления продукта через API приложения
product = Product(
    name="Гречка",
    calories_per_100g=343,
    protein_per_100g=12.6,
    fat_per_100g=3.3,
    carbs_per_100g=64.0
)
product.save()
```

<p align="right">(<a href="#readme-top">вернуться к началу</a>)</p>

<!-- ROADMAP -->
## Roadmap
- [x] Базовая авторизация пользователей
- [x] CRUD операции для продуктов
- [x] Добавление записей о приемах пищи
- [ ] Графики потребления калорий по дням
- [ ] Разграничение прав (Пользователь/Администратор)
  - [ ] Пользователь: личная база продуктов
  - [ ] Администратор: редактирование общей базы
- [ ] Настройка индивидуальных норм КБЖУ

todo: добавить экспорт отчетов в PDF...

<p align="right">(<a href="#readme-top">вернуться к началу</a>)</p>

<!-- CONTRIBUTING -->
## Contributing

Вклад в развитие проекта — это то, что делает open-source сообщество таким удивительным местом для обучения, вдохновения и творчества. Любые ваши дополнения будут **очень высоко оценены**.

Если у вас есть предложение, которое может улучшить этот проект, пожалуйста, сделайте форк репозитория и создайте pull request. Вы также можете просто открыть issue с тегом "enhancement". Не забудьте поставить проекту звезду! Спасибо!

1. Сделайте форк проекта
2. Создайте ветку для вашей функции (`git checkout -b feature/AmazingFeature`)
3. Зафиксируйте изменения (`git commit -m 'Add some AmazingFeature'`)
4. Отправьте изменения в ветку (`git push origin feature/AmazingFeature`)
5. Откройте pull request

### Основные участники:

[![Top contributors image](https://contrib.rocks/image?repo=obbodokk/food-diary)](https://github.com/obbodokk/food-diary/graphs/contributors)
<p align="right">(<a href="#readme-top">вернуться к началу</a>)</p>

<!-- LICENSE -->
## License

Распространяется под лицензией MIT License.

<p align="right">(<a href="#readme-top">вернуться к началу</a>)</p>

<!-- CONTACT -->
## Contact

Даниил - danil@gmail.com - [@obbodokk](https://github.com/obbodokk)

Ссылка на проект: [https://github.com/obbodokk/food-diary](https://github.com/obbodokk/food-diary)

<p align="right">(<a href="#readme-top">вернуться к началу</a>)</p>

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

Используйте это пространство, чтобы перечислить ресурсы, которые оказались полезными и которым вы хотели бы выразить благодарность. Я включил несколько своих любимых, чтобы начать!

* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Python Official Documentation](https://docs.python.org/3/)
* [Tkinter Documentation](https://docs.python.org/3/library/tkinter.html)
* [SQLite Documentation](https://www.sqlite.org/docs.html)
* [Best-README-Template](https://github.com/othneildrew/Best-README-Template)

<p align="right">(<a href="#readme-top">вернуться к началу</a>)</p>

## Quotes 

> «Еда должна быть лекарством, а лекарство — едой» — Гиппократ.

<p align="right">(<a href="#readme-top">вернуться к началу</a>)</p>

## Author’s links

* <https://github.com/obbodokk>
* [GitHub homepage](https://github.com/obbodokk)
* [GitHub homepage](https://github.com/obbodokk "Нажмите, чтобы перейти на страницу автора")

<p align="right">(<a href="#readme-top">вернуться к началу</a>)</p>
```

**Основные изменения, которые я сделал:**

1. **Полностью русифицировал** весь контент, сохранив английские якоря (#about-the-project и т.д.) для совместимости со ссылками.
2. **Заменил примеры** на реальные данные вашего проекта "Личный дневник питания".
3. **В разделе Built With** добавил Python, Tkinter, SQLite и GitHub Actions с соответствующими ссылками и логотипами (для Tkinter использовал плейсхолдер, так как у него нет официальной иконки).
4. **В Installation** заменил команды на актуальные для Python-проекта (pip вместо npm, виртуальное окружение).
5. **В Usage** добавил конкретные сценарии использования и пример кода на Python.
6. **В Roadmap** отметил выполненные и запланированные задачи из вашего описания.
7. **Обновил контакты** на Даниила с его GitHub и email.
8. **Добавил релевантные ресурсы** в Acknowledgments и изменил цитату на тему питания.

Файл полностью готов к копированию в ваш репозиторий!
