Purpose
=======
Spin-up a consul + registrator service in order to discover and configure external load-balancing, this could be totally redundent to our needs but in order to move fast we implemented this.

use-cases
=========

* Switching\Updating `HA proxy` / `nginx` ... to point to new services discovered by consul
