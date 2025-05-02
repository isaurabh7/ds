
Assignment 1: Socket Programming

1. What is interprocess communication?
Interprocess communication (IPC) refers to the mechanisms that allow processes to communicate with each other and synchronize their actions, either on the same or different computers in a network.

2. What is socket?
A socket is an endpoint for sending or receiving data across a computer network. It enables communication between processes over a network using protocols like TCP or UDP.

3. Difference between TCP and UDP socket communication?

TCP: Connection-oriented, reliable, ensures delivery, and maintains order.

UDP: Connectionless, faster but unreliable, suitable for time-sensitive transmissions.


4. What is shared memory programming?
It is a form of IPC where multiple processes can access a common memory space for communication.

5. What is port? State application of port.
A port is a logical access channel for a network service. Applications like web browsers (port 80 for HTTP) or email clients (port 25 for SMTP) use specific ports to communicate.


---

Assignment 2: Remote Method Invocation

1. What is Heterogeneity?
Heterogeneity refers to systems and applications built on different platforms, languages, or architectures that still need to interact.

2. Example of marshaling and unmarshalling?
Marshaling: Converting Java objects into a format suitable for network transmission.
Unmarshalling: Converting received data back into Java objects.

3. Explain RMI with diagram.
RMI enables a Java object to invoke methods on an object in another JVM. It uses stub (client-side proxy) and skeleton (server-side gateway), and communicates via the RMI registry.

4. What is binding?
Binding associates a name with a remote object in the RMI registry so that clients can locate it.

5. What is role of RMI registry? Why start RMI registry first?
It acts as a naming service where remote objects are registered and discovered. It must be running before server binds objects.

6. What is use of UnicastRemoteObject, lookup(), rebind()?

UnicastRemoteObject: Enables remote access.

lookup(): Client locates remote object.

rebind(): Server registers object in the registry.


7. What is stub and skeleton?
Stub resides on the client and forwards method calls. Skeleton on server receives calls and dispatches them.

8. What is difference between Exception and RemoteException?

Exception is a general class for all exceptions.

RemoteException is specific to issues during remote method calls.



---

Assignment 3: CORBA

1. What is CORBA?
CORBA (Common Object Request Broker Architecture) is a standard for distributed objects communication.

2. How CORBA works?
It uses ORB to handle requests across languages and platforms using IIOP protocol.

3. Is it synchronous/Asynchronous?
CORBA supports both, but is primarily synchronous.

4. What is ORB?
ORB (Object Request Broker) routes client requests to appropriate object implementations.

5. What is IDL interface?
IDL (Interface Definition Language) defines methods that remote CORBA objects expose.

6. What is ORBD?
Object Request Broker Daemon enables client-server communication and object registration.

7. What is middleware?
Middleware is software that connects different applications or services in a distributed system.

8. Examples of middleware:
CORBA, RMI, SOAP, REST, .NET Remoting.

9. Use of middleware:

Communication between apps

Scalability

Security

Interoperability


10. Applications of CORBA:
Banking systems, telecommunications, air traffic control, enterprise-level distributed applications.


---

Assignment 4: MPI

1. What is use of MPI?
MPI allows processes to communicate and coordinate in parallel computing systems.

2. Application of MPI?
Used in scientific simulations, big data analytics, and parallel processing systems.

3. Why assign rank to process in MPI?
To identify and manage communication among processes uniquely.

4. Explain MPI operations:

Initialization (MPI_Init)

Communication (MPI_Send, MPI_Recv)

Finalization (MPI_Finalize)

Synchronization, Scatter, Gather


5. Different data types of MPI:
MPI_INT, MPI_FLOAT, MPI_DOUBLE, MPI_CHAR, etc.

6. Draw MPI architecture:
(MPI_COMM_WORLD -> Communicators -> Processes)

7. What is MPI_ABORT?
Terminates all processes in the communicator.

8. What is MPI_FINALIZE?
Cleans up and ends MPI environment.

9. Difference between MPI_ABORT and MPI_FINALIZE?

MPI_ABORT: Forceful termination.

MPI_FINALIZE: Graceful shutdown.



---

Assignment 5: Clock Synchronization

1. Difference between logical clock and physical clock?

Logical Clock: Orders events (Lamport clock).

Physical Clock: Real-world time (system clock).


2. Why synchronize clocks in distributed systems?
To maintain consistency, coordination, and correctness in event ordering.

3. How Berkeley algorithm synchronizes time?
Master polls slave clocks, calculates average offset, and broadcasts adjustment.

4. Other clock synchronization algorithms:

Cristian’s Algorithm

NTP (Network Time Protocol)

Lamport Timestamp

Vector Clocks



---

Assignment 6: Mutual Exclusion

1. What is race condition?
A race condition occurs when multiple processes access shared data concurrently and the outcome depends on the sequence of access.

2. What is deadlock and starvation?

Deadlock: All processes wait indefinitely.

Starvation: A process never gets access due to continuous denial.


3. What is Mutual Exclusion?
Ensuring only one process accesses the critical section at a time.

4. How to avoid mutual exclusion?
Using algorithms like Token Ring, Ricart–Agrawala, or centralized coordination.


---

Assignment 7: Election Algorithms

1. Who is process coordinator? Responsibilities?
Coordinator is a designated process managing tasks like resource allocation and synchronization.

2. Need of Election Algorithm?
To elect a new coordinator when the current one fails.

3. What is centralized and decentralized algorithm?

Centralized: Single controller makes decisions.

Decentralized: Decisions distributed among nodes.


4. Explain working of Ring & Bully Algorithm?

Ring: Passes message in a logical ring; highest ID becomes coordinator.

Bully: Highest-numbered active process wins by sending election messages to higher-ID processes.


5. What is a Token?
A control message passed among processes to gain access or coordinate actions.

6. Why “Bully” algorithm?
Because the highest-ID process “bullies” its way to coordination, overriding lower processes.


---

Assignment 8: Web Services

1. What Is a Web Service?
Software system designed to support interoperable machine-to-machine interaction over a network.

2. Explain Architecture (Provider, Requestor, Registry, Broker):

Provider: Offers service

Requestor: Consumes service

Registry: Directory to find services

Broker: Mediates between provider and requestor (optional)


3. What is WSDL?
Web Services Description Language – describes service interface in XML.

4. Types of Web Services:

SOAP (protocol-based)

REST (architectural style)


5. Difference between SOAP and REST:
| Feature | SOAP | REST | |--------|------|------| | Protocol | Yes | No | | Format | XML | XML/JSON | | Speed | Slower | Faster | | Flexibility | Less | More | | Standards | Strict | Loose |

6. Examples of web services:
Google Maps API, Amazon Web Services, PayPal API.

7. Applications of web services:
Cloud storage, e-commerce, online banking, social networking apps.
