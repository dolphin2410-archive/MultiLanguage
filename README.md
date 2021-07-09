# MultiLanguage

### Introduction
MultiLanguage is an application that allows users to setup an easy json database for multiple language suuport in their application. It programmed with python without any dependencies, 
so you can just execute this program only with the `MultiLanguage.py` file

### Usage
#### Using as a library
If you are a python developer, install this as a depdency by executing
```shell
pip install MultiLanguage
```
```python
from MultiLanguage.MultiLanguage import *


LanguageAdder.add("database.json", [("english", "pumpkin"), ("korean": "호박")])
LanguageAccessorFactory.create("database.json", "pumpkin").get("korean") # 호박
```

#### Using as a program
**Notice**: This requires at least python 3.9 to be installed in your computer.

1. To use this as an application, copy the file from `MultiLanguage/MultiLanguage.py` and place it to your project root.
2. To add words to the database, you will have to pass a parameter <[language]> and <value in [language]>. Here is an example.
```shell
python MultiLanguage.py english pumpkin korean 호박
```
3. If you have spaces in <[language]> or <value in [language]>, wrap it with double quotes.
```shell
python MultiLanguage.py "en us" pumpkin "ko" 호박 "vi" "quả bí ngô"
```
4. This will modify the json file in format like
```json
[
  {"english": "pumpkin", "korean": "호박"},
  {"en us": "pumpkin", "ko": "호박", "vi": "quả bí ngô"}
]
```
