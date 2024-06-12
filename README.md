# TZ_Testirovshik_Chuvakorzin_B.A.
Тестовое задание на Тестировщика. Чувакорзин Б.А.

Общие вопросы:

1. По-вашему - кто такой QA инженер?
Как я понял, QA инженер – это it-специалист, который участвует в процессе формирования приложения, сайта или другого продукта сети в качестве тестировщика, а именно, он проверяет (тестирует) продукт на каждом этапе его разработки с целью повышения качества самого продукта для пользователей.

2. Что такое тестирование?
Тестирование - это действия тестировщика, направленные на выявление ошибок в работе программы, приложения или ПО в процессе подготовки их к выходу в открытый доступ.

3. Зачем вообще проводить проверку ПО?
Тестирование ПО необходимо проводить для своевременного выявления ошибок в работе программы, приложения или ПО, а также для проверки соответствия программы требованиям заказчика.
Проверка ПО направлена на то, чтобы продукт полностью был готов к выпуску. То есть, в процессе тестирования проверяются его надежность, стабильность и качество.
Тестирование помогает сократить возможные расходы на устранение ошибок уже выпущенного ПО.

Логическая задача:
Решение:
Для решения данной задачи необходимо пойти с конца возможных вариантов развития событий.
1. Самый последний вариант - это когда остаётся 2 пирата, так как по правилам необходимо, чтобы хотя бы половина пиратов была согласна с делением монет. Таким образом, если остаётся только 4 и 5 пират, то 4 оставит себе все 100 монет, а 5 ничего не получит.
2. Если остаётся три пирата (3, 4 и 5), то необходимо, чтобы двое из 3 пиратов проголосовали "За". 3 пират оставляет себе 99 монет, а 1 монету отдаёт 5 пирату, так как 4 пирату выгодна смерть 3. А в случае смерти 3 пирата, 5 пират ничего не получит.
3. Если остаётся 4 пирата (2, 3, 4 и 5), то опять хотя бы 2 пирата должны быть согласны с распределением. Получается, что 2 пират оставит себе 99 монет. Третьему пирату ничего не даст, так как ему выгодна смерть 2ого. Зато даст 1 монету 4 пирату, так как в случае смерти 2ого пирата, 4ый ничего не получит.
4. Все живы. Необходимо, чтобы 3 пирата были согласны с распределением. 1ый оставляет себе 98 монет. Второму пирату ничего не даёт, так как ему выгодна смерть 1ого. Зато 1ый отдаст по 1 монете 3 и 5 пиратам, так как в случае смерти 1ого пирата, 3 и 5 пираты ничего не получат.
Ответ: 1-ый пират оставит себе 98 монет. 3-ий и 5-ый пираты получат по 1 монете.

 
Задачи на тестирование:
1. Как протестировать сломанный тостер?
Необходимо понимать, что именно сломано в тостере: может быть он даже включается и просто не работает какой-то конкретный функционал. Это выясним ниже.
1) Smoke-тестирование: проверка работоспособности тостера – подключение его к сети.
Если тостер работает, то необходимо проверить его функционал, так как, возможно, что-то 1 вышло из строя.
2) Функциональное тестирование:
- проверка выбора уровня прожарки тоста. Правильную работу данного функционала мы можем проверить при прожарке нескольких порций тостов с выбором разного уровня прожарки каждый раз;
- проверка нагревательного элемента. Проверяется при загрузке в тостер кусков хлеба и запуске его в работу;
- проверка работоспособности механизма (рычага), который выталкивает тосты после завершения работы программы по их обжарке. Это мы сможем проверить по истечении определенного времени, то есть когда тосты должны быть готовы;
- проверка автоотключения после приготовления тостов;
- проверка дополнительных функций тостера, которые бывают не во всех моделях: функция предварительной разморозки тостов, подогрев уже готовых остывших тостов, прожарка особых рисунков на тостах с помощью специальных шаблонов.
3) Нефункциональное тестирование:
- проверка на совместимость с различным видом хлеба, так как, возможно, из-за маленького размера хлеба, булки или другого хлебобулочного изделия, уже приготовленный тост не выходит наружу;
- проверка на совместимость данного тостера с различным составом хлебобулочных изделий. Не подходящий хлеб или булка может сгореть снаружи, но быть абсолютно не готовой внутри.
4) Тестирование установки:
Возможно, рассматриваемый тостер имеет функцию Умного дома, которая перестала работать и тостер перестал подключаться к телефону и готовить тосты по сценарию. Нужно проверить сам протокол, с помощью которого она подключается к системе «Умный дом». Возможно, это обычный bluetooth адаптер вышел из строя.

2. В приложении к тестовому заданию вы найдете 2 скриншота - реальное приложение (приложение №1) и макет (приложение №2). Найдите ошибки при реализации. Опционально - дайте рекомендации по улучшению.
Ошибки при реализации Приложение № 1:
1) отсутствуют точки после сокращений до одной буквы следующих слов: город (г), улица (ул), дом (д);
2) адрес явно определился неправильно: должна быть указана всего 1 улица, а в тексте указаны 2 разные улицы. Даже если так указал получатель карты, то приложение не должно было позволить перейти на следующий шаг, пока пользователь не укажет точный адрес. (куда поедет курьер?);
3) в конце текста стоит знак «многоточие» - здесь явно не влезла вся информация, которая необходима клиенту, например, время доставки карты курьером по указанному адресу или что-нибудь ещё.
Рекомендации по улучшению Приложение № 1:
1) Необходимо добавить информацию о типе карты и ее тарифе: дебетовая, кредитная, детская и т.д.;
2) Обязательно должно быть точное время или промежуток времени, когда курьер должен привезти карту;
3) Я бы добавил кнопку «перенести доставку», так как у клиента могли измениться планы на выбранный день и время;
4) Стоит добавить информацию о том, что должно быть с собой у клиента в момент доставки карты, вдруг он выбрал адрес офиса, а не своей квартиры, и у него не окажется с собой паспорта.
Ошибки при реализации Приложение № 2:
1) указана дата, до которой можно получить карту – 19 декабря, но нет года.
Рекомендации по улучшению Приложение № 2:
1) Напоминание «Не забудьте паспорт» стоит выделить, например, написать его с новой строки, выделить курсивом или полужирным шрифтом. Это привлечет внимание клиента, и он точно возьмет с собой необходимые документы;
2) Возможно, здесь уместно добавить кнопку «продлить дату получения карты», если банк предоставляет такую возможность. Так как у клиента уже на данный момент известно, что он надолго уезжает в командировку или поедет в отпуск вплоть до указанной в приложении даты;
3) Опять-таки не хватает информации о типе карты и ее тарифе.

3. Вам передали на тестирование калькулятор и список проверок к нему, которые написал предыдущий QA. Требования описаны чуть ниже. Ваша задача - проверить корректность этих проверок.
Ошибки:
1) № 4 чек-листа «Пятнадцать умножить на двадцать пять»:
фактический результат – «375 (триста семьдесят пять)» - верный.
Ошибка в ожидаемом результате – неправильно выполнены расчеты;
2) № 5 чек-листа «Одна целая две десятых разделить на семь»:
ожидаемый результат – «0,17143 (ноль целых семнадцать тысяч сто сорок три стотысячных)» - верный.
Ошибка в фактическом результате - неправильно произведено округление до 5-го знака после запятой;
3) № 6 чек-листа «Минус один + 1»:
Фактический результат – «-1 (минус один)» - верный.
Ошибка в ожидаемом результате – скорее всего калькулятор принимает первое отрицательное число (-1) за 1 действие, а так как он может выполнить только 1 действие, а не 2, поэтому и получается ошибка.
4) № 7 чек-листа «Триста четыренадцать минус 14»:
Ожидаемый результат – «Некорректный ввод (?)» - верный.
Ошибка в фактическом результате – калькулятор распознал правильно написанное число «Триста», однако не обратил внимание на следующее некорректно написанное число «четыренадцать» и прогнал расчет без его учета.
