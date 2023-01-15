# Установка из PyPI
Наиболее распространенным использованием  [pip](https://packaging.python.org/en/latest/key_projects/#pip) является установка из  [Python Package Index](https://packaging.python.org/en/latest/glossary/#term-Python-Package-Index-PyPI) с использованием  [requirement specifier](https://packaging.python.org/en/latest/glossary/#term-Requirement-Specifier), который представляет собой перечень необходимых к установке пакетов. Вообще говоря, он состоит из имени проекта, за которым следует необязательный   [спецификатор версии](https://packaging.python.org/en/latest/glossary/#term-Version-Specifier). **PEP 440** содержит полную спецификацию поддерживаемых в настоящее время спецификаторов. Ниже приведены некоторые примеры.

- Для установки последней версии “SomeProject”:

**Unix/macOS**
```sh
 python3 -m pip install "SomeProject"
```
**Windows**
```sh
 py -m pip install "SomeProject"
```
- Для установки определенной версии “SomeProject”:

**Unix/macOS**
```sh
 python3 -m pip install "SomeProject==1.4"
```
**Windows**
```sh
py -m pip install "SomeProject==1.4"
```
- Для установки более ранней или наоборот более поздней версии

**Unix/macOS**
```sh
python3 -m pip install "SomeProject>=1,<2"
```
**Windows**
```sh
py -m pip install "SomeProject>=1,<2"
```
- Чтобы установить версию, которая “совместима” с определенной версией:
 
**Unix/macOS**
```sh
python3 -m pip install "SomeProject~=1.4.2"
```
**Windows**
```sh
py -m pip install "SomeProject~=1.4.2"
```
В данном случае это означает установку любой версии “==1.4.*”, которая также является “>=1.4.2”.

# Исходный код vs Wheels
[pip](https://packaging.python.org/en/latest/key_projects/#pip) можно устанавливать либо из исходных дистрибутивов  [(Source Distributions (sdist))](https://packaging.python.org/en/latest/glossary/#term-Source-Distribution-or-sdist), либо из [Wheels](https://packaging.python.org/en/latest/glossary/#term-Wheel), но если в PyPI присутствуют оба, pip предпочтет wheel. Вы можете переопределить поведение pip по умолчанию, например, используя его опцию  [–no-binary](https://pip.pypa.io/en/latest/cli/pip_install/#install-no-binary).

[Wheels](https://packaging.python.org/en/latest/glossary/#term-Wheel) - это предварительно созданный формат дистрибутива, который обеспечивает более быструю установку по сравнению с исходными дистрибутивами [(sdist)](https://packaging.python.org/en/latest/glossary/#term-Source-Distribution-or-sdist), особенно когда проект содержит скомпилированные расширения.

Если pip не найдет wheel для установки, он будет локально создавать wheel и кэшировать его для будущих установок, вместо того, чтобы перестраивать исходный дистрибутив в будущем.

# Обновление пакетов
Обновите уже установленный какой-либо проект `SomeProject` до последней версии из PyPI.

**Unix/macOS**
```sh
python3 -m pip install --upgrade SomeProject
```
**Windows**
```sh
py -m pip install --upgrade SomeProject
```
# Файлы требований
Установите перечень требований, указанных в файле требований [(Requirements File)](https://pip.pypa.io/en/latest/user_guide/#requirements-files).

**Unix/macOS**
```sh
python3 -m pip install -r requirements.txt
```
**Windows**
```sh
py -m pip install -r requirements.txt
```