# msabook

Эта книга задумана мной как максимально полный путеводитель в мир микросервисных архитектур. В первую очередь, она призвана объяснить читателю, что же такое микросервисы и как они устроены, а так же разрушить множество мифов, которые появились в индустрии за последние 10-15 лет.

Связано это в первую очередь с набором практик и подходов, которые пропогандируются во многих популярных книгах и курсах, которые зачастую могут сильно расходится с тем, как строится дизайн реальных production-ready систем. Эта книга поможет вам докопаться до истины, разобраться во многих подходах и научиться понимать, когда и как необходимо принимать различные архитектурные решения, на основании чего и к каким последствиям это может привести.

> [!WARNING]
>
> Работа над книгой ведется в свободное время, из-за чего процесс её написания сильно недетерменирован во времени. Структура страниц, их содержание и даже оглавление могут меняться очень часто. Текущая структура оглавления не является отражением содержимого книги и представляет собой напоминание лично мне о том, что я считаю важным описать в этой книге

## Оглавление

- [Введение]()
  - [Для кого написана эта книга]()
  - [Структура книги]()
- [Что же такое микросервисы?](/)
  - [Определение](/)
  - [Архитектурные драйверы](/)
  - [Мифы и заблуждения]()
    - [Миф 1: Монолитная архитектура - это плохо]()
    - [Миф 2: Монолитная архитектура плохо масштабируется]()
    - [Миф 3: Монолитная архитектура ухудшает TTM]()
  - [Когда декомпозировать монолит?](/)
    - [Сбор и анализ требований]()
      - [Типы требований]()
        - [Functional requirements]()
        - [Non-functional requirements]()
      - [Повему это важно?]()
      - [Новый проект: монолит или микросервисы?]()
    - [Стратегии декомпозиции приложений](/)
- [Взаимодействие систем]()
  - [Стили взаимодействия]()
  - [Синхронные взаимодействия]()
    - [Как реализуются]()
      - [GRPC API]()
      - [HTTP API]()
        - [RPC]()
        - [REST FULL & REST LIKE]()
        - [JSON RPC]()
    - [Как быть, когда существует более одного потребителя апи?]()
  - [Асинхронные взаимодействия]()
    - [События и команды]()
    - [Как реализуются]()
      - [Очереди и брокеры]()
      - [Локальные очереди задач]()
      - [Webhooks]()
- [Синхронное апи: детальное погружение]()
  - [Обрывы соединений]()
    - [Стратегии ретраев]()
    - [Идмепотентность апи]()
  - [Версионирование]()
  - [Circuit breaker]()
  - [Роль Service Mesh в современных системах]()
- [Асинхронное апи: детальное погружение]()
  - [Гарантии доставки событий]()
  - [Версионирование контрактов]()
  - [Задержки сообщений и таймауты]()
  - [Наблюдаемость процессов]()
  - [Реконсиляция]()
  - [Дедупликация]()
    - [Дедупликация в очереди]()
    - [Дедупликация на консьюмерах]()
  - [Competing consumers как способ реализации circuit breaker]()
  - [Анти-паттерны]()
    - [Async request-response]()
- [Транзакции и бизнес-процессы]()
  - [Выбор способов взаимодействия]()
    - [Анализ предметной области]()
    - [Структура организации и потоки ценности (Value Streams)]()
- [Практика]()
  - [Учебный проект]()
  - [Сбор требований и анализ предметной области]()
  - [Итерация 1: HLD]()
  - [Итерация 2: Декомпозиция приложений]()
  - [Резюме]()
