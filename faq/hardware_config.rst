.. index::

.. _faq_hardware_config:

Do New Pieces of Hardware Require Any Manual Configuration?
===========================================================

As long as it will PXE boot to a DHCP server under our control (for now), and Rebar has been delegated an IP address to use for admin purposes, then our current node discovery workflow will handle configuring IPMI/DRAC/AMT.  Rebar was initially designed as a tool to take racks of servers from racked and cabled to running Openstack or Hadoop with minimal intervention, and configuring things like IPMI is part of that workflow that we have retained.