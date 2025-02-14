# Otus.Lesson24.PAM
1. Запретить всем пользователям кроме группы admin логин в выходные (суббота и воскресенье), без учета праздников  
  
После запуска плейбука будет предложено ввести пароль для новых пользователей.  
По завершении работы плейбука поменяем время на VM  
  
root@deb12:~# date 021512302025.00  
Сб 15 фев 2025 12:30:00 MSK  
  
Попробуем подключиться от имени пользователя otus:  
```
[C:\~]$ ssh otus@192.168.57.10

Connecting to 192.168.57.10:22...
Connection established.
To escape to local shell, press Ctrl+Alt+].
Connection closing...Socket close.

Connection closed by foreign host.

Disconnected from remote host(192.168.57.10:22) at 11:40:02.
```
Теперь подключимся пользователем otusadm:  
```
[C:\~]$ ssh otusadm@192.168.57.10


Connecting to 192.168.57.10:22...
Connection established.
To escape to local shell, press Ctrl+Alt+].

Linux deb12 6.1.0-18-amd64 #1 SMP PREEMPT_DYNAMIC Debian 6.1.76-1 (2024-02-01) x86_64

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Sat Feb 15 12:30:15 2025 from 10.1.1.21
otusadm@deb12:~$ date
Сб 15 фев 2025 12:30:41 MSK
```
Мы успешно авторизовались на VM.  
