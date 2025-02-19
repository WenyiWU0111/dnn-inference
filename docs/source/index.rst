.. dnn-inference documentation master file, created by
   sphinx-quickstart on Sun Aug  8 20:28:09 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

🔬 dnn-inference
================

.. -*- mode: rst -*-

|dAI|_ |PyPi|_ |Keras|_ |MIT|_ |Python3|_ |tensorflow|_ |downloads|_ |downloads_month|_

.. |dAI| image:: https://img.shields.io/badge/Powered%20by-cuhk%40dAI-purple.svg
.. _dAI: https://www.bendai.org

.. |PyPi| image:: https://badge.fury.io/py/dnn-inference.svg
.. _PyPi: https://pypi.org/project/dnn-inference/

.. |Keras| image:: https://img.shields.io/badge/keras-tf.keras-red.svg
.. _Keras: https://keras.io/

.. |MIT| image:: https://img.shields.io/pypi/l/dnn-inference.svg
.. _MIT: https://opensource.org/licenses/MIT

.. |Python3| image:: https://img.shields.io/badge/python-3-green.svg
.. _Python3: www.python.org

.. |tensorflow| image:: https://img.shields.io/badge/keras-tensorflow-blue.svg
.. _tensorflow: https://www.tensorflow.org/

.. |downloads| image:: https://pepy.tech/badge/dnn-inference
.. _downloads: https://pepy.tech/project/dnn-inference

.. |downloads_month| image:: https://pepy.tech/badge/dnn-inference/month
.. _downloads_month: https://pepy.tech/project/dnn-inference

.. image:: ./logo/logo_header.png
   :width: 900

**dnn-inference** is a Python module for hypothesis testing based on blackbox models, including **deep neural networks**. 

- GitHub repo: `https://github.com/statmlben/dnn-inference <https://github.com/statmlben/dnn-inference>`_
- Documentation: `https://dnn-inference.readthedocs.io <https://dnn-inference.readthedocs.io/en/latest/>`_
- PyPi: `https://pypi.org/project/dnn-inference <https://pypi.org/project/nonlinear-causal>`_
- Open Source: `MIT license <https://opensource.org/licenses/MIT>`_
- Paper: `arXiv:2103.04985 <https://arxiv.org/abs/2103.04985>`_


🎯 What We Can Do
-----------------

.. image:: ./logo/demo_result.png
   :width: 800

**dnn-inference** is able to provide an asymptotically valid `p-value` to examine if :math:`\mathcal{S}` is discriminative features to predict :math:`Y`.
Specifically, the proposed testing is:

.. math::

   H_0: R(f^*) - R_{\mathcal{S}}(g^*) = 0, \quad \text{versus} \quad H_a: R(f^*) - R_{\mathcal{S}}(g^*) < 0,


where :math:`\mathcal{S}` is a collection of hypothesized features, 
:math:`R` and :math:`R_{\mathcal{S}}` are risk functions with/without the hypothesized features :math:`\mathbf{X}_{\mathcal{S}}`, 
and :math:`f^*` and :math:`g^*` are population minimizers on :math:`R` and :math:`R_{\mathcal{S}}` respectively. 
The proposed test just considers the difference between the best predictive scores with/without hypothesized features. 
Please check more details in our paper `arXiv:2103.04985 <https://arxiv.org/abs/2103.04985>`_.

- When `log-likelihood` is used as a loss function, then the test is equivalent to a conditional independence test: :math:`Y \perp X_{\mathcal{S}} | X_{\mathcal{S}^c}`. 
- Only `a small number of fitting` on neural networks is required, and the number can be as small as 1.
- Asymptotically Type I error control and power consistency.


Reference
---------
**If you use this code please star the repository and cite the following paper:**

.. code:: bib

   @misc{dai2021significance,
         title={Significance tests of feature relevance for a blackbox learner},
         author={Ben Dai and Xiaotong Shen and Wei Pan},
         year={2021},
         eprint={2103.04985},
         archivePrefix={arXiv},
         primaryClass={stat.ML}
   }

📒 Contents
-----------

.. toctree::
   :maxdepth: 2

   installation
   example
   api

Indices and tables
==================

* :ref:`genindex`
* :ref:`search`
   
.. quickstart