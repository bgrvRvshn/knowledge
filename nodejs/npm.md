## Проверка установки
```bash
node --version | -v
npm --version | -v
```
## Обновление
```bash
npm i -g npm@latest
```
## Инициализация проекта
```bash
npm init

# auto
npm init --yes | -y
```
## Установка зависимостей
```bash
npm install | i

# проверка конкретной зависимости
npm explore [package-name]

# проверка всех зависимостей
npm doctor

# очистка
npm ci
```
## Принудительная переустановка зависимостей
```bash
npm i --force | -f
```
## Установка только продакшн-пакетов
```bash
npm i --only=production | --only=prod
```
## Добавление зависимости
```bash
npm i [package-name]
npm i [package-name@version]
```
## Добавление зависииости для разработки
```bash
npm i --save-dev | -D [package-name]
```
## Обновление зависимости
```bash
npm update | up [package-name]
```
## Удаление зависимости
```bash
# dependency
npm remove | rm | r [package-name]

# devDependency
npm r -D [package-name]
```
## Глобальная установка/обновление/удаление пакета
```bash
npm i/up/r -g [package-name]
```
## Определение устаревших пакетов
```bash
npm outdated
npm outdated [package-name]
```
## Список установленных зависимостей
```bash
npm list | ls

# top level
npm ls --depth=0 | --depth 0

# global + top level
npm ls -g --depth 0
```
## Информация о пакете
```bash
npm view | v [package-name]
```
## Запуск скрипта/выполнение команды
```bash
npm run [script]

# пример
# package.json: "scripts": { "dev": "nodemon server.js" }
npm run dev
```
## Удаление дублирующихся пакетов
```bash
npm dedupe | ddp
```
## Удаление посторонних пакетов
```bash
npm prune
```
## Обнаружение уязвимостей
```bash
npm audit
# json
npm audit --json
# plain text
npm audit --parseable
```
## Автоматическое исправление уязвимостей
```bash
npm audit fix
```
