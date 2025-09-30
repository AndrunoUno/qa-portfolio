# TC_API_001 Создание нового питомца через POST /pet

**Приоритет:** High

**Окружение:**
- Postman v11.63.3
- Swagger Petstore API (https://petstore.swagger.io/#/)

**Предусловие:** Подготовлен корректный JSON-файл с данными питомца:

``` json
{
  "id": 102,
  "category": {
    "id": 666,
    "name": "Dogster"
  },
  "name": "Test-Dog",
  "photoUrls": [
    "string"
  ],
  "tags": [
    {
      "id": 666,
      "name": "Dogster"
    }
  ],
  "status": "avaiable"
}
```

## Шаги:
1. Создать новый запрос **POST** к https://petstore.swagger.io/v2/pet
2. В **Body** выбрать формат **raw** - **JSON**
3. Вставить JSON из предусловия
4. Нажать **Send**
5. Проверить ответ

## Ожидаемый результат:
- HTTP-код ответа: **200 OK**
- В теле ответа возвращается объект питомца с теми же данными, что были переданы в запросе (`"id"`, `"category"`, `"name"` и т.д.)
- Созданный питомец доступен для получения по запросу **GET/pet/{id}**
- Статус питомца = `"avaiable"`