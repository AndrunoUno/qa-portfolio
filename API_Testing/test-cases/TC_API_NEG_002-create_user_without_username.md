# TC_API_NEG_002 - Поптыка создать пользователя без username через POST /user

**Приоритет:** High

**Окружение:**
- Postman v11.64.8
- Swagger Petstore API (https://petstore.swagger.io/#/)

## Шаги:
1. Создать новый запрос **POST** к https://petstore.swagger.io/v2/pet
2.  В **Body** выбрать формат **raw** - **JSON**
3. Вставить JSON с заполненными данными, например:
``` json
{
  "id": 77,
  "username": "",
  "firstName": "Name",
  "lastName": "Surname",
  "email": "test@mail.ccc",
  "password": "pass",
  "phone": "+12345678900",
  "userStatus": 0
}
```
4. Нажать **Send**
5. Проверить ответ

# Ожидаемый результат
- Система должна вернуть ошибку HTTP `400 Bad Request`
- Сообщение об ошибке `"Username is required"`
-  Регистрация пользователя в системе не происходит