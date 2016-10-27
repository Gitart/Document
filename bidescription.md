# Description BI API
Описание для взаимодействия систем расчета ВI и внешних систем



## Основные API для BI
|API|Method|Description|
|----|----|----|
|**/bi/task**|GET|Получение задания для расчета
|**/bi/load**|POST|Для загрузки данных из системы BI 
|**/bi/directory/pharmacy**|GET|Справочник торговых точек  
|**/bi/directory/anlyses**|GET|Справочник перечня анализа
|**/bi/data/{key}**|GET|Получение готового расчитанного результата BI по ключу для ТТ


## Данные из системы BI
```
  {
    "ID": "string", 
    "ID_STRUCTURE":"QWWE-RYRYR-RKOITOT-ROOROR1",
    "ID_DRUG": "1233445",
    "COUNT":123
   }
```
