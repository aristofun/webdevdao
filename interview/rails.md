# Вопросы по Ruby on Rails с собеседований

1. Что такое ActiveRecord, и какие средства предоставляет для работы с обьектами?

    <details>
      <summary>Ответ</summary>
      ActiveRecord это паттерн программирования. AR является популярным способом доступа к данным реляционных баз данных в объектно-ориентированном программировании. ActiveRecord еще называют буквой M в MVC — которая является слоем в системе, ответственным за представление бизнес-логики и данных.

      Active Record упрощает создание и использование бизнес-объектов, данные которых требуют персистентного хранения в базе данных. Сама по себе эта реализация паттерна Active Record является описанием системы ORM (Object Relational Mapping). Active Record это фреймворк ORM.

      Active Record предоставляет нам несколько механизмов, наиболее важными из которых являются способности для:

      * Представления моделей и их данных.
      * Представления связей между этими моделями.
      * Представления иерархий наследования с помощью связанных моделей.
      * Валидации моделей до того, как они станут персистентными в базе данных.
      * Выполнения операций с базой данных в объектно-ориентированном стиле.

      Подробнее:

      * http://rusrails.ru/active-record-basics
      * https://dic.academic.ru/dic.nsf/ruwiki/1264999
    </details>

1. За что отвечают Model, View, Controller уровни в Rails?

    <details>
      <summary>Ответ</summary>
      MVC — это паттерн программирования, который подразумевает схему разделения данных приложения, пользовательского интерфейса и управляющей логики на три отдельных компонента.
    </details>

1. Как работает роутинг? Что такое ресурсные роуты? Как они формируются?

    <details>
      <summary>Ответ</summary>
      Браузеры запрашивают страницы от Rails, выполняя запрос по URL, используя определенный метод HTTP, такой как GET, POST, PATCH, PUT и DELETE.

      Роутинг распознает запрос по методу и по URL и направляет его в экшн контроллера или в приложение Rack.

      Он также может генерировать пути и URL, избегая необходимость жестко прописывать строки в ваших вьюхах.

      Ресурсный роутинг позволяет быстро объявлять все общие маршруты для заданного ресурсного контроллера. Вместо объявления отдельных маршрутов для экшнов `index`, `show`, `new`, `edit`, `create`, `update` и `destroy`, ресурсный маршрут объявляет их одной строчкой кода.

      http://rusrails.ru/rails-routing
    </details>

1. Как использовать `content_for` и `yield`?
1. Что такое скоупы (scopes)? Как использовать?

    <details>
      <summary>Ответ</summary>
      Скоупы позволяют задавать часто используемые запросы, к которым можно обращаться как к вызовам метода в связанных
      объектах или моделях. С помощью этих скоупов можно использовать такие методы как where, joins и includes.
      Все методы скоупов возвращают объект `ActiveRecord::Relation`, который позволяет вызывать на нем
      дополнительные методы (такие как другие скоупы).
      
      Для определения простого скоупа мы используем метод scope внутри класса, передав запрос, который хотим запустить при вызове этого скоупа:
      
      ```rb
      class Article < ApplicationRecord
        scope :published, -> { where(published: true) }
      end
      
      ```
      Подробнее [тут](http://rusrails.ru/active-record-query-interface#scopes)
    </details>
    
1. Что такое синглтон метод?
1. Что такое ActiveJob? Когда его использовать?
1. Что такое Asset Pipeline?
1. Что такое serializer и для чего он нужен? Где применяется? В чем его основная задача?
1. Что такое presenter и для чего он нужен? Где применяется? В чем его основная задача?
1. Что такое валидации? Как написать свои валидации? Для чего нужны валидации? Где применяются валидации? Примеры Валидаций.
1. Есть ли у Rails механизм, который отслеживает изменения в базе данных?
1. Что такое `Rack`?

    <details>
      <summary>Ответ</summary>
      https://www.8host.com/blog/kratkij-obzor-veb-serverov-dlya-prilozhenij-ruby/

      Rack это промежуточное программное обеспечение, оно делит входящие HTTP-запросы на различные этапы, затем обрабатывает их по частям, после чего посылает ответ веб-приложения (контроллера).

      Программа Rack  состоит из двух отдельных компонентов: обработчика и адаптера, с помощью которых происходит обмен данными между веб-серверами и приложениями (фреймворками).

      Какие серверы есть:

      * Phusion Passenger
      * Puma
      * Thin
      * Unicorn

      [Как устроен Rack](https://gist.github.com/Integralist/8341704)

      * https://www.youtube.com/watch?v=NJ-ilQMsqMs
      * https://www.youtube.com/watch?v=MHYMObuEahc
      * https://www.youtube.com/watch?v=DzrVB1-KyTU
    </details>

1. Что такое `partial` и для чего используются?

    <details>
      <summary>Ответ</summary>
      partial — это кусочек кода, который можно вынести в отдельный темплейт, для удобства использования и для использования в других представлениях.
    </details>

1. Что такое Haml, Slim? Какие плюсы на ваш взгляд, их использования?

    <details>
      <summary>Ответ</summary>
      Haml и Slim — это шаблонизаторы, используются для удобства использования и минимизации написания кода в представлениях. Сокращает в несколько раз написание кода, нет проблем в закрывании тегов, не получится что тег не закрыт и код не работает. Меньше вероятность что можно ошибиться + лучше читаемость в коде.

      http://slim-lang.com

      https://haml.ru
    </details>

1. Что означает несколько расширений файла example.html.erb?

    <details>
      <summary>Ответ</summary>

      **example** — название файла

      **html** — расширение, которое позволяет использовать стандартный язык разметки HyperText Markup Language

      **erb** — позволяет включить использование кода написанного на языке Ruby вместе с языком разметки
    </details>

1. Что такое ERB? Можете расшифровать аббревиатуру?

    <details>
      <summary>Ответ</summary>
      ERB — Embedded Ruby (встроенный Ruby)
    </details>

1. Знать и рассказать структуру папок Rails приложения.

    <details>
      <summary>Ответ</summary>
    
       📂 app — основные файлы приложения
       └📁 assets — картинки, стили, js
       └📁 controllers — контроллеры
       └📁 helpers — хелперы
       └📁 jobs — задания
       └📁 mailers — рассыльщики
       └📁 models — модели
       └📁 views — представления
        └📁 layouts — макеты
       📂 config — конфигурация маршрутов, базы данных и т.д
        └📁 environments — настройки сред приложения
        └📁 locales — интернационализация
       📂 db — текущая схема базы данных, сиды
        └📁 migrates — файлы миграции
       📂 lib — внешние модули
       📂 log — журналы логов
       📂 public — доступна извне как есть, статичные файлы и скомпилированные ассеты
       📂 test — структурирована по тестам моделей / контроллеров / интеграционным
        └📂 fixtures — вспомогательные данные (фикстуры)
       📂 tmp — временные файлы (такие как файлы кэша и pid)
       📂 vendor — код сторонних разработчиков, например, внешние гемы.
        └📂 plugins — внешние плагины

      http://rusrails.ru/getting-started-with-rails#sozdanie-prilozheniya-blog
    </details>

1. Какие связи для связывания моделей в приложении Rails вы знаете?

    <details>
      <summary>Ответ</summary>
      Rails поддерживает шесть типов связей:

      * `belongs_to`
      * `has_one`
      * `has_many`
      * `has_many :through`
      * `has_one :through`
      * `has_and_belongs_to_many`

      http://rusrails.ru/active-record-associations#tipy-svyazey
    </details>

1. Привести примеры использования `has_many`, `belongs_to`, `has_and_belongs_to_many`, `has_one`, `has_many :through`?

    <details>
      <summary>Ответ</summary>
      Фильм имеет имеет множество сезонов, сезон принадлежит фильму и имеет множество серий. У каждого фильма может быть только один официальный сайт. В каждом фильме снимается множество актёров, при этом каждый актёр снимается в разных фильмах:

      ```rb
      class Film < ApplicationRecord
        has_many :seasons
        has_many :episodes, through: :seasons

        has_one :official_site
        has_and_belongs_to_many :actors
      end

      class Season < ApplicationRecord
        belongs_to :film
        has_many :episodes
      end

      class Episode < ApplicationRecord
        belongs_to :season
      end

      class OfficialSite < ApplicationRecord
        belongs_to :film
      end

      class Actor < ApplicationRecord
        has_and_belongs_to_many :films
      end
      ```

      http://rusrails.ru/active-record-associations#tipy-svyazey
    </details>

1. Что лучше выбрать `has_many :through` или `has_and_belongs_to_many`?

    <details>
      <summary>Ответ</summary>

      Это зависит от контекста связи `many-to-many`.

      Если планируется использование дополнительной логики в этой связи, создание дополнительных полей в соединительной табице, то лучше отдать предпочтение `has_many :through`. В этом случае применяются промежуточные модели-связки.

      В том случае, если достаточно простой соединительной таблицы, то можно обойтись `has_and_belongs_to_many` (т.н. HBTM).

      http://rusrails.ru/active-record-associations#dopolnitelnye-metody-stolbtsov
    </details>

1. Что такое полиморфные связи?

    <details>
      <summary>Ответ</summary>
      Особый вид связи, при которой модель может принадлежать сразу нескольким моделям.

      Например, картинку можно добавлять к статье, комментарию, пользователю.

      ```rb
      class Picture < ApplicationRecord
        belongs_to :imageable, polymorphic: true
      end

      class Article < ApplicationRecord
        has_many :pictures, as: :imageable
      end

      class Comment < ApplicationRecord
        has_many :pictures, as: :imageable
      end

      class User < ApplicationRecord
        has_many :pictures, as: :imageable
      end
      ```

      При этом картинка сохраняет в себе имя класса и `id` объекта, которому она принадлежит. В приведённом примере у картинки имеются атрибуты `imageable_id` и `imageable_type`, это возможно благодаря миграции:

      ```rb
      class CreatePictures < ActiveRecord::Migration[5.2]
        def change
          create_table :pictures do |t|
            t.references :imageable, polymorphic: true, index: true
          end
        end
      end
      ```

      http://rusrails.ru/active-record-associations#polymorphic-associations

    </details>

1. Что такое `pluralize` и как он может быть полезен на проекте?
1. Что такое `i18n` (интернационазиция)?

    <details>
      <summary>Ответ</summary>
      Гем, поставляемый с Ruby on Rails (начиная с Rails 2.2), представляет простой и расширяемый фреймворк для перевода приложения на язык, отличный от английского.

      Rails автоматически добавляет все файлы `.rb` и `.yml` из директории `config/locales` к пути загрузки переводов.

      http://rusrails.ru/rails-internationalization-i18n-api
    </details>

1. Что такое `dependent` связь?

    <details>
      <summary>Ответ</summary>

      Опция `:dependent` указывает, что необходимо сделать с зависимой моделью (моделями) при удалении текущей модели. В зависимости от типа связи может принимать значения:

      * `:delete` — связанные объекты будут удалены прямо из базы данных без вызова метода `destroy`, т.е. без соответствующих коллбэков
      * `:delete_all` — см. `:delete`
      * `:destroy` — будет вызван `destroy` на связанных объектах
      * `:nullify` — внешний ключ будет установлен `NULL`
      * `:restrict_with_error` — при наличии связанного объекта вызовет ошибку
      * `:restrict_with_exception` — при наличии связанного объекта вызовется исключение


      http://rusrails.ru/active-record-associations
    </details>

1. Что такое `t.references`?

    <details>
      <summary>Ответ</summary>
      Столбец таблицы в миграции, указывающий на принадлежность к другой таблице. Например, книга принадлежит автору:

      ```rb
      class CreateBooks < ActiveRecord::Migration[5.2]
        def change
          create_table :books do |t|
            t.references :author
          end
        end
      end
      ```

      http://rusrails.ru/active-record-associations
    </details>

1. Что такое exception и от чего наследуется?
1. Как сгенерировать модель, конторллер, представление (вьюху)
1. Что такое scaffolding? Зачем он используется и где применяется?
1. Как реализовано кеширование в рельсах?
1. Представьте, что есть огромная табл. `users`. Как можно перебрать ее элементы максимально быстро?

    <details>
      <summary>Ответ</summary>
      Быстро можно перебрать с помощью find_each, стандартно по 1000 записей.

      * `batch_size` — сколько обрабатывать записей за раз
      * `start` — с какого id к примеру продолжить работу
      * `finish` — может использоваться совместно с `start`, к примеру чтобы выслать письма только пользователям с первичным ключом от 2000 до 10000:

      https://apidock.com/rails/ActiveRecord/Batches/ClassMethods/find_each

      http://rusrails.ru/active-record-query-interface
    </details>

1. Как можно решить проблему N+1 в Rails?

    <details>
      <summary>Ответ</summary>
      Указанный код выполнит 10 + 1 запрос в БД (первый запрос загрузит 10 клиентов, а затем для каждого клиента будет сделано по запросу).

      ```rb
      clients = Client.limit(10)

      clients.each do |client|
        puts client.address.postcode
      end
      ```

      Проблему N+1 можно решить при помощи метода `includes`, при этом Active Record обеспечивает то, что все указанные связи загружаются с использованием минимально возможного количества запросов:

      ```rb
      clients = Client.includes(:address).limit(10)

      clients.each do |client|
        puts client.address.postcode
      end
      ```

      В данном случае будет сделано всего два запроса:


      ```sql
      SELECT * FROM clients LIMIT 10
      SELECT addresses.* FROM addresses WHERE (addresses.client_id IN (1,2,3,4,5,6,7,8,9,10))
      ```

      http://rusrails.ru/active-record-query-interface#neterpelivaya-zagruzka-svyazey
    </details>

1. Как без рендеринга шаблона сказать мобильному приложению, что у него нет прав на просмотр определённого контента одной строкой в контроллере?

    <details>
      <summary>Ответ</summary>

      ```rb
      head :forbidden
      ```

      или

      ```rb
      render status: 403
      ```

      https://guides.rubyonrails.org/layouts_and_rendering.html
    </details>

1. Что такое Service Objects, Form Objects, View Objects, Query Objects, для чего они нужны?

    <details>
      <summary>Ответ</summary>
      Это обычные классы Ruby, которые применяются для рефакторинга Rails-приложения, инкапсулируя часть логики моделей / представлений / контроллеров.

      Service Objects, например, используются, когда одновременно задействованы несколько моделей, когда производятся сложные действия с моделями.

      Form Objects используются, когда отправка одной формы изменяет несколько моделей.

      View Objects используются, например, когда большой метод внутри модели используется только отображения данных.

      Query Objects используются для сложных SQL запросов, утяжеляющих модели/контроллеры.

      https://habr.com/ru/post/158011/
    </details>

Где искать ответы:

* http://guides.rubyonrails.org/
* http://rusrails.ru/
* http://ruby-doc.org
