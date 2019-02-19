Если ты не используешь Chromebook, можешь пропустить эту секцию. 
В противном случае процесс установки будет немного другим, и тебе нужно будет пройти только эту инструкцию по установке.


### Облачная IDE (PaizaCloud Cloud IDE, AWS Cloud9)

Облачная IDE — это инструмент, который предоставляет тебе редактор кода и доступ к компьютеру, 
запущенному в интернете. На этом удалённом компьютере ты можешь устанавливать, создавать и запускать программы.
На время прохождения этого руководства облачная IDE будет вести себя как _локальный компьютер_.
Ты будешь так же, как и другие участницы с OS X, Ubuntu или Windows, выполнять команды в командной строке,
но она будет подключена к компьютеру облачной IDE, который находится где-то в другом месте.

Ниже ты увидишь инструкции для настройки облачных IDE (PaizaCloud Cloud IDE, AWS Cloud9).
Ты можешь выбрать одну из них и выполнить соответствующие действия.

#### PaizaCloud Cloud IDE

1. Перейди на сайт [PaizaCloud Cloud IDE](https://paiza.cloud/)
2. Войди в свой аккаунт
3. Нажми _New Server_
4. Нажми кнопку Terminal (в левой части окна)

Теперь ты должна увидеть интерфейс с боковой панелью, кнопки расположены слева. 
Нажми кнопку "Terminal", чтобы открыть командную строку. Ты увидишь приглашение командной строки:

{% filename %}Terminal{% endfilename %}
```
$
```

Командная строка в PaizaCloud Cloud IDE готова к твоим командам. 
Ты можешь изменить размер этого окна, чтобы сделать его немного больше.


#### AWS Cloud9

1. Перейди на сайт [AWS Cloud9](https://aws.amazon.com/cloud9/)
2. Войди в свой аккаунт
3. Нажми _Create Environment_

Теперь ты должна увидеть интерфейс с боковой панелью, большим основным окном с текстом, 
а также маленьким окошком снизу, которое выглядит как-то так:

{% filename %}bash{% endfilename %}
```
yourusername:~/workspace $
```

Эта область внизу и есть твоя командная строка. Ты можешь использовать её, чтобы давать команды 
удалённому компьютеру в Cloud9. Ты можешь изменить размер этого окна, чтобы сделать его немного больше.


### Виртуальное окружение

Виртуальное окружение (его также называют virtualenv) похоже на личную коробку, куда мы можем 
сложить полезный код для проекта, над которым работаем. Виртуальные окружения нужны нам, чтобы держать отдельно
разные кусочки кода для наших проектов — так они не перемешаются между разными проектами.

В твоей командной строке в нижней части интерфейса Cloud 9 запусти следующие команды:

{% filename %}Cloud 9{% endfilename %}
```
sudo apt update
sudo apt install python3.6-venv
```

Если они не сработают, попроси своего тренера помочь.

Далее запусти:

{% filename %}Cloud 9{% endfilename %}
```
mkdir djangogirls
cd djangogirls
python3.6 -mvenv myvenv
source myvenv/bin/activate
pip install django~={{ book.django_version }}
```

(обрати внимание, что в последней строчке мы используем сочетание тильды и знака равенства: `~=`).

### GitHub

Создай аккаунт на [GitHub](https://github.com).

### PythonAnywhere

Руководство Django Girls включает в себя раздел «Публикация». Этим словом описывается процесс,
когда ты переносишь код, запускающий твоё новое веб-приложение, на публично доступный компьютер 
(он называется сервер), чтобы другие люди могли видеть результаты твоей работы.

Если ты проходишь это руководство на Chromebook, этап публикации может выглядеть немного нетипично, так как
для разработки мы уже используем удалённый компьютер где-то в интернете (а, например, не мощности своего ноутбука).
Тем не менее, будет полезно пройти раздел «Публикация», ведь мы можем рассматривать наше рабочее пространство 
в Cloud9 или PaizaCloud как место для незавершенной работы, а PythonAnywhere как место
для демонстрации законченных дел.

Так что тебе нужно будет завести аккаунт на сайте [www.pythonanywhere.com](https://www.pythonanywhere.com).