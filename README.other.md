
              item                        size in bytes             position
    +--------------------------------+-------------------------+
    | Hash Descriptor                |  total 132              |
    |                                |                         |
    |  - tag                         |     8                   |    --> +0
    |  - num_bytes_following         |     8                   |    --> +8
    |  - hash algorithm              |     8                   |    --> +16
    |  - partition name              |     32                  |
    |  - salt length                 |     4                   |
    |  - digest length               |     4                   |
    |  - reserved                    |     60                  |
    +--------------------------------+-------------------------+
    | Partition name                 |                         |
    +--------------------------------+-------------------------+
    | salt                           |                         |
    +--------------------------------+-------------------------+
    | digest                         |                         |
    +--------------------------------+-------------------------+
    | Padding                        |  align by 8             |
    +--------------------------------+-------------------------+    --> +16 + num_bytes_following
