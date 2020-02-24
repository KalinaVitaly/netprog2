
# Задача

Разработать FTP-клиент с интерфейсом командной строки.

## Требования

1. Программа устанавливает управляющее TCP-соединение с сервером по адресу
   127.0.0.1 на порте 21. Все FTP-запросы передаются через управляющее
   соединение.

2. Программа считывает из потока ввода команды вида **\<ftp_command\>
   \<argument\>**, где \<argument\> является опциональным. Для каждой команды
   пользователя программа формирует FTP-запрос, отправляет его серверу,
   дожидается ответа и выводит результат в терминал.

3. Программа поддерживает FTP-команды USER, PASS, PASV, QUIT.

4. Программа выполняет скачивание файла с сервера в текущий каталог по команде
   RETR. Скачивание производится в пассивном режиме. Для этого программа
   автоматически отправляет FTP-команду PASV, узнает номер порта для передачи
   данных, открывает соединение на этом порте и отправляет FTP-команду RETR.
   После считывания всех данных дополнительное соединение закрывается.

5. При запуске программа принимает 2 опциональных аргумента командной строки с
   именем и паролем. Если эти аргументы введены, программа автоматически
   выполняет аутентификацию на сервере.

# Упрощенная задача

Исключить скачивание файла (запрос RETR).