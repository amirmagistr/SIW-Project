<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instagram Database Project</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            padding: 20px;
        }
        .container {
            max-width: 800px;
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            margin: auto;
        }
        img {
            max-width: 100%;
            height: auto;
            border: 1px solid #ddd;
            margin-bottom: 20px;
        }
        h1, h2 {
            color: #333;
        }
        p {
            font-size: 18px;
            color: #555;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Instagram Database Project</h1>
        <p><strong>Имя студента:</strong> Амир</p>
        <p><strong>Преподаватель:</strong> Танжырыкова Меруерт</p>
        <p><strong>Дата:</strong> Понедельник, 14 октября 2024 года</p>
        <p><strong>Курс:</strong> 2-й курс</p>

        <h2>Создание таблиц с помощью CREATE TABLE</h2>
        <p>На скриншоте ниже показан код создания таблиц для проекта Instagram database. Он включает таблицы Users, Posts, Comments, Followers, и Likes:</p>
        <img src="код1.png" alt="Код создания таблиц">
        
        <p>Далее подтверждение успешного выполнения запроса на создание таблиц:</p>
        <img src="пр2.png" alt="Результат выполнения запроса">

        <p>Список созданных таблиц в базе данных:</p>
        <img src="пр1.png" alt="Список таблиц">
    </div>

    <div class="container">
        <h2>Использование ALTER TABLE для создания первичных ключей</h2>
        <p>На скриншоте ниже показан код, в котором используется команда <code>ALTER TABLE</code> для добавления первичных ключей в таблицы Users, Posts, Comments, Followers и Likes:</p>
        <img src="код2.png" alt="Код создания первичных ключей">
        
        <p>Запрос был успешно выполнен, как показано на следующем скриншоте:</p>
        <img src="пр3.png" alt="Результат выполнения команды ALTER TABLE"><br>
    </div>

    <div class="container">
        <h2>Создание внешних ключей с помощью ALTER TABLE</h2>
        <p>На скриншоте ниже показан код с использованием команды <code>ALTER TABLE</code> для добавления внешних ключей в таблицы:</p>
        <img src="код3.png" alt="Код создания внешних ключей">
        
        <p>Запрос был успешно выполнен, как показано на следующем скриншоте:</p>
        <img src="пр4.png" alt="Результат выполнения команды ALTER TABLE"><br>
    </div>

    <div class="container">
        <h2>ER Diagram for Instagram Database</h2>
        <img src="erdiagram.png" alt="ER Diagram">
        
        <h3>Связи между таблицами:</h3>
        <ul>
            <li><strong>Users и Posts:</strong> u_id в Posts ссылается на u_id в Users (отношение "один ко многим"). Один пользователь может создать много постов.</li>
            <li><strong>Posts и Comments:</strong> post_id в Comments ссылается на post_id в Posts (отношение "один ко многим"). Один пост может иметь много комментариев.</li>
            <li><strong>Users и Followers:</strong> u_id и follower_id в Followers ссылаются на u_id в Users (отношение "многие ко многим"). Один пользователь может подписываться на других и иметь подписчиков.</li>
            <li><strong>Posts и Likes:</strong> post_id в Likes ссылается на post_id в Posts (один пост может иметь много лайков), а u_id в Likes ссылается на u_id в Users (один пользователь может поставить много лайков).</li>
        </ul>
    </div>

    <div class="container">
        <h2>Удаление таблицы Likes с помощью команды DROP TABLE</h2>
        <p>На скриншоте ниже показан код с использованием команды <code>DROP TABLE</code> для удаления таблицы <code>Likes</code>:</p>
        <img src="drop.png" alt="Код удаления таблицы Likes">
        
        <p>Запрос был успешно выполнен, как показано на следующем скриншоте:</p>
        <img src="dropr.png" alt="Результат выполнения команды DROP TABLE">
        <p>И вот визуальный результат:</p>
        <img src="withoutlike.png" alt="Визуальный результат">
    </div>

    <div class="container">
    <h2>Добавление записей в таблицы</h2>
    <p>На скриншоте ниже показан код для вставки данных в таблицы Users, Posts, Comments и Followers с помощью INSERT:</p>
    <img src="insertкод.png" alt="Код добавления записей в таблицы">
    
    <p>Запросы были успешно выполнены, как показано на следующем скриншоте:</p>
    <img src="insertпр.png" alt="Результат выполнения команды INSERT">
</div>

<div class="container">
    <h2>UPDATE данных в таблице Posts</h2>
    <p>На скриншоте ниже показан код для обновления количества лайков у поста с <code>post_id = 1</code>(было 67, стало 68) и выборка данных после обновления:</p>
    <img src="upcode.png" alt="Код для обновления и выборки данных">
    
    <p>Запрос на обновление был успешно выполнен, как показано на следующем скриншоте:</p>
    <img src="updater.png" alt="Результат выполнения команды UPDATE">
    
    <p>Результаты после выполнения команды SELECT, показывающие изменения в базе данных:</p>
    <img src="updr.png" alt="Результаты SELECT после UPDATE"><br>
</div>

<div class="container">
    <h2>Просмотр комментария с comment_id = 2</h2>
    <p>На скриншоте ниже показан SQL-запрос для выборки комментария с <code>comment_id = 2</code>:</p>
    <img src="comment2.png" alt="Запрос на выборку комментария с comment_id = 2">
    
    <p>Результат выполнения запроса, показывающий информацию о комментарии:</p>
    <img src="comment2c.png" alt="Результат SELECT для comment_id = 2">
    
</div>

<div class="container">
    <h2>Удаление комментария с помощью DELETE</h2>
    <p>На скриншоте ниже показан SQL-запрос для удаления комментария с <code>comment_id = 2</code>:</p>
    <img src="delete1.png" alt="Запрос на удаление комментария с comment_id = 2">
    
    <p>Запрос был успешно выполнен, как показано на следующем скриншоте:</p>
    <img src="deleter.png" alt="Результат выполнения команды DELETE">
    
    <p>Результат после выполнения команды DELETE, где комментарий с <code>comment_id = 2</code> был удалён:</p>
    <img src="deleter2.png" alt="Результаты после удаления комментария"><br>
</div>

<div class="container">
    <h2>Исходное расположение данных в таблице Users</h2>
    <p>На скриншоте ниже показан результат запроса для просмотра всех записей в таблице <code>Users</code>:</p>
    <img src="selectres.png" alt="Результат SELECT для таблицы Users">
</div>

<div class="container">
    <h2>Сортировка пользователей по дате регистрации с помощью ORDER BY</h2>
    <p>На скриншоте ниже показан результат сортировки пользователей в таблице <code>Users</code> по столбцу <code>regdate</code> в порядке убывания:</p>
    <img src="regdate.png" alt="Результат сортировки по regdate DESC"><br>
</div>

<div class="container">
    <h2>Подсчет количества постов для каждого пользователя с помощью COUNT</h2>
    <p>На скриншоте ниже показан результат выполнения запроса, который подсчитывает количество постов, созданных каждым пользователем, используя <code>GROUP BY</code>:</p>
    <img src="countr.png" alt="Результат подсчета количества постов для каждого пользователя"><br>
    
    <a href="project SUBD.html">Вернуться на главную</a>
</div>
</body>
</html>
