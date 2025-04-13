# Distributed Systems

- **What is a Distributed System?**  
  Let's build a solid foundation before we move forward.

  Andrew S. Tanenbaum, an established author and computer scientist, defined distributed systems as:

  > **A collection of independent computers that appears to its users as one computer.**

  Seems obvious. In other words, it's a bunch of computers working together, serving some goals while appearing as one machine to the end user.

  Digging a little deeper, he defined three main characteristics for a system to be classified as a distributed system:

  1. The computers operate concurrently.  
  2. The computers fail independently.  
  3. The computers do not share a global clock.

  The third characteristic is subtle, but in many cases, it's the differentiating point between a distributed and a non-distributed system.

---

Now, let's look at **The Free Online Dictionary of Computing's** definition of Distributed Systems:

> A collection of (probably heterogeneous) automata whose distribution is transparent to the user so that the system appears as one local machine. This is in contrast to a network, where the user is aware that there are several machines; their location, storage replication, load balancing, and functionality is not transparent. Distributed systems usually use some kind of client-server organization.

If we study this statement closely, we can identify two faults:

- **"Appears as one local machine"** — This is almost never the case, as sites on the Web are never all up or all down at the same time.  
  _e.g._, site A might be up while site B is down; site B is up while site A is down—yet the Web *is* a distributed system.

- **"Usually use some kind of client-server organisation"** — In BitTorrent and many other peer-to-peer networks, the infrastructure relies on nodes or peers connected to each other and not on a central server—hence being called peer-to-peer.

You can see by now that **Tanenbaum’s** definition of a distributed system shares the same first fault with the FOLDOC definition.

---

For the purpose of sticking to technology, let's define a distributed system as the following:

> **A distributed system is a collection of nodes that are programmable, asynchronous, autonomous, and failure-prone, while communicating using an unreliable medium.**

### Here:

- **Nodes**: Any entity or process that is running on some device—be it a personal computer, a notebook, a mobile phone, or even a sensor.
- **Programmable**: Meaning this node responds to commands written in code included in these processes. Clearly, you cannot program humans or animals (at least not yet), so they cannot be included.
- **Asynchronous**: Each node runs based on its own clock, so entity clocks are not synchronized with each other.
- **Autonomous**: Each node will still operate on its own just fine even if left alone with its own devices on the network.
- **Failure-Prone**: Each entity may crash arbitrarily at any given time and may recover later.
- **Unreliable Medium**: Nodes send and receive messages between each other all the time, but those messages can drop or get delayed for no specific reason at any given time.
