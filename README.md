# 🎮 C# MMO Game Server

This project is a high-performance MMO Game Server built from scratch using C# and .NET. It is the result of applying core concepts of MMO server development, including multithreaded programming, asynchronous socket networking, packet serialization, and concurrency control.

---

## 🚀 Key Features & Core Concepts Implemented

This server incorporates the following core technologies to build a stable and scalable MMO backend.

### 🧠 Multithreaded Programming
- **Thread Management:** Maximizes performance in multi-core CPU environments by directly creating and managing C# threads.
- **Synchronization Primitives:** Ensures thread-safe access to shared resources by implementing custom `SpinLock`, `ReaderWriterLock`, `AutoResetEvent`, and leveraging the `Interlocked` class.
- **Deadlock Avoidance:** Implements strategies such as lock ordering to prevent deadlocks in a concurrent environment.
- **Memory Model & Optimization:** Guarantees code predictability and correctness by understanding the C# memory model, compiler optimizations, CPU caching, and using `Memory Barriers`.
- **Thread Local Storage (TLS):** Enhances performance by reducing lock contention, allowing each thread to manage its own data independently.

### 🌐 Network Programming
- **Asynchronous Socket Programming:** Efficiently handles thousands of concurrent client connections using an asynchronous I/O model based on C#'s `Socket` class.
- **Session Management:** Manages each client connection as a `Session` object, handling data reception, transmission, and disconnection logic.
- **Custom Buffer Management:** Minimizes garbage collection and reuses memory efficiently by implementing custom `SendBuffer` and `RecvBuffer` classes.
- **TCP-Based Communication:** Utilizes the TCP protocol for reliable data transmission, with custom `Listener` and `Connector` implementations to manage server-client connections.

### 📦 Packet Serialization & Automation
- **Custom Serialization:** Implements a custom binary serialization framework to convert game packets into byte arrays and back, handling string encoding differences (`UTF-8` vs. `UTF-16`).
- **Packet Generator:** Automates the creation of C# packet classes for both the server and client from a simple definition file (e.g., XML or JSON). This reduces repetitive work and prevents human error.

### ⚡ Job Queue & Concurrency
- **Job Queue System:** Implements a job queue to process client requests sequentially on a dedicated worker thread. This model simplifies state management and avoids complex synchronization issues for core game logic.
- **Command Pattern:** Encapsulates various game logic tasks as `Job` objects, allowing them to be processed consistently by the job queue.
- **Job Timer:** Manages delayed actions and periodic events by scheduling jobs to be executed at a specific time in the future.

---

## 🛠️ Technologies Used
- **C#**
- **.NET Framework / .NET Core**
- **Visual Studio**
