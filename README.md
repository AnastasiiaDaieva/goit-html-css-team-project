# parcel-project-template

## Зависимости

На компьютере должена быть установлена LTS-версия [Node.js](https://nodejs.org/en/).

## Перед началом работы

Один раз на проект установить все зависимости.

```shell
npm ci
```

### Разработка

Запустить режим разработки.

```shell
npm run dev
```

Во вкладке браузера перейти по адресу [http://localhost:1234](http://localhost:1234).

### Деплой

Сборка будет автоматически собирать и деплоить продакшен версию проекта на GitHub Pages, в ветку
`gh-pages`, каждый раз когда обновляется ветка `main`. Например, после прямого пуша или принятого
пул-реквеста. Для этого необходимо в файле `package.json` отредактировать поле `homepage` и скрипт
`build`, заменив `имя_пользователя` и `имя_репозитория` на свои.

```json
"homepage": "https://имя_пользователя.github.io/имя_репозитория",
"scripts": {
  "build": "parcel build src/*.html --public-url /имя_репозитория/"
},
```

Через какое-то время живую страницу можно будет посмотреть по адресу указанному в отредактированном
свойстве `homepage`, например
[https://goitacademy.github.io/parcel-project-template](https://goitacademy.github.io/parcel-project-template).

## Файлы и папки

- Все паршалы файлов стилей должны лежать в папке `src/sass` и импортироваться в
  `src/sass/main.scss`
- Изображения добавляйте в папку `src/images`, заранее оптимизировав их. Сборщик просто копирует
  используемые изображения чтобы не нагружать систему оптимизацией картинок, так как на слабых
  компьютерах это может занять прилично времени.

// .is-open { // display: block; // position: fixed; // // height: 100vh; // z-index: 10; //
padding-left: 20px; // padding-right: 20px; // overflow-y: scroll; // }

// .menu-wrapper { // display: none; // width: 100%; // height: 100vw; // top: 0; // right: 0; //
padding-top: 60px; // padding-left: 20px; // padding-right: 20px; // padding-bottom: 0; //
background-color: var(--mobile-menu-bg); // animation: slide 100ms linear;

// @media screen and (min-width: 768px) and (max-width: 1279px) { // width: 254px; // } // @media
screen and (min-width: 1280px) { // width: auto; // height: auto; // background-color: transparent;
// display: block; // padding: 0; // } // }

position: fixed; display: block; width: 100%; height: 100vw; top: 0; right: 0; padding-top: 60px;
padding-left: 20px; padding-right: 20px; padding-bottom: 0; background-color: var(--mobile-menu-bg);
animation: slide 100ms linear; z-index: 10; overflow-y: scroll;

@media screen and (min-width: 768px) and (max-width: 1279px) { width: 254px; }

@media screen and (min-width: 1280px) { width: auto; height: auto; background-color: transparent;
display: block; padding: 0; }
