# A meta VPN work in progress proof of concept

**Disclaimer: This is just a playground git repository to drop my ideas
on the subject. Don't expect any working tools.**

## Configuration of a node

1) Initialize

Each node needs to be initialized and its identification and keys created.

    # ./metavpn-init

2a) Create inital YAML configuration file on a trusted node

    # ./metavpn-config

2b) Export the public key for the trusted node

    # ./metavpn-identify

3) Add new node to the configuration on a trusted node

    # ./metavpn-add

## Synchronization

Basic mechanisms:

  * All new nodes talk to a configured reachable node.
  * All get registered.
  * All retrieve updated configuration.

Multiple nodes, split and merge

  * When two nodes offer a signed configuration, how do they synchronize? Do
    we use a timestamp or a Git repo or whatever? What if I have signing keys
    in two places, i.e. multiple trusted nodes?

## Terminology

Node
:   A system installation using metavpn.
Connected node
:   A node that is part of the VPN network.
Trusted node
:   A node with the authority to distribute a list of nodes and their keys.
