# Установка на Linux
> Используете Anaconda в коммерческих целях? Возможно, вам потребуется приобрести расширенную лицензию, например [Anaconda Professional](https://docs.anaconda.com/anaconda-professional), [Anaconda Server](https://team-docs.anaconda.com/en/latest/) или [Anaconda Enterprise](https://enterprise-docs.anaconda.com/en/latest/). Если вы уже приобрели Professional, пожалуйста, после завершения установки перейдите к разделу Аутентификации Anaconda Professional.
Если вы еще не приобрели Anaconda Professional, то посетите [https://anaconda.cloud/register](https://anaconda.cloud/register/)

## Предпосылки
Чтобы использовать пакеты GUI с Linux, вам необходимо установить следующие расширения для Qt:
|ОС семейства Linux | Необходимые расширения| 
|-------------------|:---------------------:|
|Debian|  `apt-get` `install` `libgl1-mesa-glx` `libegl1-mesa` `libxrandr2` `libxss1` `libxcursor1` `libxcomposite1` `libasound2`` libxi6` `libxtst6` | 
| RedHat| `yum` `install` `libXcomposite` `libXcursor` `libXi` `libXtst` `libXrandr` `alsa-lib` `mesa-libEGL` `libXdamage` `mesa-libGL` `libXScrnSaver` |  
| ArchLinux| `pacman` `-Sy` `libxau` `libxi` `libxss` `libxtst` `libxcursor` `libxcomposite` `libxdamage` `libxfixes` `libxrandr` `libxrender` `mesa-libgl`  `alsa-lib` `libglvnd` | 
| OpenSuse/SLES   |`zypper` `install` `libXcomposite1` `libXi6` `libXext6` `libXau6` `libX11-6` `libXrandr2` `libXrender1` `libXss1` `libXtst6` `libXdamage1` `libXcursor1` `libxcb1` `libasound2`  `libX11-xcb1` `Mesa-libGL1` `Mesa-libEGL1` | 
| Gentoo | `emerge` `x11-libs/libXau` `x11-libs/libxcb` `x11-libs/libX11` `x11-libs/libXext` `x11-libs/libXfixes` `x11-libs/libXrender` `x11-libs/libXi` `x11-libs/libXcomposite` `x11-libs/libXrandr` `x11-libs/libXcursor` `x11-libs/libXdamage` `x11-libs/libXScrnSaver` `x11-libs/libXtst` `media-libs/alsa-lib` `media-libs/mesa` | 

## Установка
Для x86 систем.
1. Загрузите в браузере установщик [Anaconda для Linux](https://www.anaconda.com/download/#linux).
2. Найдите “терминал” в ваших приложениях и нажмите, чтобы открыть.
3. (Рекомендуется) Проверьте целостность данных установщика с помощью [SHA-256](https://docs.anaconda.com/anaconda/install/hashes/). Дополнительные сведения о проверке хэша см. в разделе  [Проверка криптографического хэша](https://conda.io/projects/conda/en/latest/user-guide/install/download.html#cryptographic-hash-verification).
В терминале выполните следующее:
```sh
shasum -a 256 /PATH/FILENAME
# Replace /PATH/FILENAME with your installation's path and filename.
```
4. Установите для Python 3.7 или 2.7 в терминале:

- Для Python 3.7 введите следующее:
```sh
# Include the bash command regardless of whether or not you are using the Bash shell
bash ~/Downloads/Anaconda3-2020.05-Linux-x86_64.sh
# Replace ~/Downloads with your actual path
# Replace the .sh file name with the name of the file you downloaded
```
- Для Python 2.7 введите следующее:
```sh
# Include the bash command regardless of whether or not you are using the Bash shell
bash ~/Downloads/Anaconda2-2019.10-MacOSX-x86_64.sh
# Replace ~/Downloads with your actual path
# Replace the .sh file name with the name of the file you downloaded
```
5. Нажмите Enter, чтобы ознакомиться с лицензионным соглашением. Затем нажмите и удерживайте клавишу Enter для прокрутки.
6. Введите “да”, чтобы согласиться с лицензионным соглашением.
7. Используйте Enter, чтобы выбрать место установки по умолчанию, используйте CTRL+C, чтобы отменить установку, или введите другой путь к файлу, чтобы указать альтернативный каталог установки. Если вы принимаете расположение установки по умолчанию, программа установки отобразит `PREFIX=/home/<USER>/anaconda<2/3>` и продолжит установку. Это может занять несколько минут.
> Anaconda рекомендует вам выбрать место установки по умолчанию. Не выбирайте путь как `/usr` для установки Anaconda/Miniconda.
8. Программа установки предложит вам выбрать, следует ли инициализировать дистрибутив Anaconda, запустив `conda init`. Анаконда рекомендует ввести “yes”. 
Если вы введете “no”, то conda вообще не будет изменять ваши shell scripts. Чтобы выполнить инициализацию после завершения процесса установки, сначала запустите `source [PATH TO CONDA]/bin/activate`, а затем запустите `conda init`. ( См. [раздел Часто задаваемые вопросы](https://docs.anaconda.com/anaconda/user-guide/faq/#distribution-faq-linux-path))
9. Программа установки завершит работу и отобразит: “Thank you for installing Anaconda<2/3>!”
10. По желанию: Установщик описывает "партнерство" между Anaconda и JetBrains и предоставляет ссылку для установки Dataspell для Anaconda по адресу [https://www.anaconda.com/dataspell](https://www.anaconda.com/dataspell) .
11. Закройте и снова откройте окно терминала, чтобы установка вступила в силу, или введите команду `source ~/.bashrc`, чтобы обновить терминал.
12. Вы также можете контролировать, активируется ли базовая среда вашей оболочки при каждом ее открытии.
```sh
# The base environment is activated by default
conda config --set auto_activate_base True

# The base environment is not activated by default
conda config --set auto_activate_base False

# The above commands only work if conda init has been run first
# conda init is available in conda versions 4.6.12 and later
```
13. [Проверьте свою установку.](https://docs.anaconda.com/anaconda/install/verify-install/)
> Если вы устанавливаете несколько версий Anaconda, система по умолчанию использует самую последнюю версию, если вы не изменили путь установки по умолчанию.

## Проблемы с установкой?
Смотрите раздел [Устранение неполадок.](https://docs.anaconda.com/anaconda/user-guide/troubleshooting/)