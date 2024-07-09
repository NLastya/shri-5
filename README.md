# Домашнее задание ШРИ: Автотесты

## Легенда

Однажды, во время очередной виртуальной прогулки по интернету, кот Шрикс наткнулся на рекламу интернет-магазина зоотоваров. В его глазах загорелся огонек, ведь на сайте красовалась фотография великолепной когтеточки, о которой он давно мечтал.
Шрикс был не просто котом, а котом-разработчиком. Поэтому он знал, что прежде чем купить товар, нужно написать тесты. 
С энтузиазмом Шрикс принялся за работу, стуча лапками по клавиатуре и мурлыкая от азарта. Но есть проблема, у Шрикса лапки, поэтому ему нужна помощь.

## Задача

Вам дано приложение — интернет магазин. С его помощью можно смотреть каталог товаров, добавлять товары в корзину и оформлять заказы.

Форкните этот репозиторий и напишите тесты, проверяющие правильность работы продуктовых сценариев. Проверяйте сценарии модульными/интеграционными тестами, на свое усмотрение.

Главный критерий проверки — автотесты должны находить баги. Дополнительный критерий — на каждый баг должно падать небольшое количество тестов (не больше 1-2).

**Внимание!** Содержимое папки `src` менять нельзя!

## Запуск

```sh
# установите зависимости
npm ci

# соберите клиентский код приложения
npm run build

# запустите сервер
npm start
```

После этого можете открыть приложение в браузере по адресу http://localhost:3000/hw/store

## Как проверять

Вы можете запускать приложение с параметром `bug id`, который может принимать значение от 1 до 10. Каждое из значений `bug id` добавляет в работу приложения какой-то баг. Проверьте, что без параметра `bug id` все тесты проходят, а для каждого значения `bug id` падают 1-2 теста.

Как передать `bug id`:
- при запуске интеграционных тестов передавайте значение в параметре запроса, например, http://localhost:3000/hw/store/catalog/0?bug_id=9
- при запуске модульных тестов передавайте значение в переменной окружения `BUG_ID`, например, `BUG_ID=1 npm run test`
