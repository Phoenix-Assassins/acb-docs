Hermes is the name of Ubisoft's engine module for online service management.

# Overview

Generally speaking, Hermes is a task-based facade (programming interface) for RMC services both from the original SDK (OSDK) and Ubisoft's custom RMC protocols (see [RMC](RMC.md) for details and full service list).

Since Hermes is only a Quazal RMC interface it is not strictly bound to the engine and was used in:
- Assassin's Creed Brotherhood (Anvil)
- Ghost Recon Phantoms (Yeti)
- Ghost Recon Future Soldier (Yeti)

# Hermes Interface

`HermesInterface` is a high-level API for RMC service management. It includes `RdvInterface` API which controls RMC protocol clients.

# Tasks

`Task` is an interface class for Hermes to trigger RMC service calls. Implementations of `Task` base class are schedulable operations to control RMC calls and define basic workflow for transactions. Tasks are scheduled and dispatched by `HermesInterface`. Task objects hold and directly pass data to/from RMC requests/responses.

Hermes unifies the workflow for RMC service calls:
1. A high-level `HermesInterface` service is called.
2. A `Task` object is created and scheduled by `HermesInterface`.
3. Task is dispatched by Hermes and its `opStart` method is called.
4. Task's method `opRunning` is called which executes its main workflow with RMC service calls.


# Online Events

The game's workflow depends on scheduling and dispatching job-like structures called Online Events. Those events can be scheduled externally via [notification events](/RMC-Notification-Protocol.md) as well as by the game internally.