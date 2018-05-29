# Important principles for technology

Most of this is generic and basically equivalent to saying follow best practices. Hopefully this section will be refined more clearly to possess the high-level approach to a healthy technology mindset.

1. Code design, cleanliness, isolation, and ability to move and change is more important than the implementation of the code itself.
    1. The algorithmic approach to how the problem is solved is clearly needed to make the software "work".
    2. Following good code quality and design ensures that business changes don't destabilize the system.
    3. Code cleanliness and simplicity is just as important as the logic of the code!
2. Use the most appropriate technology for the task at hand.
    1. The newest and most exciting technology is not always the best choice.
    2. At the same time, the old stable technology may be stale and out of date.
    3. Picking the best technology for a project that is new and unknown by most of the company's engineers will have additional
challenges getting adoption.
    4. If a project is long-term, at times even if the technology is not well known...it may be worth the time and effort to adopt this
technology.
3. Version control, best practices.
    1. Don't store binary files in Git, use a proper binary versioning system.
    2. Store code related documentation alongside in git. Ideally documentation within your code repository should be updated alongside the code.
    3. Backup VCS repositories, you can corrupt and/or delete files that you cannot easily fix.
4. Design for least privilege access for all security controls.
    1. Don't take shortcuts, don't be lazy and reuse security groups.
    2. Prefer never allowing entire subnets or address blocks.
    3. Use security groups as sources and limit the ports to only those you need.
    4. Don't use the same public keys for every system and especially across environments.
5. All database calls must be executed by type safe technologies that follow type checking, proper error handling and logging levels.
    1. Generally, databases must utilize ORM technologies. Ideally, queries should not be written by hand.
    2. Try to use abstractions whenever possible as the storage mechanisms may change over time. You don't want to have to rewrite everything.
6. All data transferred in any public connection, and preferably even in private connections must be encrypted with the latest standards in
encryption.
    1. A public connection such as over the public internet. Even VPC's that are either publicly accessible or a lot of users and sensitive
data. The golden rule is data must never be transferred at all publicly unencrypted.
    2. Encryption does not always have to be using a TLS connection. Data may be encrypted at one end and sent over the wire
without any additional encryption and be acceptable.
    3. Consult with the CTO and or CISO on best practices and specifics.
