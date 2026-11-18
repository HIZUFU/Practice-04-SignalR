# Практическая работа №4. SignalR

Добавлены датчики, имитатор показаний и мониторинг без перезагрузки. В хабе есть JoinSite и SubmitReading; сервер отправляет снимок состояния, новые замеры, подтверждения, тревоги и количество подключений. Замеры сохраняются в БД. Мониторинг доступен после входа. Поддерживаются роли и CRUD.

Сохранены каталог участков и оборудования, REST API, MVC-клиент, SQLite, Swagger, регистрация, вход и роли User/Admin.

Нужен .NET 10 SDK. В первом терминале:

```powershell
dotnet restore
$env:Admin__Password = 'StudyAdmin123!'
dotnet run --project ProductCatalogApp.Api --launch-profile http
```

Во втором терминале:

```powershell
dotnet run --project ProductCatalogApp.Client --launch-profile http
```

Клиент: http://localhost:5034. Swagger: http://localhost:5100/swagger. Администратор: admin, пароль из команды выше. Зарегистрированные пользователи получают роль User.
Мониторинг: http://localhost:5034/Monitoring.

