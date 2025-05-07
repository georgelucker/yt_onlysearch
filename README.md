# 🎯 YouTube Clean View – минимализм для YouTube

Этот пользовательский стиль **очищает главную страницу YouTube**, оставляя только строку поиска, и **скрывает комментарии под видео**. Подходит для тех, кто хочет избавиться от отвлекающего контента и сосредоточиться на поиске нужного видео.

---

## 📦 Что делает этот стиль?

- Удаляет рекомендации и ленту с главной страницы.
- Скрывает боковую панель навигации.
- Скрывает комментарии под видео.
- Центрирует строку поиска.

---

## 🛠 Установка

### 1. Установите расширение Stylus

| Браузер | Ссылка |
|--------|--------|
| Chrome / Chromium / Яндекс.Браузер | [Установить](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne) |
| Firefox | [Установить](https://addons.mozilla.org/firefox/addon/styl-us/) |
| Opera | [Установить](https://addons.opera.com/extensions/details/stylus/) |

---

### 2. Установите стиль

#### Способ 1: Импорт из файла

1. Скачайте файл `youtube-clean.user.css` из этого репозитория.
2. Нажмите на значок Stylus в браузере → «Управление».
3. Нажмите «Импорт» и выберите файл `youtube-clean.user.css`.

#### Способ 2: Вставка вручную

1. Перейдите на [https://www.youtube.com/](https://www.youtube.com/)
2. Нажмите на иконку Stylus → «Создать стиль».
3. Вставьте следующий код:

```css
/* Скрывает весь контент на главной странице, кроме строки поиска */
ytd-browse:not([page-subtype="search"]) #contents,
ytd-rich-grid-renderer,
ytd-mini-guide-renderer,
ytd-guide-renderer,
ytd-masthead #end,
#chips-wrapper,
#secondary,
ytd-merch-shelf-renderer,
ytd-rich-section-renderer {
    display: none !important;
}

/* Скрывает комментарии под видео */
ytd-comments {
    display: none !important;
}

/* Центрирование строки поиска */
#center {
    margin: auto !important;
}
