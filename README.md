'''

I n t r o d u c t i o n

Corps Python helps developers compose modular and adaptive Python-based micro-services, services, and applications
(all examples of Corps) for deployment on arbitrary configurations of many processors on many hosts.

Corps Python is a Python package built using standard Python and is a superset of it.

Corps Python is designed to reduce the many traditional pain points in developing, deploying, and managing concurrent
programs in heterogenous parallel and distributed contexts such as multiprocessor hosts and hybrid- and multi-cloud.

Any host where Python runs can run Corps Python. If the host has multiple cores/processors they can be utilized as part
of a Corps.

If the host has internet connectivity it can be part of a larger-scale Corps, even if the machines run different
operating systems and have different processor types.

Corps Python can run a Corps on any vendor's cloud, on data center servers and employees' desktop computers, in edge
data centers or in edge devices, etc., all at the same time.

It makes the underlying computational machinery (threads, processes, synchronization objects and operations, network
stacks, underlying operating system, processor types, etc.) disappear.

Developers can simply focus on program functionality.


B a s i c   C o m p u t a t i o n a l   M o d e l

Corps Python adds a small number of easy-to-use, but powerful, abstractions to Python, as well as a transparent
run-time system.

An individual Corps is an assemblage of Workers that can work independently or cooperatively to accomplish a task.

Workers can be built from regular Python objects (Concs) or functions (Funcs), from previously-defined Corps (Corps
can be Workers external to the Corps or as contained, private, Workers), or custom-built from standard Worker
classes.

Each Corps is internally composed of a number of environments, or Envs, where Workers live and run.

The Envs are transparent to developers and are automatically created on the various Hosts' processors by the Corps
Python runtime.

The Workers are automatically created and placed in the Envs and all operations between them are automatic and
transparent, even when the Workers are in different Envs.

Regular Python methods and functions operate synchronously.

The caller, running in a single thread, single process, makes the call and the Python run-time pauses the caller
until the return value has been produced by the method or function.

But Workers can operate asynchronously from other Workers.

If a Worker asks another Worker to execute a method or function, the requesting Worker can do something else while the
servicing Worker accomplishes its task.

In fact it can ask many other servicing Workers to work concurrently.  And those Workers themselves may be composed of
many concurrently-operating Workers, and so on.

When the Workers are running on many processors in many hosts a high degree of parallelism can be achieved.

Corps Python automatically creates and sends the messages that pass between the Workers, schedules the Workers'
execution of the functions or methods, and returns the results back to the requesting Worker.

The calls to the Workers' methods and functions use the same syntax as regular Python objects' methods and
functions.

The developer just has to handle the asynchronously-returned result (which is fairly easy).



F u r t h e r   R e a d i n g

- All documentation is contained in the Doc directory.

- The Tutorials (Tutorial0.py, Tutorial1.py, etc) introduce the major Corps Python abstractions and demonstrate
    some important usage patterns.

- Status.py summarizes the project status.

- Roadmap.py contains the current development tasks as well as a list of future initiatives.

- The Corps Python Reference, Reference.py, is the definitive specification outside of the codebase for
    developer-facing functionality.

- The Integration Tests (CorpsPythonTest and CorpsTest0, 1, ...) in the Test directory attempt to vigorously exercise
    Corps Python functionality and can serve as examples of feature usage.

'''
