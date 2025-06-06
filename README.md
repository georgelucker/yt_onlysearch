# 🎯 yt_onlysearch – минимализм для YouTube

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
| Firefox | [Установить](https://addons.mozilla.org/firefox/addon/styl-us/) |
| Chrome / Chromium / Яндекс.Браузер | [Установить](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne) |

---

### 2. Установите стиль

#### Способ 1: Импорт из файла

1. Скачайте файл `style.user.css` из этого репозитория.
2. Нажмите на значок **Stylus** в браузере → **Manage** (или «Управление»).
3. Нажмите **Import** (Импорт).
4. Выберите загруженный файл `style.user.css` и нажмите **OK**.

#### Способ 2: Вставка вручную

1. Перейдите на [https://www.youtube.com/](https://www.youtube.com/)
2. Нажмите на иконку **Stylus** → **Manage** (или «Управление»)
3. Нажмите **Write new style** (или «Создать новый стиль»)
4. Вставьте следующий код в поле редактора:

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
