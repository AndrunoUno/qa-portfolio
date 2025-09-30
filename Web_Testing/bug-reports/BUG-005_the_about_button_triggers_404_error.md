# BUG-005 - Кнопка "About" вызывает ошибку 404

### Priority: Medium
### Severity: Major

**Описание:**
При переходе по кнопке “About” на боковой панели слева, открывается страница 404

**Предусловие:** 
- Пользователь авторизован на сайте https://www.saucedemo.com/ (login - *problem_user*, password - *secret_sauce*)
- Пользователь находится на главной странице товаров

### Шаги для воспроизведения:
1. Развернуть боковую панель, нажав на кнопку с тремя горизонтальными полосками (слева вверху);
2. Нажать кнопку “About”;
3. Обратить внимание на результат.

### Ожидаемый результат:
Открывается страница “About”.

### Фактический результат:
Ошибка 404.

**Окружение:**
- ОС: Windows 11
- Браузер: Google Chrome
- Версия браузера: 139.0.7258.139
- Устройство: ПК

**cURL:**
```
curl ^"https://saucelabs.com/error/404^" ^
  -X ^"HEAD^" ^
  -H ^"accept: /^" ^
  -H ^"accept-language: ru-RU,ru;q=0.9,en-US;q=0.8,en;q=0.7,uk;q=0.6^" ^
  -H ^"baggage: sentry-environment=production,sentry-release=pAL4B7VgLWviE_rgwti8J,sentry-public_key=d9ae8432ca8e442aa512c487f8327757,sentry-trace_id=e3cacbecd8cb4c99958fd839efb42718^" ^
  -b ^"__gtm_referrer=https^%^3A^%^2F^%^2Fwww.saucedemo.com^%^2F; _rtfl_s_handshake_guid=00462df7-db7f-401e-a66e-4df30ab4b4f0; _mkto_trk=id:468-XBT-687^&token:_mch-saucelabs.com-718be859277d5fc1577d1af0fc133231; cb_user_id=null; cb_group_id=null; cb_anonymous_id=^%^2224beb20c-85bc-4582-868d-b4de2ff6c1bf^%^22; _gcl_au=1.1.1774523454.1756297001; _gid=GA1.2.800384747.1756297001; _ga_8VH1KDRPL5=GS2.1.s1756297001^$o1^$g1^$t1756297249^$j60^$l0^$h2042879934; _ga=GA1.2.1329136458.1756297001; _dc_gtm_UA-6735579-1=1; OptanonConsent=isGpcEnabled=0^&datestamp=Wed+Aug+27+2025+15^%^3A20^%^3A50+GMT^%^2B0300+(^%^D0^%^9C^%^D0^%^BE^%^D1^%^81^%^D0^%^BA^%^D0^%^B2^%^D0^%^B0^%^2C+^%^D1^%^81^%^D1^%^82^%^D0^%^B0^%^D0^%^BD^%^D0^%^B4^%^D0^%^B0^%^D1^%^80^%^D1^%^82^%^D0^%^BD^%^D0^%^BE^%^D0^%^B5+^%^D0^%^B2^%^D1^%^80^%^D0^%^B5^%^D0^%^BC^%^D1^%^8F)^&version=202301.2.0^&isIABGlobal=false^&hosts=^&consentId=498f182a-015e-4933-8998-9440bf6172ed^&interactionCount=1^&landingPath=https^%^3A^%^2F^%^2Fsaucelabs.com^%^2Ferror^%^2F404^&groups=C0001^%^3A1^%^2CC0003^%^3A0^%^2CC0002^%^3A0^%^2CC0004^%^3A0^%^2CC0005^%^3A0; _rdt_uuid=1756296645209.9d92769d-14ac-43d7-8f4e-8cd37e8b7f00; _uetsid=b12751c0833f11f0a107973a9d85ad2d; _uetvid=b1275130833f11f0835b2bc13447788b^" ^
  -H ^"dnt: 1^" ^
  -H ^"newrelic: eyJ2IjpbMCwxXSwiZCI6eyJ0eSI6IkJyb3dzZXIiLCJhYyI6IjkzMzM5NCIsImFwIjoiMTEzNDMxMjQxNyIsImlkIjoiYzE0MzMxYWIzNTgwNjU3NyIsInRyIjoiZGNmMTFjY2Q2NmQ3NDlhNzNiYWEyNmE2ODI0MGZlMjAiLCJ0aSI6MTc1NjI5NzI1MTQxNywidGsiOiIxMzgwNzA1In19^" ^
  -H ^"priority: u=1, i^" ^
  -H ^"referer: https://saucelabs.com/error/404^" ^
  -H ^"sec-ch-ua: ^\^"Not;A=Brand^\^";v=^\^"99^\^", ^\^"Google Chrome^\^";v=^\^"139^\^", ^\^"Chromium^\^";v=^\^"139^\^"^" ^
  -H ^"sec-ch-ua-mobile: ?1^" ^
  -H ^"sec-ch-ua-platform: ^\^"Android^\^"^" ^
  -H ^"sec-fetch-dest: empty^" ^
  -H ^"sec-fetch-mode: cors^" ^
  -H ^"sec-fetch-site: same-origin^" ^
  -H ^"sentry-trace: e3cacbecd8cb4c99958fd839efb42718-94d29d3da4d902a2-0^" ^
  -H ^"traceparent: 00-dcf11ccd66d749a73baa26a68240fe20-c14331ab35806577-01^" ^
  -H ^"tracestate: 1380705^@nr=0-1-933394-1134312417-c14331ab35806577----1756297251417^" ^
  -H ^"user-agent: Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/139.0.0.0 Mobile Safari/537.36^"
```
