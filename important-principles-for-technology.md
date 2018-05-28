# Important principles for technology
1. Code design, cleanliness, isolation, and ability to move and change is more important than the implementation of the code itself.
    1. The algorithmic approach to how the problem is solved is clearly needed to make the software "work".
    2. Following good code quality and design ensures that business changes don't destabilize the system.
2. Use the most appropriate technology for the task at hand.
    1. The newest and most exciting technology is not always the best choice.
    2. At the same time, the old stable technology may be stale and out of date.
    3. Picking the best technology for a project that is new and unknown by most of the company's engineers will have additional
challenges getting adoption.
    4. If a project is long-term, at times even if the technology is not well known...it may be worth the time and effort to adopt this
technology.
3. Version control, best practices.
4. Design for least privilege access for all security controls.
    1. Don't take shortcuts, don't be lazy and reuse security groups.
    2. Prefer never allowing entire subnets or address blocks.
    3. Use security groups as sources and limit the ports to only those you need.
    4. Don't use the same public keys for every system and especially across environments.
5. All database calls must be executed by type safe technologies that follow type checking, proper error handling and logging levels.
    1. Generally, databases must utilize ORM technologies. Ideally, queries should not be written by hand.
6. All data transferred in any public connection, and preferably even in private connections must be encrypted with the latest standards in
encryption.
    1. A public connection such as over the public internet. Even VPC's that are either publicly accessible or a lot of users and sensitive
data. The golden rule is data must never be transferred at all publicly unencrypted.
    2. Encryption does not always have to be using a TLS connection. Data may be encrypted at one end and sent over the wire
without any additional encryption and be acceptable.
    3. Consult with the CTO and or CISO on best practices and specifics. There are many possible way to k
