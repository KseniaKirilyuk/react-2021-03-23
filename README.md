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
