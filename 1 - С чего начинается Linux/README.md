### Текст задания
> 1. Запустить ВМ c Ubuntu. 
> 2. Обновить ядро ОС на новейшую стабильную версию из mainline-репозитория.
> 3. Оформить отчет в README-файле в GitHub-репозитории.
### Основные команды
```bash
# Проверка версии ядра
uname -r
# подготовка к установке новой версии ядра с помощью mainline
sudo add-apt-repository ppa:cappelikan/ppa
sudo apt update
sudo apt install mainline 
mainline list
# устранение выявленной в процессе зависимости и установка ядра версии 6.10.14
sudo apt install policykit-1
sudo mainline install 6.10.14
# проверка версии ядра
ls /boot/vmlinuz-*
# выполнение завершающих процедур
sudo update-grub
sudo reboot
# финальная проверка версии ядра
uname -r
```
### Заметки и скриншоты
Более полный текст, с выводом некоторых команд - в заметке `Выполнение задания.md`
