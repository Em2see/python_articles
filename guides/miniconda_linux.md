# Установка на Linux

1. Загрузите установщик:
- [Miniconda для Linux](https://docs.conda.io/en/latest/miniconda.html#linux-installers)
- [Anaconda для Linux](https://www.anaconda.com/download/)

2. [Проверьте хэши вашего установщика.](https://docs.conda.io/projects/conda/en/latest/user-guide/install/download.html#hash-verification)

3. В окне вашего терминала запустите:
- Miniconda:
```sh
bash Miniconda3-latest-Linux-x86_64.sh
```
- Anaconda:
```sh
bash Anaconda-latest-Linux-x86_64.sh
```
4. Следуйте инструкциям на экранах установщика.
Если вы не уверены в каких-либо настройках, примите значения по умолчанию. Вы можете изменить их позже.
5. Чтобы изменения вступили в силу, закройте, а затем снова откройте окно вашего терминала.
6. Протестируйте свою установку. В окне вашего терминала или командной строке Anaconda запустите команду `conda list`
Появится список установленных пакетов, если он был установлен правильно.

## Использование с оболочкой "fish shell"
Чтобы использовать conda с "fish shell", выполните в своем терминале следующее:
`conda init fish`
## Установка в режиме "silent mode"
Смотрите инструкции по установке данного режима [для macOS.](https://docs.conda.io/projects/conda/en/latest/user-guide/install/macos.html#install-macos-silent)
## Обновление Anaconda или Miniconda
1. Откройте окно терминала.
2. Запустите `conda update conda`.

## Удаление Anaconda или Miniconda
1. Откройте окно терминала.
2. Удалите весь установочный каталог Miniconda с помощью:
```sh
rm -rf ~/miniconda
```
3. ПО УСМОТРЕНИЮ: Отредактируйте `~/.bash_profile`, чтобы удалить каталог Miniconda из вашей переменной окружения PATH. 
4. ПО УСМОТРЕНИЮ: Удалите следующие скрытые файлы и папки, которые, возможно, были созданы в домашнем каталоге:
- `.condarc` file
- `.conda` directory
- `.continuum`directory
Запустив:
```sh
rm -rf ~/.condarc ~/.conda ~/.continuum
```
