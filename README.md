## Hometask 3

1.	Создать новый проект, в котором будут все необходимые зависимости для spring boot
2.	Разработать на основе spring boot приложение со следующим функционалом: 
- создайте сервис currency, который загружает данные по котировкам валют за последние n дней, выделяет из них котировку по долларам и сохраняет. Ссылка на документацию по API для выгрузки котировок - https://cbr.ru/development/SXML/. Для обращения к этому API в вашем приложении вам понадобится RestTemplate из Spring MVC. 
- создать сервис weather, который загружает данные о погоде за последние n дней в конкретном городе и сохраняет их. Если город не передан в качестве параметра, то по умолчанию берется Москва. Ссылка на документацию по API - https://www.weatherapi.com/docs/#intro-request. 
- создать два контроллера, каждый из которых отвечает за отправку данных о котировках и погоде клиенту. Оба этих контроллера должны иметь endpoint’ы для возврата данных за n дней, если пользователь указал, что ему нужны данные за n дней, либо по умолчанию возвращать данные за текущий день, в контроллере сервиса weather еще должен быть endpoint, в котором можно указать город в котором мы хотим получить выгрузку по погоде. 
- оба сервиса и оба контроллера должны быть логически разнесены по соответствующим java пакетам. 
- создать сервис predict, который забирает данные двух других сервисов за последние 30 дней, и на основе них строит корреляцию для вычисления предположительной стоимости валют за завтрашний день. Алгоритмы можете брать любой на ваше усмотрение – регресс, k ближайших соседей или еще что либо другое. Например, реализацию регрессии есть в библиотеке для Java apache math3 - https://commons.apache.org/proper/commons-math/javadocs/api-3.3/org/apache/commons/math3/stat/regression/SimpleRegression.html , а k ближайших есть в apache spark. Либо можете сами написать реализацию алгоритма. 
- весь код следует разделять на соответствующие слои, соблюдать принципы solid
