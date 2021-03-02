## GRAPE: импорт маркетов по заданной ссылке

Необходимо реализовать сервис со следующим функционалом с использованием гема `Grape`.
Данные по маркетам нужно взять отсюда: https://absrest.realexchange.pro/public/tickers24h


Реализовать **2 REST API** метода:

- `GET` /currencies — должен возвращать список маркетов 

Пример ответа:

```ruby
  [
    {
    market: 'BCH/BTC',
    base_unit: 'bch',
    quote_unit: 'btc',
    last_price: 0.01209
    },
    {
    market: 'BCH/USDT',
    base_unit: 'bch',
    quote_unit: 'usdt',
    last_price: 291.14
    },
    # ........
  ]
```

- `GET` /currency/ — должен возвращать информацию про маркет по имени маркета. 

Пример ответа:

```ruby
  {
    market: 'BCH/BTC',
    base_unit: 'bch',
    quote_unit: 'btc',
    last_price: 0.01209
  }
```

`base_unit` и `quote_unit` нужно вытянуть c поля `market`.

При REST запросе на ваш сервис, ваше приложение должно взять данные со стороннего сервиса и выдать отформатированный ответ.
