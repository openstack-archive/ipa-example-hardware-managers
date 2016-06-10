ipa-example-hardware-managers
=============================

Example hardware managers for use with the `ironic python agent <http://git.openstack.org/cgit/openstack/ironic-python-agent>`_.

Example Device Hardware Manager
-------------------------------

This example manager is meant to demonstrate good patterns for developing a
device-specific hardware manager, such as for a specific version of NIC or
disk.

Use Cases include:
  * Adding device-specific clean-steps, such as to flash firmware or
    verify it's still properly working after being provisioned.
  * Implementing erase_device() using a vendor-provided utility for a given
    disk model.


Example Business Logic Hardware Manager
---------------------------------------

This example manager is meant to demonstrate how cleaning and the agent can
use the node object and the node itself to enforce business logic and node
consistency.

Use Cases include:
  * Quality control on hardware by ensuring no component is beyond its useful
    life.
  * Asserting truths about the node; such as number of disks or total RAM.
  * Reporting metrics about the node's hardware state.
  * Overriding logic of get_os_install_device().
