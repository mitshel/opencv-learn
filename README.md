# Книги
https://vk.com/topic-51126445_32505707

# Захват и распознавание лиц
https://robotos.in/uroki/obnaruzhenie-i-raspoznavanie-litsa-na-python
https://github.com/robotoss/OpenCV-Face-Recognition-master.git
https://www.pyimagesearch.com/2018/06/18/face-recognition-with-opencv-python-and-deep-learning/
https://github.com/ageitgey/face_recognition
https://cmusatyalab.github.io/openface/
https://neurohive.io/ru/tutorial/raspoznavanie-lica-facenet/
https://habr.com/ru/post/317798/
https://proglib.io/p/faceid-python/

# ML Проекты
https://rb.ru/story/30-ml-projects/

# Русские шрифты в OpenCv
http://www.compvision.ru/forum/index.php?/topic/625-unicode-%D0%B8-opencv-%D0%B2%D1%8B%D0%B2%D0%BE%D0%B4-%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%B8%D1%85-%D0%BD%D0%B0%D0%B4%D0%BF%D0%B8%D1%81%D0%B5%D0%B9/


# Описание OpenCV
http://robocraft.ru/page/opencv/
https://tproger.ru/translations/opencv-python-guide/

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

Работа с виртуальными окружениями:

    # Создание виртуального окружения  с именем tf и установить в него следующие пакеты
    conda create -n tf python=3 keras tensorflow pandas matplotlib jupyter nb_conda vs2017_win-64
    
    # показать список имеющихся виртуальных окружений
    conda info --envs
    
    # переключиться в виртуальное окружние
    conda activate tf
    
    # выйти из виртуального окружния
    conda activate
    
    # удаление виртуального окружения
    conda remove --name tf --all
    
    # клонирование виртуального окружения
    conda create --name myclone --clone myenv
    
    
# Создание клнфигурации для Tensorflow + Keras
How to Install Keras with Tensorflow using Conda
Feb 28, 2017
Updated 28 Jun 2017.
Keras is an amazing wrapper for Tensorflow (and Torch) that makes it simple to start playing with Neural Networks.
Using environment manager like Anaconda makes life easier. But sometimes due to different dependencies it takes additional steps to unserstand how to install needed packages.
I assume that you have Anaconda installed.
Since there is no tensorflow package in an Anaconda Package List one have to use conda-forge - community supported repository of packages.
But as of February 27, 2017 the latest Python version is 3.6 and conda-forge lacks tensorflow package for that version.
So first of all, let’s create environment with the Python, and name it a ‘tf’. I also advice to install pandas, matplotlib, jupyter and nb_conda packages for data manipulation and visualization of the result.

    conda config --add channels conda-forge
    conda create -n tf python=3 keras tensorflow pandas matplotlib jupyter nb_conda vs2017_win-64

Then we make new environment active:

    conda activate tf

Testing that Tensorflow is working

    python
    import tensorflow as tf
    hello = tf.constant('Hello, TensorFlow!')
    sess = tf.Session()
    print(sess.run(hello))

There would be warnings that The TensorFlow library wasn't compiled to use <...> instructions, .... That is ok. We don’t want to build libraries from the the source code here.
The succesfull output should be:
Hello, TensorFlow!
Set up Keras
To work with Tensorflow as backend, please make sure that you have the following in the ~/.keras/keras.json file:

    {
        "image_dim_ordering": "th",
        "floatx": "float32",
        "epsilon": 1e-07,
        "backend": "tensorflow"
    }

That’s it, you are ready to use Keras with Tensorflow!
Let’s do some “Hello, World!” handwritten digits recognition.


Поскольку после всех этих процедур у нас будет утсноавлен 

    numpy==1.17.0
    tensorflow==1.13.1

то при импорте tensorflow будут возникать варнинги, т.к. numpy 1.17.0 слишком новый
для tensoeflow 1.13.1. Поэтому нуно либо продаунгрэйдить numpy

    pip install nympy<1.16    #(а может и еще ниже до 1.14 ???)

либо роапгрейдить tensorflow

    pip install tensorflow==2.0.0-beta1




