# ДЗ

## Как делать:

0. Сделать форк этого репозитория в свой аккаунт (только 1 раз в самом начале).

1. Перед выполнением ДЗ сделайте пул мастера этого репозитория себе в форк (чтобы иметь актуальный код);
2. Обновить зависимости `yarn` или `npm i`;
3. Создайте новую ветку от актуального мастера для выполнения ДЗ;
4. Выполните ДЗ в этой ветке;
5. Сделайте Pull Request этой ветки в мастер моего репозитория;
6. Напишите мне (a.koretskiy@javascript.info) письмо со ссылкой на PR.

Дедлайн – 22:00 по Москве/Киеву за день до занятия.

## HT1

1. Создать компонент **Rate**, который принимает рейтинг (число от 1 до 5) и его отображает (можно просто показать число, можно нарисовать звездочки и раскрасить их, и т.д.). Например `<Rate value={3} />`.
2. Создать компонент **Reviews**, который принимает все ревью по одному ресторану и отображает имена и отзывы про ресторан, а так же рейтинг с помощью компонента **Rate**.
3. Создать компонент **Restaurant** (рендерить там, где сейчас **Menu**). В **Restaurant** показывать **Menu** и **Reviews**, а так же средний рейтинг с помощью компоненты **Rate**.

## HT2

1. Покрыть **PropTypes** все компоненты (только то, что используется в компоненте).
2. Написать тесты на уменьшение блюд (опционально - без клика по increment).
3. Покрыть тестами **Reviews** (теститовать только разметку).

## HT3

1. Сделать компонент **Basket** в котором отображать выбранные товары с их количеством, суммой по каждому товару и общей стоимостью заказа.
2. Сделать у каждой позиции в этом заказе кнопки **+**, **-**, **х** (при нажатии на **х** удаляеься все количество товара)

## HT4

1. Переписать редьюсеры **review** и **restaurant** на key=>value (аналогично **products**)
2. Добавить **users** редьюсер (так же key=>value)
3. Починить отображение **Review** компонента (взять данные из редьюсеров **review** и **users**)
4. Переписать все обращения в к стейту в mapStateToProps на селекторы (аналогично компоненту **Basket**)
5. Написать **middleware** для генерации **[uuid](https://github.com/uuidjs/uuid)**
6. Реализовать добавление нового review и юзера в стор и показывать его (мы считаем, что на каждый новый отзыв у нас добавляется новый пользователь)

## HT5

1. Загрузить **products** через **api middleware**, грузить только для текущего ресторана
2. Загрузить **users** через **redux-thunk**
3. Дописать обратотку екшенынов **LOAD_REVIEWS** в **reviews** редьюсере
4. Полностью убрать **fixtures** из приложения (удалить все импорты и сам файл), все грузить с сервера
5. При загрузках показывать лоадеры, все грузить максимально низко, там где эти данные нужны
6. Все данные грузить только один раз (не загружать повторно данные, которые уже есть)
7. (Опционально) переписать все на **immer**

# HT6

1. Сделать reviews/menu отдельными роутами (/restaurants/:id/reviews)
2. В корзине сделать продукты линками на их ресторан

## HT7

1. Сделать редирект со **/** и с **/restaurants** на страницу ресторана
2. Проверить если мы на **/checkout**, то при нажатии на кнопку:

- отправить **POST** запрос на: '/api/order' с **JSON** формата [{id: "d75f762a-eadd-49be-8918-ed0daa8dd024", amount: 2}]
- блокировать кнопку на время запроса (можно добавить лоадер)
- при успешном ответе (при сумме заказа от 50 до 200) редиректить на новую страницу "Спасибо за заказ!" и очищать корзину
- при ошибке редиректить на странцу ошибки, показать текст ошибки

3. Реализовать переключение валюты, хранить словарь словарь в контексте (минимум 3 валюты). Реализовать таким образом, чтобы это было максимально удобный использовать.
4. Анимировать добавление ревью использус css modules
