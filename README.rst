Introduction
============




.. image:: https://img.shields.io/discord/327254708534116352.svg
    :target: https://adafru.it/discord
    :alt: Discord


.. image:: https://github.com/CedarGroveStudios/CircuitPython_AD5245/workflows/Build%20CI/badge.svg
    :target: https://github.com/CedarGroveStudios/CircuitPython_AD5245/actions
    :alt: Build Status


.. image:: https://img.shields.io/badge/code%20style-black-000000.svg
    :target: https://github.com/psf/black
    :alt: Code Style: Black

A CircuitPython driver for the AD5245 digital potentiometer.

The AD5245 Digital Potentiometer is an I2C, 10K-ohm chip. The potentiometer sports
256 resistance steps and can work with a power source from 2.7v to 5.5v. The pins
act similarly to a passive resistive potentiometer, but require that voltages placed
on any of the three pins not exceed the power supply voltage or drop below ground potential.

The Cedar Grove AD5245 custom breakout board provides power and signal connections
for I2C and the potentiometer chip. The AD5245 is also integrated with the
AD9833 ADSR Precision Waveform Generator FeatherWing.


Dependencies
=============
This driver depends on:

* `Adafruit CircuitPython <https://github.com/adafruit/circuitpython>`_

Please ensure all dependencies are available on the CircuitPython filesystem.
This is easily achieved by downloading
`the Adafruit library and driver bundle <https://circuitpython.org/libraries>`_
or individual libraries can be installed using
`circup <https://github.com/adafruit/circup>`_.

Installing to a Connected CircuitPython Device with Circup
==========================================================

Make sure that you have ``circup`` installed in your Python environment.
Install it with the following command if necessary:

.. code-block:: shell

    pip3 install circup

With ``circup`` installed and your CircuitPython device connected use the
following command to install:

.. code-block:: shell

    circup install cedargrove_ad5245

Or the following command to update an existing version:

.. code-block:: shell

    circup update

Usage Example
=============

.. code-block:: python

    import cedargrove_ad5245

    ad5245 = cedargrove_ad5245.AD5245(address=0x2C)

    ad5245.wiper = 255
    print("Wiper set to %d"%ad5245.wiper)


``ad5245_simpletest.py`` and other examples can be found in the ``examples`` folder.


Documentation
=============
`AD5245 CircuitPython Driver API Class Description <https://github.com/CedarGroveStudios/CircuitPython_AD5245/blob/master/media/pseudo_readthedocs_cedargrove_ad5245.pdf>`_

`CedarGrove AD5245 Breakout OSH Park Project <https://oshpark.com/shared_projects/WcYMJx7L>`_

.. image:: https://github.com/CedarGroveStudios/CircuitPython_AD5245/blob/master/media/AD5245_breakout_for_fritzing.png

For information on building library documentation, please check out
`this guide <https://learn.adafruit.com/creating-and-sharing-a-circuitpython-library/sharing-our-docs-on-readthedocs#sphinx-5-1>`_.

Contributing
============

Contributions are welcome! Please read our `Code of Conduct
<https://github.com/CedarGroveStudios/Cedargrove_CircuitPython_AD5245/blob/HEAD/CODE_OF_CONDUCT.md>`_
before contributing to help this project stay welcoming.
