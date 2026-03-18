

# Содержание

- [Содержание](#содержание)
- [Добавление](#добавление)
  - [Вне папок _CNext](#вне-папок-_cnext)
    - [В .yml файлах](#добавление-строк-в-yml)
      - [В одну строку](#добавление-строк-вне-папки-_cnext-yml-однострочное)


# Требования к изменениям



## Добавление
#### Вне папок _CNext
##### добавление строк в .yml
###### добавление строк вне папки _CNext .yml однострочное

на той же строке, которую добавили отступаем один пробел, пишем знак комментария(для .yml - `#`, для .cs `//`), пробел, `CNext: ` и название изменения или краткое описание.
то есть выходит следующее:

```yml
...
  - type: SolutionContainerVisuals
    maxFillLevels: 3
    inHandsFillBaseName: null
  - type: Tag
    tags:
      - Bucket
      - Trash # CNext: bucket is trash
  - type: PhysicalComposition
    materialComposition:
      Plastic: 50
```

###### добавление строк вне папки _CNext .yml многострочное

перед строкой которую первую добавили пишем знак комментария(для .yml - `#`, для .cs `//`), а после через пробел `CNext-start: ` и название или краткое описание.
после добавленных строк в конце последней добавленой строки нажимаем enter и нас переводит на строку ниже, там пишем знак комментария(для .yml - `#`, для .cs `//`) и отступив пробел `CNext-end`.
Вот как будет выглядеть:

```yml
...
  - type: SolutionContainerVisuals
    maxFillLevels: 3
    inHandsFillBaseName: null
  - type: Tag
    tags:
      - Bucket
      - Trash # CNext: bucket is trash
  - type: PhysicalComposition
    materialComposition:
      Plastic: 50
  # CNext-start: something
  - type: StaticPrice
    price: 1000
  - type: GuideHelp
    guides:
    - VoltageNetworks
    - Power
  # CNext-end
```

###### добавление компонентов

в случае добавления одного компонента - делаем по данному [методу](#добавление-строк-вне-папки-_cnext-yml-однострочное), но комментарий указываем напротив указания компонента.
Вот как будет выглядеть:

```yml
...
  - type: StaticPrice # CNext: added price
    price: 1000
...
```

При добавлении нескольких компонентов - делаем по [методу](#добавление-строк-вне-папки-_cnext-yml-однострочное)





# TODO
позже эти требования дополнятся
