```bash
    -------------------------
## Просмотр параметров конфигурации ##
npm config ls -l

    -------------------------
## Проверка установки
node --version | -v
npm --version | -v

    -------------------------
## Обновление
npm i -g npm@latest

    -------------------------
## Инициализация проекта
npm init

# auto
npm init --yes | -y

    -------------------------
## Установка зависимостей
npm install | i

# проверка конкретной зависимости
npm explore [package-name]

# проверка всех зависимостей
npm doctor

# очистка
npm ci

    -------------------------
## Принудительная переустановка зависимостей
npm i --force | -f

    -------------------------
## Установка только продакшн-пакетов
npm i --only=production | --only=prod

    -------------------------
## Добавление зависимости
npm i [package-name]
npm i [package-name@version]

    -------------------------
## Добавление зависииости для разработки
npm i --save-dev | -D [package-name]

    -------------------------
## Обновление зависимости
npm update | up [package-name]

    -------------------------
## Удаление зависимости
# dependency
npm remove | rm | r [package-name]

# devDependency
npm r -D [package-name]

    -------------------------
## Глобальная установка/обновление/удаление пакета
npm i/up/r -g [package-name]

    -------------------------
## Определение устаревших пакетов
npm outdated
npm outdated [package-name]

    -------------------------
## Список установленных зависимостей
npm list | ls

# top level
npm ls --depth=0 | --depth 0

# global + top level
npm ls -g --depth 0

    -------------------------
## Информация о пакете
npm view | v [package-name]

    -------------------------
## Запуск скрипта/выполнение команды
npm run [script]

# пример
# package.json: "scripts": { "dev": "nodemon server.js" }
npm run dev

    -------------------------
## Удаление дублирующихся пакетов
npm dedupe | ddp

    -------------------------
## Удаление посторонних пакетов
npm prune

    -------------------------
## Обнаружение уязвимостей
npm audit

# json
npm audit --json

# plain text
npm audit --parseable

    -------------------------
## Автоматическое исправление уязвимостей
npm audit fix
```
