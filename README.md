<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="dns-prefetch" href="//fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css?family=Nunito" rel="stylesheet">

    <link rel="stylesheet" href="/build/assets/app-c9c92c89.css">

    <link rel="preload" as="style" href="https://logisticsbtl.kz/build/assets/app-c9c92c89.css" />
    <link rel="stylesheet" href="https://logisticsbtl.kz/build/assets/app-c9c92c89.css" />
    <title>Регистрация</title>
</head>
<body class="bg-gray-200">
    <div class="max-w-2xl mx-auto">
        <main class="py-4">
            <div class="border card p-10">
                <form id="registrationForm" method="POST" action="Войти.html">
                    <div class="col-md-7">
                        <label class="label" for="login">Телефон</label><br>
                        <input type="tel" id="login" class="w-full border-blue-0" name="login" value="" placeholder="87071112233" />
                        <div id="loginError" class="text-red-500 text-sm"></div><br>
                    </div>
                    <div class="col-md-6">
                        <label class="label" for="name">Имя</label><br>
                        <input 
                            type="text" 
                            id="name" 
                            class="w-full border-blue-200" 
                            name="name" 
                            value="" 
                            placeholder="" 
                        />
                        <div id="nameError" class="text-red-500 text-sm"></div><br>
                    </div>
                    <div class="col-md-6">
                        <label class="label" for="surname">Фамилия на английском</label><br>
                        <input
                            type="text"
                            id="surname"
                            class="w-full border-blue-200"
                            name="surname"
                            value=""
                            placeholder=""
                        />
                        <div id="surnameError" class="text-red-500 text-sm"></div><br>
                    </div>
                    <div class="col-md-6">
                        <label class="label" for="">Пароль</label><br>
                        <input type="password" id="password" class="w-full border-blue-350" value="" placeholder="Придумайте пароль" />
                        <div id="passwordError" class="text-red-500 text-sm"></div><br>
                    </div>
                    <button type="submit" class="btn btn-primary" formnovalidate>Регистрация</button>
                    <br>
                    <hr class="my-4">
                    Вы уже зарегистрированы? <a class="link" href="Войти.html">Войти</a>
                </form>
            </div>
        </main>
    </div>

    <script>
        document.getElementById("registrationForm").addEventListener("submit", function(event) {
            var loginValue = document.getElementById("login").value;
            var nameValue = document.getElementById("name").value;
            var surnameValue = document.getElementById("surname").value;
            var passwordValue = document.getElementById("password").value;

            document.getElementById("loginError").innerHTML = loginValue ? "" : "Введите номер телефона";
            document.getElementById("nameError").innerHTML = nameValue ? "" : "Введите имя";
            document.getElementById("surnameError").innerHTML = surnameValue ? "" : "Введите фамилию";
            document.getElementById("passwordError").innerHTML = passwordValue ? "" : "Придумайте пароль";

            if (!loginValue || !nameValue || !surnameValue || !passwordValue) {
                event.preventDefault(); // Prevent form submission if fields are not filled
            }
        });
    </script>
</body>
</html>
