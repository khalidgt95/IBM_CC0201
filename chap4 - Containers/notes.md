# Containers
- When running different applications, it becomes important to isolate them and give them dedicated resources
- If everything is running on a single machine, then that machine becomes a single point of failure
- To isolate user space instances, we use the concept of containers
- Each container or application space is independent from each other, meaning that they do not know about other's existence
- This segregation helps to isolate different components incase one of them fails
- These containers all use the same underlying kernel who manages them
