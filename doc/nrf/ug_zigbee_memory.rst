.. _zigbee_memory:

Zigbee memory requirements
##########################

.. contents::
   :local:
   :depth: 2

This page provides information about the amount of flash memory and RAM that is required by :ref:`zigbee_samples`, as well as stack memory requirements for ``main`` and ``zboss`` threads.
Use it to check if your application has enough space for a given configuration.
Values are provided for :ref:`ZBOSS libraries <nrfxlib:zboss>`.

Samples were built using the available :ref:`nrfxlib:zboss`.
Unless stated otherwise, the default :file:`prj.conf` was used.

.. _zigbee_memory_52840:
.. _zigbee_memory_52833:
.. _zigbee_memory_5340:
.. _zigbee_memory_21540:

RAM and flash memory requirements
*********************************

RAM and flash memory requirement values differ depending on the DK, and the programmed sample.

The following tables list memory requirement values for Zigbee samples.

Values are provided in kilobytes (KB).
``n/a`` indicates that the sample with the given variant is not supported on the DK.

.. tabs::

   .. tab:: nRF52840

      The following table lists memory requirements for samples running on the :ref:`nRF52840 DK <gs_programming_board_names>` (:ref:`nrf52840dk_nrf52840 <zephyr:nrf52840dk_nrf52840>`).

      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | Sample                                                                                                                 | ROM, ZBOSS stack + App   | ROM, MCUboot bootloader   | ROM, ZBOSS non-volatile memory   | ROM, ZBOSS product config   | Total ROM   | RAM, ZBOSS stack + App   | Total RAM   |
      +========================================================================================================================+==========================+===========================+==================================+=============================+=============+==========================+=============+
      | :ref:`Network coordinator <zigbee_network_coordinator_sample>`                                                         | 327                      | 0                         | 32                               | 4                           | 363         | 67                       | 67          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light bulb <zigbee_light_bulb_sample>`                                                                           | 350                      | 0                         | 32                               | 4                           | 386         | 53                       | 53          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light switch <zigbee_light_switch_sample>`                                                                       | 270                      | 0                         | 32                               | 4                           | 306         | 48                       | 48          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light switch <zigbee_light_switch_sample>` with :ref:`lib_zigbee_fota`                                           | 282                      | 48                        | 32                               | 4                           | 366         | 53                       | 53          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light switch <zigbee_light_switch_sample>` with :ref:`zigbee_light_switch_sample_nus`                            | 373                      | 0                         | 32                               | 4                           | 409         | 64                       | 64          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light switch <zigbee_light_switch_sample>` with :ref:`zigbee_light_switch_sample_nus` and :ref:`lib_zigbee_fota` | 385                      | 48                        | 32                               | 4                           | 469         | 69                       | 69          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`NCP <zigbee_ncp_sample>`                                                                                         | 350                      | 0                         | 32                               | 4                           | 386         | 79                       | 79          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`NCP with USB transport <zigbee_ncp_sample>`                                                                      | 370                      | 64                        | 32                               | 4                           | 470         | 88                       | 88          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Zigbee application template <zigbee_template_sample>`                                                            | 326                      | 0                         | 32                               | 4                           | 362         | 62                       | 62          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Zigbee shell <zigbee_shell_sample>`                                                                              | 409                      | 0                         | 32                               | 4                           | 445         | 91                       | 91          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+

   .. tab:: nRF52833

      The following table lists memory requirements for samples running on the :ref:`nRF52833 DK <gs_programming_board_names>` (:ref:`nrf52833dk_nrf52833 <zephyr:nrf52833dk_nrf52833>`).

      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | Sample                                                                                                                 | ROM, ZBOSS stack + App   | ROM, MCUboot bootloader   | ROM, ZBOSS non-volatile memory   | ROM, ZBOSS product config   | Total ROM   | RAM, ZBOSS stack + App   | Total RAM   |
      +========================================================================================================================+==========================+===========================+==================================+=============================+=============+==========================+=============+
      | :ref:`Network coordinator <zigbee_network_coordinator_sample>`                                                         | 325                      | 0                         | 16                               | 4                           | 345         | 65                       | 65          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light bulb <zigbee_light_bulb_sample>`                                                                           | 348                      | 0                         | 16                               | 4                           | 368         | 51                       | 51          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light switch <zigbee_light_switch_sample>`                                                                       | 268                      | 0                         | 16                               | 4                           | 288         | 46                       | 46          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light switch <zigbee_light_switch_sample>` with :ref:`lib_zigbee_fota`                                           | n/a                      | n/a                       | n/a                              | n/a                         | n/a         | n/a                      | n/a         |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light switch <zigbee_light_switch_sample>` with :ref:`zigbee_light_switch_sample_nus`                            | 370                      | 0                         | 16                               | 4                           | 390         | 62                       | 62          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light switch <zigbee_light_switch_sample>` with :ref:`zigbee_light_switch_sample_nus` and :ref:`lib_zigbee_fota` | n/a                      | n/a                       | n/a                              | n/a                         | n/a         | n/a                      | n/a         |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`NCP <zigbee_ncp_sample>`                                                                                         | 348                      | 0                         | 16                               | 4                           | 368         | 77                       | 77          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`NCP with USB transport <zigbee_ncp_sample>`                                                                      | 368                      | 64                        | 16                               | 4                           | 452         | 86                       | 86          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Zigbee application template <zigbee_template_sample>`                                                            | 323                      | 0                         | 16                               | 4                           | 343         | 60                       | 60          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Zigbee shell <zigbee_shell_sample>`                                                                              | 396                      | 0                         | 16                               | 4                           | 416         | 86                       | 86          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+

   .. tab:: nRF5340

      The following table lists memory requirements for samples running on the :ref:`nRF5340 DK <gs_programming_board_names>` (:ref:`nrf5340dk_nrf5340_cpuapp <zephyr:nrf5340dk_nrf5340>`).

      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | Sample                                                                                                                 | ROM, ZBOSS stack + App   | ROM, MCUboot bootloader   | ROM, ZBOSS non-volatile memory   | ROM, ZBOSS product config   | Total ROM   | RAM, ZBOSS stack + App   | Total RAM   |
      +========================================================================================================================+==========================+===========================+==================================+=============================+=============+==========================+=============+
      | :ref:`Network coordinator <zigbee_network_coordinator_sample>`                                                         | 304                      | 0                         | 32                               | 4                           | 340         | 73                       | 73          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light bulb <zigbee_light_bulb_sample>`                                                                           | 327                      | 0                         | 32                               | 4                           | 363         | 60                       | 60          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light switch <zigbee_light_switch_sample>`                                                                       | 247                      | 0                         | 32                               | 4                           | 283         | 54                       | 54          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light switch <zigbee_light_switch_sample>` with :ref:`lib_zigbee_fota`                                           | n/a                      | n/a                       | n/a                              | n/a                         | n/a         | n/a                      | n/a         |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light switch <zigbee_light_switch_sample>` with :ref:`zigbee_light_switch_sample_nus`                            | 296                      | 0                         | 32                               | 4                           | 332         | 63                       | 63          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light switch <zigbee_light_switch_sample>` with :ref:`zigbee_light_switch_sample_nus` and :ref:`lib_zigbee_fota` | n/a                      | n/a                       | n/a                              | n/a                         | n/a         | n/a                      | n/a         |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`NCP <zigbee_ncp_sample>`                                                                                         | 327                      | 0                         | 32                               | 4                           | 363         | 86                       | 86          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`NCP with USB transport <zigbee_ncp_sample>`                                                                      | 347                      | 64                        | 32                               | 4                           | 447         | 95                       | 95          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Zigbee application template <zigbee_template_sample>`                                                            | 302                      | 0                         | 32                               | 4                           | 338         | 68                       | 68          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Zigbee shell <zigbee_shell_sample>`                                                                              | 371                      | 0                         | 32                               | 4                           | 407         | 94                       | 94          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+

   .. tab:: nRF21540

      The following table lists memory requirements for samples running on the :ref:`nR21540 DK <gs_programming_board_names>` (:ref:`nrf21540dk_nrf52840 <zephyr:nrf21540dk_nrf52840>`).

      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | Sample                                                                                                                 | ROM, ZBOSS stack + App   | ROM, MCUboot bootloader   | ROM, ZBOSS non-volatile memory   | ROM, ZBOSS product config   | Total ROM   | RAM, ZBOSS stack + App   | Total RAM   |
      +========================================================================================================================+==========================+===========================+==================================+=============================+=============+==========================+=============+
      | :ref:`Network coordinator <zigbee_network_coordinator_sample>`                                                         | 330                      | 0                         | 32                               | 4                           | 366         | 67                       | 67          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light bulb <zigbee_light_bulb_sample>`                                                                           | 352                      | 0                         | 32                               | 4                           | 388         | 53                       | 53          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light switch <zigbee_light_switch_sample>`                                                                       | 273                      | 0                         | 32                               | 4                           | 309         | 48                       | 48          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light switch <zigbee_light_switch_sample>` with :ref:`lib_zigbee_fota`                                           | 285                      | 48                        | 32                               | 4                           | 369         | 53                       | 53          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light switch <zigbee_light_switch_sample>` with :ref:`zigbee_light_switch_sample_nus`                            | n/a                      | n/a                       | n/a                              | n/a                         | n/a         | n/a                      | n/a         |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Light switch <zigbee_light_switch_sample>` with :ref:`zigbee_light_switch_sample_nus` and :ref:`lib_zigbee_fota` | n/a                      | n/a                       | n/a                              | n/a                         | n/a         | n/a                      | n/a         |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`NCP <zigbee_ncp_sample>`                                                                                         | 353                      | 0                         | 32                               | 4                           | 389         | 79                       | 79          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`NCP with USB transport <zigbee_ncp_sample>`                                                                      | 373                      | 64                        | 32                               | 4                           | 473         | 89                       | 89          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Zigbee application template <zigbee_template_sample>`                                                            | 328                      | 0                         | 32                               | 4                           | 364         | 62                       | 62          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+
      | :ref:`Zigbee shell <zigbee_shell_sample>`                                                                              | 411                      | 0                         | 32                               | 4                           | 447         | 91                       | 91          |
      +------------------------------------------------------------------------------------------------------------------------+--------------------------+---------------------------+----------------------------------+-----------------------------+-------------+--------------------------+-------------+

..

Stack memory requirements
*************************

The following table lists stack memory requirement values for ``main`` and ``zboss`` threads.
These measurements were carried out with :ref:`zephyr:thread_analyzer`, using the following Kconfig options for configuration:

* For the stack memory size of the ``main`` thread - :kconfig:`CONFIG_MAIN_STACK_SIZE`
* For the stack memory size of the ``zboss`` thread - :kconfig:`CONFIG_ZBOSS_DEFAULT_THREAD_STACK_SIZE`

Values are provided in bytes (B).

.. tabs::

   .. tab:: nRF52 Series

      The following table lists memory requirements for the :ref:`nRF52 Series <ug_nrf52>` devices.

      +----------------------------------------------------------------+-------------------------------+------------------------------+--------------------------------+-------------------------------+
      | Sample                                                         | ``main`` thread stack usage   | ``main`` thread stack size   | ``zboss`` thread stack usage   | ``zboss`` thread stack size   |
      +================================================================+===============================+==============================+================================+===============================+
      | :ref:`Network coordinator <zigbee_network_coordinator_sample>` | 464                           | 1024                         | 1120                           | 1952                          |
      +----------------------------------------------------------------+-------------------------------+------------------------------+--------------------------------+-------------------------------+
      | :ref:`Light bulb <zigbee_light_bulb_sample>`                   | 688                           | 1024                         | 1288                           | 1952                          |
      +----------------------------------------------------------------+-------------------------------+------------------------------+--------------------------------+-------------------------------+
      | :ref:`Light switch <zigbee_light_switch_sample>`               | 464                           | 1024                         | 1224                           | 1952                          |
      +----------------------------------------------------------------+-------------------------------+------------------------------+--------------------------------+-------------------------------+

   .. tab:: nRF53 Series

      The following table lists memory requirements for the :ref:`nRF53 Series <ug_nrf5340>` devices.

      +----------------------------------------------------------------+-------------------------------+------------------------------+--------------------------------+-------------------------------+
      | Sample                                                         | ``main`` thread stack usage   | ``main`` thread stack size   | ``zboss`` thread stack usage   | ``zboss`` thread stack size   |
      +================================================================+===============================+==============================+================================+===============================+
      | :ref:`Network coordinator <zigbee_network_coordinator_sample>` | 744                           | 2048                         | 1112                           | 2048                          |
      +----------------------------------------------------------------+-------------------------------+------------------------------+--------------------------------+-------------------------------+
      | :ref:`Light bulb <zigbee_light_bulb_sample>`                   | 744                           | 2048                         | 1056                           | 2048                          |
      +----------------------------------------------------------------+-------------------------------+------------------------------+--------------------------------+-------------------------------+
      | :ref:`Light switch <zigbee_light_switch_sample>`               | 744                           | 2048                         | 1032                           | 2048                          |
      +----------------------------------------------------------------+-------------------------------+------------------------------+--------------------------------+-------------------------------+

..
