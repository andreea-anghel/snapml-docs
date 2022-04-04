Installation Guide
##################

Snap ML can be installed using pip.

.. code-block:: bash

    pip install snapml

* Your pip version should be at least 19.3.
* We currently support Python 3.7, 3.8 and 3.9.
* The OpenMP runtime must also be installed on your system.

Complete instructions for all supported platforms are provided below.

Ubuntu
======

On Ubuntu we support Intel™ (x86_64), IBM Power™ (ppc64le) and IBM Z™ (s390x) architectures.

To install Snap ML:

.. code-block:: bash

    apt-get install -y libgomp1
    pip install snapml

In order to use GPU acceleration one should have CUDA 10.2 (or higher) installed.

RHEL/CentOS
=============

On RHEL/CentOS we support Intel™ (x86_64), IBM Power™ (ppc64le) and IBM Z™ (s390x) architectures.

To install Snap ML:

.. code-block:: bash

    yum install -y libgomp
    pip install snapml    

In order to use GPU acceleration one should have CUDA 10.2 (or higher) installed.

MacOS
=====

On MacOS we support the Intel™ (x86_64) architecture.

To install Snap ML:

.. code-block:: bash

    brew install libomp
    pip install snapml

GPU acceleration is not currently supported on MacOS.

Windows
=======

On Windows we support the Intel™ (amd64) architecture.

To install Snap ML, one should firstly download and install the `Microsoft Visual C++ Redistributable for Visual Studio 2019 <https://aka.ms/vs/16/release/VC_redist.x64.exe>`_.
Next, install the Snap ML package via pip:

.. code-block:: bash

    pip install snapml

GPU acceleration is not currently supported on Windows.

