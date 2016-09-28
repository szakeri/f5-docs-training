.. table:: Hierarchical Port Binding settings

    +--------------------------------------+-------------------------------------------+---------------+
    | Setting                              | Description                               | Default Value |
    +======================================+===========================================+===============+
    |f5_network_segment_physical_network   || The name of the network segment in which | None          |
    |                                      || the agent will manage BIG-IP(s).         |               |
    +--------------------------------------+-------------------------------------------+---------------+
    |f5_network_segment_polling_interval   || Seconds between polling Neutron for a    | 10            |
    |                                      || ``network_id`` to ``segmentation_id``    |               |
    |                                      || mapping.                                 |               |
    |                                      || See :ref:`disconnected services`.        |               |
    +--------------------------------------+-------------------------------------------+---------------+
    |f5_network_segment_gross_timeout      || Maximum seconds to wait for a network to | 300           |
    |                                      || be bound before the LBaaS request fails. |               |
    |                                      || See :ref:`disconnected services`.        |               |
    +--------------------------------------+-------------------------------------------+---------------+
