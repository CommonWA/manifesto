# An Initiative to Create a Common WebAssembly Runtime and Interface Specification

### WHAT IS WEBASSEMBLY?
WebAssembly (wasm) is a safe, portable, low-level code format designed for efficient execution and compact representation.

WebAssembly's thoughtful design makes it a suitable compilation target for other high-level languages and this can be observed from the great enthusiasm within the community as many create compilers and runtimes that target WebAssembly bytecode. Although WebAssembly's initial implementations were for web browsers, it is not constrained to that environment and it is desirable by some to have it running in other environments like the server or a kernel's Ring 0.

### WHAT ARE WE TRYING TO ACHIEVE?
The aim of this initiative is to help webassembly achieve what it is really designed for. To be a universally portable executable format. This goal cannot be realized if the various wasm runtimes have widly different APIs. This means code written for one runtime won't necessarily work correctly on another runtime. Therefore the specific goal of this initiative is to get all the creators to agree on a common interface specification with which wasm programs can call underlying systems. By underlying sytems, we mean any sort of functionality or extension exposed to the webassembly runtime which a wasm program can take advantage of.

Now it is important to describe what we mean by API. Application Programming Interface (or API) is an high-level abstraction that allows two programs to interact with each other. The APIs will define how a wasm will communicate and share data with its host and they can be implemented in a number of ways.

### WHY THIS IS IMPORTANT?
This initiative is important because wasm runtime developers can come together to agree on certain interface specification, thereby standardizing it and making it easy for the users and developers of wasm programs to run their programs anywhere with zero or minimal modification. This should always hold true given the runtime provides similar set of functionalities the wasm code expects.

### WHY WE CAN'T REALLY WAIT FOR THE OFFICIAL SPECS COVERAGE
Indeed one can wait for the official specification of host bindings and GC to be completed, but it is unknown when this specification will be done or whether it will cover all the areas that are important to some runtime developers. In addition to this, there are already several implementations in works, many of which are already rolling their own APIs. Some of these runtimes may become widely used in the future and given the current state of things this will lead to situations where wasm programs are not portable between similar runtimes.

### WHY WE CAN'T RESUSE EXISTING STANDARDS
Ideas can be borrowed from existing standards (such as POSIX) but it should be done in a way that fits webassembly use case and its applications.

### WHY THE COMMON RUNTIME IS NEEDED
It's easy to come up with ideas, some of which may end up not working well in production. This is why the development of a wasm engine is part of this initiative.
While working on a canonical implementation, we can find flaws in our ideas and adjust appropriately.

### HOW DECISIONS WILL BE MADE
The decision making process will be based on general consensus. There won't be a singular figure or lead making the decisions, instead it will based on the selection of popular opinions. In cases where decisions cannot be reached a voting system will be used to arrive at a definite choice.

### IN SUMMARY
We want to be able to run a valid webassembly program on any available runtime as long as such runtime provide the set of functionalities expected by the program.

