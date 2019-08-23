## Дополнительные настройки ANACONDA
conda install -c conda-forge keras 
conda install -c conda-forge opencv

## Если при импорте ( import cv2 ) возникает ошибка "DLL Load failed"
pip install opencv-contrib-python

# detect_barcode.py
pip install imutils

## Код по этим статьям
https://habr.com/ru/company/enterra/blog/244163/
https://www.pyimagesearch.com/2014/11/24/detecting-barcodes-images-python-opencv/

## Еще статьи
https://robotclass.ru/tutorials/opencv-python-find-contours/
https://reference.wolfram.com/language/ref/BarcodeRecognize.html
https://www.learnopencv.com/barcode-and-qr-code-scanner-using-zbar-and-opencv/

## Алгоритмы выделения контуров изображений (Робертс, Превитт. Собель)
https://habr.com/ru/post/114452/

# 2. zbar-test.py
## Дополнительные настройки ANACONDA
pip install pyzbar

## Еще статьи
https://www.learnopencv.com/barcode-and-qr-code-scanner-using-zbar-and-opencv/
https://github.com/spmallick/learnopencv

# 3. ImageAI
https://medium.com/nuances-of-programming/%D0%BE%D0%B1%D0%BD%D0%B0%D1%80%D1%83%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BE%D0%B1%D1%8A%D0%B5%D0%BA%D1%82%D0%BE%D0%B2-%D1%81-10-%D1%81%D1%82%D1%80%D0%BE%D1%87%D0%BA%D0%B0%D0%BC%D0%B8-%D0%BA%D0%BE%D0%B4%D0%B0-953bd0e22a2
https://proglib.io/p/deep-learning-advice/
http://imageai.org/

# 4. Пример создания Envirovment in Conda
One solution could be creating a conda environment:
conda create -n keras python=3.5

Now activate it:
conda activate keras

and install keras:
(keras)$ conda install keras

Try if it works:
(keras)$ python
>>> import keras


# об Anaconda
Conda - менеджер пакетов питона, позволяет устанавливать уже скомпилированные пакеты (может работать и в режиме компиляции пакетов перед установкой). Также Conda - менеджер окружений системы, позволяет создавать окружения с разными версиями чего угодно (библиотеки C, низкоуровневые библиотеки и т.д.).
Conda бывает в двух версиях:

    Анаконда - более 150 предустановленных пакетов (около 3 Гб) + более 250 пакетов, готовых к установке командой conda install package_name
    Миниконда - более 400 пакетов, готовых к установке командой conda install package_name

и Анаконда и Миниконда включают:

    conda
    интерпретатор питона
    pip

Команды Conda:

    conda search package_name - поиск пакета через conda
    conda install package_name - установка пакета через conda
    conda install - установка всего стандартного набора пакетов - более 150, около 3 Гб
    conda list - список установленных пакетов
    conda update conda - обновление conda
    conda clean -t - удаление кеша - архивов .tar.bz2, которые могут занимать много места и не нужны


