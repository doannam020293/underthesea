====================================
Underthesea - Vietnamese NLP Toolkit
====================================


.. image:: https://img.shields.io/pypi/v/underthesea.svg
        :target: https://pypi.python.org/pypi/underthesea

.. image:: https://img.shields.io/pypi/pyversions/underthesea.svg
        :target: https://pypi.python.org/pypi/underthesea

.. image:: https://img.shields.io/pypi/l/underthesea.svg
        :target: https://pypi.python.org/pypi/underthesea

.. image:: https://img.shields.io/travis/magizbox/underthesea.svg
        :target: https://travis-ci.org/magizbox/underthesea

.. image:: https://readthedocs.com/projects/magizbox-underthesea/badge/?version=latest
        :target: http://underthesea.readthedocs.io/en/latest/
        :alt: Documentation Status

.. image:: https://pyup.io/repos/github/magizbox/underthesea/shield.svg
        :target: https://pyup.io/repos/github/magizbox/underthesea/
        :alt: Updates

.. image:: https://img.shields.io/badge/chat-on%20facebook-green.svg
    :target: https://www.facebook.com/undertheseanlp/

|

.. image:: https://raw.githubusercontent.com/magizbox/underthesea/master/logo.jpg
        :target: https://raw.githubusercontent.com/magizbox/underthesea/master/logo.jpg

**underthesea** is a suite of open source Python modules, data sets and tutorials supporting research and development in Vietnamese Natural Language Processing.

* Free software: GNU General Public License v3
* Documentation: `https://underthesea.readthedocs.io <http://underthesea.readthedocs.io/en/latest/>`_
* Live demo: `underthesea app <http://magizbox.com:9386/#/>`_
* Facebook Page: `https://www.facebook.com/undertheseanlp/ <https://www.facebook.com/undertheseanlp/>`_

Installation
----------------------------------------

To install underthesea, simply:

.. code-block:: bash

    $ pip install underthesea
    ✨🍰✨

Satisfaction, guaranteed.

Usage
----------------------------------------

* `1. Word Segmentation <#1-word-segmentation>`_
* `2. POS Tagging <#2-pos-tagging>`_
* `3. Chunking <#3-chunking>`_
* `4. Named Entity Recognition <#4-named-entity-recognition>`_
* `5. Text Classification <#5-text-classification>`_
* `6. Sentiment Analysis <#6-sentiment-analysis>`_


****************************************
1. Word Segmentation
****************************************

.. image:: https://img.shields.io/badge/F1-94%25-red.svg
        :target: https://github.com/magizbox/underthesea.word_sent

.. image:: https://img.shields.io/badge/%E2%98%85-custom%20models-blue.svg
        :target: https://github.com/undertheseanlp/word_sent

.. image:: https://img.shields.io/badge/%E2%8C%AC-api-green.svg
    :target: http://underthesea.readthedocs.io/en/latest/api.html#word-sent-package

Usage

.. code-block:: python

    >>> # -*- coding: utf-8 -*-
    >>> from underthesea import word_sent
    >>> sentence = u"Chúng ta thường nói đến Rau sạch, Rau an toàn để phân biệt với các rau bình thường bán ngoài chợ."

    >>> word_sent(sentence)
    [u"Chúng ta", u"thường", u"nói", u"đến", u"Rau sạch", u",", u"Rau", u"an toàn", u"để", u"phân biệt", u"với",
    u"các", u"rau", u"bình thường", u"bán", u"ngoài", u"chợ", u"."]

    >>> word_sent(sentence, format="text")
    u'Chúng_ta thường nói đến Rau_sạch , Rau an_toàn để phân_biệt với các rau bình_thường bán ngoài chợ .'

****************************************
2. POS Tagging
****************************************

.. image:: https://img.shields.io/badge/accuracy-92.3%25-red.svg
        :target: https://github.com/magizbox/underthesea.pos_tag

.. image:: https://img.shields.io/badge/%E2%98%85-custom%20models-blue.svg
        :target: https://github.com/undertheseanlp/pos_tag

.. image:: https://img.shields.io/badge/%E2%8C%AC-api-green.svg
    :target: http://underthesea.readthedocs.io/en/latest/api.html#pos-tag-package

Usage

.. code-block:: python

    >>> # -*- coding: utf-8 -*-
    >>> from underthesea import pos_tag
    >>> text = u"Chợ thịt chó nổi tiếng ở TP Hồ Chí Minh bị truy quét"
    >>> pos_tag(text)
    [(u'Chợ', 'N'),
     (u'thịt', 'N'),
     (u'chó', 'N'),
     (u'nổi tiếng', 'A'),
     (u'ở', 'E'),
     (u'TP HCM', 'Np'),
     (u'bị', 'V'),
     (u'truy quét', 'V')]

****************************************
3. Chunking
****************************************

.. image:: https://img.shields.io/badge/F1-77%25-red.svg
		:target: https://github.com/magizbox/underthesea.chunking

.. image:: https://img.shields.io/badge/%E2%98%85-custom%20models-blue.svg
		:target: https://github.com/undertheseanlp/chunking

.. image:: https://img.shields.io/badge/%E2%8C%AC-api-green.svg
    :target: http://underthesea.readthedocs.io/en/latest/api.html#chunking-package

Usage

.. code-block:: python

    >>> # -*- coding: utf-8 -*-
    >>> from underthesea import chunk
    >>> text = u"Bác sĩ bây giờ có thể thản nhiên báo tin bệnh nhân bị ung thư?"
    >>> chunk(text)
    [(u'Bác sĩ', 'N', 'B-NP'),
     (u'bây giờ', 'P', 'I-NP'),
     (u'có thể', 'R', 'B-VP'),
     (u'thản nhiên', 'V', 'I-VP'),
     (u'báo tin', 'N', 'B-NP'),
     (u'bệnh nhân', 'N', 'I-NP'),
     (u'bị', 'V', 'B-VP'),
     (u'ung thư', 'N', 'I-VP'),
     (u'?', 'CH', 'O')]

****************************************
4. Named Entity Recognition
****************************************

.. image:: https://img.shields.io/badge/F1-86.6%25-red.svg
		:target: https://github.com/magizbox/underthesea.ner

.. image:: https://img.shields.io/badge/%E2%98%85-custom%20models-blue.svg
		:target: https://github.com/undertheseanlp/ner

.. image:: https://img.shields.io/badge/%E2%8C%AC-api-green.svg
    :target: http://underthesea.readthedocs.io/en/latest/api.html#ner-package

Usage

.. code-block:: python

    >>> # -*- coding: utf-8 -*-
    >>> from underthesea import ner
    >>> text = u"Chưa tiết lộ lịch trình tới Việt Nam của Tổng thống Mỹ Donald Trump"
    >>> ner(text)
    [('Chưa', 'R', 'O', 'O'),
     ('tiết lộ', 'V', 'B-VP', 'O'),
     ('lịch trình', 'V', 'B-VP', 'O'),
     ('tới', 'E', 'B-PP', 'O'),
     ('Việt Nam', 'Np', 'B-NP', 'B-LOC'),
     ('của', 'E', 'B-PP', 'O'),
     ('Tổng thống', 'N', 'B-NP', 'O'),
     ('Mỹ', 'Np', 'B-NP', 'B-LOC'),
     ('Donald', 'Np', 'B-NP', 'B-PER'),
     ('Trump', 'Np', 'B-NP', 'I-PER')]


****************************************
5. Text Classification
****************************************

.. image:: https://img.shields.io/badge/accuracy-86.7%25-red.svg
    :target: https://github.com/magizbox/underthesea.classification

.. image:: https://img.shields.io/badge/%E2%98%85-custom%20models-blue.svg
    :target: https://github.com/undertheseanlp/classification

.. image:: https://img.shields.io/badge/%E2%8C%AC-api-green.svg
    :target: http://underthesea.readthedocs.io/en/latest/api.html#classify-package

Install dependencies and download default model

.. code-block:: bash

    $ pip install Cython
    $ pip install future scipy numpy scikit-learn
    $ pip install -U fasttext --no-cache-dir --no-deps --force-reinstall
    $ underthesea data

Usage

.. code-block:: python

    >>> # -*- coding: utf-8 -*-
    >>> from underthesea import classify
    >>> classify("HLV đầu tiên ở Premier League bị sa thải sau 4 vòng đấu")
    ['The thao']
    >>> classify("Hội đồng tư vấn kinh doanh Asean vinh danh giải thưởng quốc tế")
    ['Kinh doanh']
    >>> classify("Đánh giá “rạp hát tại gia” Samsung Soundbar Sound+ MS750")
    ['Vi tinh']

****************************************
6. Sentiment Analysis
****************************************

.. image:: https://img.shields.io/badge/F1-55.5%25-red.svg
		:target: https://github.com/undertheseanlp/sentiment

.. image:: https://img.shields.io/badge/%E2%98%85-custom%20models-blue.svg
    :target: https://github.com/undertheseanlp/sentiment

.. image:: https://img.shields.io/badge/%E2%8C%AC-api-green.svg
    :target: http://underthesea.readthedocs.io/en/latest/api.html#sentiment-package

Install dependencies

.. code-block:: bash

    $ pip install future scipy numpy scikit-learn==0.19.0 joblib

Usage


.. code-block:: python

    >>> # -*- coding: utf-8 -*-
    >>> from underthesea import sentiment
    >>> sentiment("Gọi mấy lần mà lúc nào cũng là các chuyên viên đang bận hết ạ")
    ('CUSTOMER SUPPORT#NEGATIVE',)
    >>> sentiment("bidv cho vay hay ko phu thuoc y thich cua thang tham dinh, ko co quy dinh ro rang")
    ('LOAN#NEGATIVE',)

Up Coming Features
----------------------------------------

* Text to Speech
* Automatic Speech Recognition
* Machine Translation
* Dependency Parsing

Contributing
----------------------------------------

Do you want to contribute with underthesea development? Great! Please read more details at `CONTRIBUTING.rst. <https://github.com/magizbox/underthesea/blob/master/CONTRIBUTING.rst>`_
