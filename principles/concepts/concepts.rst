.. _ops_challenges:

The Operations Challenge
------------------------

A deployment framework is key to solving the problems of deploying,
configuring, and scaling clusters for cloud computing.

Deploying a cloud or cluster of containers or bare metal server clusters can be a complex undertaking. Manual
processes can take days or even weeks of work to get a cluster fully
operational. Even then, the infrastructure is never static. In the real world, clusters of
solutions are constantly on an upgrade or improvement path. There is a
continuous need to deploy new servers, add management capabilities, and
track the upstream releases. This is all while keeping the cloud or cluster running and
providing reliable services to end users. Thus, service continuity
requirements dictate a need for automation and orchestration. There is
no other way to reduce the cost of a cloud while simultaneously improving the cloud's uptime reliability

These were among the challenges that drove the development of the
Digital Rebar software framework from its roots as an
`OpenStack <http://OpenStack.org>`__ installer (Crowbar) into a much broader
orchestration platform. Because of this evolution, Digital Rebar has a
number of architectural features to address these challenges:

-  *Abstraction Around Orchestration*: Digital Rebar is designed to simplify the operations of large scale infrastructure based on a layered deployment model by providing a higher level abstraction on top of the existing configuration management and orchestration tools.

-  *Web Architecture*: Digital Rebar is implemented as a web application server, with a full
   user interface and a predictable and consistent REST API.

-  *Platform Agnostic Implementation*: Digital Rebar is designed to be both a platform and operating system agnostic. It supports discovery and provisioning from a bare metal
   state, including hardware configuration, BIOS and BMC boards updating and configuration, and operating system installation. Multiple
   operating systems and heterogeneous operating systems are supported.
   Digital Rebar enables use of time-honored tools, industry standard
   tools, and any form of scriptable facility to perform its state
   transition operations.

-  *Modular Architecture*: Digital Rebar is designed around modular plug-ins called Barclamps. Barclamps allow for extensibility and customization while
   encapsulating the layers of deployment in manageable units.

-  *State Transition Management Engine*: The core of Digital Rebar is based on a state machine that tracks nodes, roles, and their relationships in groupings called deployments. The state machine is responsible for analyzing dependencies and
   scheduling state transition operations (transitions).

-  *Data Model*: Digital Rebar uses a dedicated database to track system state and
   data. As discovery and deployment progresses, system data is
   collected and made available to other components in the system.
   Individual components can access and update this data, reducing
   dependencies through a combination of deferred binding and runtime
   attribute injection.

-  *Network Abstraction*: Digital Rebar is designed to support a flexible network abstraction, in which physical interfaces, BMC's, VLANS, binding, teaming, and other
   low level features are mapped to logical conduits. Other components can then reference these conduits. Networking configurations can be
   created dynamically to adapt to changing infrastructure.
