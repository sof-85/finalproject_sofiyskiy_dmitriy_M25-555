# project1_sofiyskiy_dmitriy_M25-555
Valutatrade_hub

Описание проекта

Программа отслеживания и симуляции торговли валютами представляет собой комплексную платформу, которая позволяет пользователям регистрироваться, управлять своим виртуальным портфелем фиатных и криптовалют, совершать сделки по покупке/продаже, а также отслеживать актуальные курсы в реальном времени. 

Установка

Чтобы установить программу выполните следующие шаги:

Шаг 1: Клонируйте репозиторий
git clone https://github.com/sof-85/finalproject_sofiyskiy_dmitriy_M25-555.git
cd project1_sofiyskiy_dmitriy_M25-555

Шаг 2: Установите Poetry
Проверьте наличие poetry на вашей машине командой:
poetry --version
Если команда выдает ошибку, установите Poetry согласно официальной инструкции на сайте проекта: https://python-poetry.org/docs/#installation. 

Шаг 3: Создайте виртуальное окружение и установите зависимости
Создаем виртуальное окружение и устанавливаем требуемые пакеты с помощью команды:
poetry install

Это создаст виртуальное окружение и установит все необходимые библиотеки.

Запуск программы

Для запуска программы используйте Makefile.
Запустить программу можно следующим образом:
make project
poetry run project

Структура проекта

finalproject_<фамилия>_<группа>/
│  
├── data/
│    ├── users.json          
│    ├── portfolios.json       
│    └── rates.json            
├── valutatrade_hub/
│    ├── __init__.py
│    ├── logging_config.py         
│    ├── decorators.py             
│    ├── core/
│    │    ├── __init__.py
│    │    ├── currencies.py         
│    │    ├── exceptions.py         
│    │    ├── models.py             
│    │    ├── usecases.py           
│    │    └── utils.py              
│    ├── infra/
│    │    ├─ __init__.py
│    │    ├── settings.py           
│    │    └── database.py           
│    └── cli/
│         ├─ __init__.py
│         └─ interface.py     
│
├── main.py
├── Makefile
├── poetry.lock
├── pyproject.toml
├── README.md
└── .gitignore               

Работа с программой

Работа с программой происходит путем интерактивного взаимодействия и позволяет пользователю осуществлять регистрацию, авторизацию в программе, покупать, продавать, обновлять курсы валют из внешних источников, а также просматривать состояние своего кошелька

Основные команды:

register --username <name> --password <pass> - Регистрация пользователя
login    --username <name> --password <pass> - Авторизация пользователя
logout                                       - Смена пользователя
show-portfolio [--base <CODE>]               - Состояние кошелька
buy      --currency <CODE> --amount <num>    - Покупка валюты
sell     --currency <CODE> --amount <num>    - Продажа валюты
get-rate --from <CODE> --to <CODE>           - Получить курс (из базы)
update-rates [--source <name>]               - Обновить курсы валют 
show-rates   [--currency <CODE>] [--top <N>] - Показать курс валюты
exit                                         - Завершить работу
help                                         - Помощь



Пример работы программы:
https://asciinema.org/a/3SQMn3SvT6jT7uTU


