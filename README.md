# Удаления записей «критического состояния» диска


### Описание

Если DSM решит, что диск является критическим, DSM сохранит состояние «критическое» в базе данных и не позволит вам снова использовать этот диск. Если вы запустите расширенный тест SMART на диске на компьютере и он покажет, что с диском все в порядке, DSM все равно откажет вам в использовании диска. Вы можете использовать этот сценарий на Synology для удаления записей «критического состояния» этого диска из базы данных DSM. После этого DSM позволит вам снова использовать диск.

**ПРИМЕЧАНИЕ** Сценарий не исправляет неисправный диск.

## Скачать сценарий

1. [Загрузите исходный код последней версии .zip](https://github.com/007revad/Synology_clear_drive_error/releases)
2. Сохраните загруженный zip-файл в папку на Synology.
3. Разархивируйте zip-файл.

## Как запустить скрипт

### Запускаем скрипт через SSH

[Как включить SSH и войти в DSM через SSH](https://kb.synology.com/en-global/DSM/tutorial/How_to_login_to_DSM_with_root_permission_via_SSH_Telnet)

Запустите скрипт:

```bash
sudo -s /volume1/scripts/syno_clear_drive_error.sh
```

> *Примечание.** <br>
> Replace /volume1/scripts/ путем к расположению сценария.

### После запуска скрипта

Если диспетчер хранилища уже открыт, закройте его, а затем откройте снова.

## Скриншоты

<p align="center">Сброс критической ошибки для 2 дисков</p>
<p align="center"><img src="/images/script-4.png"></p>

