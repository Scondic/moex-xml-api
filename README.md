# moex-xml-api

Чтобы получить данные из гугл-таблицы, нужно чтобы в настройках региона стояла "Россия"
[Google таблица](https://docs.google.com/spreadsheets/d/1c7akGp4hwZpsmysTj_YQ4U8zGnNBllEWy-EpRW0UTDU/edit?usp=sharing)

## Облигации
### TQCB
Получение списка облигаций с процентом к номиналу
```ts
https://iss.moex.com/iss/engines/stock/markets/bonds/boards/TQCB/securities.xml?iss.meta=off&iss.only=securities&securities.columns=SECID,PREVPRICE

=IMPORTXML(
  "https://iss.moex.com/iss/engines/stock/markets/bonds/boards/TQCB/securities.xml?iss.meta=off&iss.only=securities&securities.columns=SECID,PREVPRICE",
  "//row[@SECID='"&A1&"']/@PREVPRICE"
)
```

Получение списка облигаций с номинальной стоимостью
```ts
https://iss.moex.com/iss/engines/stock/markets/bonds/boards/TQCB/securities.xml?iss.meta=off&iss.only=securities&securities.columns=SECID,FACEVALUE

=IMPORTXML(
  "https://iss.moex.com/iss/engines/stock/markets/bonds/boards/TQCB/securities.xml?iss.meta=off&iss.only=securities&securities.columns=SECID,FACEVALUE",
  "//row[@SECID='"&A1&"']/@FACEVALUE"
)
```

### TQOB
Получение списка облигаций с процентом к номиналу
```ts
https://iss.moex.com/iss/engines/stock/markets/bonds/boards/TQOB/securities.xml?iss.meta=off&iss.only=securities&securities.columns=SECID,PREVPRICE

=IMPORTXML(
  "https://iss.moex.com/iss/engines/stock/markets/bonds/boards/TQOB/securities.xml?iss.meta=off&iss.only=securities&securities.columns=SECID,PREVPRICE",
  "//row[@SECID='"&A1&"']/@PREVPRICE"
)
```

Получение списка облигаций с номинальной стоимостью
```ts
https://iss.moex.com/iss/engines/stock/markets/bonds/boards/TQOB/securities.xml?iss.meta=off&iss.only=securities&securities.columns=SECID,FACEVALUE

=IMPORTXML(
  "https://iss.moex.com/iss/engines/stock/markets/bonds/boards/TQOB/securities.xml?iss.meta=off&iss.only=securities&securities.columns=SECID,FACEVALUE",
  "//row[@SECID='"&A1&"']/@FACEVALUE"
)
```


## Акции
### TQCB
Получение списка акций со стоимостью одного лота
```ts
https://iss.moex.com/iss/engines/stock/markets/shares/boards/TQBR/securities.xml?iss.meta=off&iss.only=securities&securities.columns=SECID,PREVPRICE

=IMPORTXML(
  "https://iss.moex.com/iss/engines/stock/markets/shares/boards/TQBR/securities.xml?iss.meta=off&iss.only=securities&securities.columns=SECID,PREVPRICE",
  "//row[@SECID='"&A1&"']/@PREVPRICE"
)
```

Получение списка акций с количеством лотов
```ts
https://iss.moex.com/iss/engines/stock/markets/shares/boards/TQBR/securities.xml?iss.meta=off&iss.only=securities&securities.columns=SECID,LOTSIZE

=IMPORTXML(
  "https://iss.moex.com/iss/engines/stock/markets/shares/boards/TQBR/securities.xml?iss.meta=off&iss.only=securities&securities.columns=SECID,LOTSIZE",
  "//row[@SECID='"&A1&"']/@LOTSIZE"
)
```
