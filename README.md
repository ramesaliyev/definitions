<details><summary><strong>algorithm</strong></summary><br>

a process or set of rules to be followed in calculations or other problem-solving operations, especially by a computer.
</details>
<details><summary><strong>analogy</strong></summary><br>

a comparison between one thing and another, typically for the purpose of explanation or clarification.
</details>
<details><summary><strong>argument vs parameter</strong></summary><br>

**parameter** is variable in the declaration of function.

    function(parameter_1, parameter_2) -> ok.

**argument** is the actual value of this variable that gets passed to function.

    function(argument_1, argument_2).

</details>
<details><summary><strong>arity</strong></summary><br>

the arity of a function is an integer representing how many arguments can be passed to the function.

</details>
<details><summary><strong>code hot-loading</strong></summary><br>

upgrading an application while it runs, without stopping it

</details>
<details><summary><strong>determinism</strong></summary><br>

determinism is the philosophical belief that **all events are determined completely by previously existing causes**. the opposite of determinism is some kind of indeterminism (otherwise called nondeterminism) or randomness. determinism is often contrasted with free will.

### in computer science

determinism in computer science means, if we have a computing device and a state the device is in. **if for every such state, by a given input, there is at most one state that can follow, then the device is called deterministic. if there are two or more states that can follow, then the device is non-deterministic**. note that non-determinism doesn't mean we don't know which states can follow but that they be multiple.

also, randomness and non-determinism are two separate notions in computer science. randomness means that given a state, the next state depends upon the result of a random draw from some "set", like a coin toss.

a **deterministic algorithm** is an algorithm which, **given a particular input, will always produce the same output**, with the underlying machine always passing through the same sequence of states. but in case of **non-deterministic algorithm**, for the same input, the algorithm may produce different output in different runs.

</details>
<details><summary><strong>hard, firm, and soft real-time</strong></summary><br>

## hard real-time
hard real-time definition considers any missed deadline to be a system failure. This scheduling is used extensively in mission critical systems where failure to conform to timing constraints results in a loss of life or property.

**Examples:**
- Air France Flight 447 crashed into the ocean after a sensor malfunction caused a series of system errors. The pilots stalled the aircraft while responding to outdated instrument readings. All 12 crew and 216 passengers were killed.
- Mars Pathfinder spacecraft was nearly lost when a priority inversion caused system restarts. A higher priority task was not completed on time due to being blocked by a lower priority task. The problem was corrected and the spacecraft landed successfully.
- An Inkjet printer has a print head with control software for depositing the correct amount of ink onto a specific part of the paper. If a deadline is missed then the print job is ruined.

## firm real-time
firm real-time definition allows for infrequently missed deadlines. In these applications the system can survive task failures so long as they are adequately spaced, however the value of the task's completion drops to zero or becomes impossible.

**Examples:**
- Manufacturing systems with robot assembly lines where missing a deadline results in improperly assembling a part. As long as ruined parts are infrequent enough to be caught by quality control and not too costly, then production continues.
- A digital cable set-top box decodes time stamps for when frames must appear on the screen. Since the frames are time order sensitive a missed deadline causes jitter, diminishing quality of service. If the missed frame later becomes available it will only cause more jitter to display it, so it's useless. The viewer can still enjoy the program if jitter doesn't occur too often.

## soft real-time
soft real-time definition allows for frequently missed deadlines, and as long as tasks are timely executed their results continue to have value. Completed tasks may have increasing value up to the deadline and decreasing value past it.

**Examples:**
- Weather stations have many sensors for reading temperature, humidity, wind speed, etc. The readings should be taken and transmitted at regular intervals, however the sensors are not synchronized. Even though a sensor reading may be early or late compared with the others it can still be relevant as long as it is close enough.
- A video game console runs software for a game engine. There are many resources that must be shared between its tasks. At the same time tasks need to be completed according to the schedule for the game to play correctly. As long as tasks are being completely relatively on time the game will be enjoyable, and if not it may only lag a little.

[resource](https://stackoverflow.com/a/30498130)

</details>
<details><summary><strong>hierarchy</strong></summary><br>

a hierarchy is an arrangement of items in which the items are represented as being `above`, `below`, or `at the same level as` one another.
</details>
<details><summary><strong>idiomatic</strong></summary><br>

- using, containing, or denoting expressions that are natural to a native speaker.
- pertaining or conforming to the natural mode of expression of a language.
- the most natural way to express something in a language.

**idiomatic code** means following the conventions of the language. you should find the easiest and most common ways of accomplishing a task rather than porting your knowledge from a different language.
</details>
<details><summary><strong>imparative, declarative, procedural, functional</strong></summary><br>

for all programming paradigms see [wikipedia](https://en.wikipedia.org/wiki/Programming_paradigm). also see [comparison between paradigms](https://en.wikipedia.org/wiki/Comparison_of_programming_paradigms).

## imperative programming

**imperative programming** is a programming paradigm that uses statements that change a program's state. in much the same way that the imperative mood (imperative mood is a grammatical mood that forms a command or request.) in natural languages expresses commands, an imperative program consists of commands for the computer to perform. imperative programming focuses on describing **`how`** a program operates.

### structured programming

**structured programming** is a programming paradigm aimed at improving the clarity, quality, and development time of a computer program by making extensive use of the structured control flow constructs of selection (`if`/`then`/`else`) and repetition (`while` and `for`), `block structures`, and `subroutines`.

    % unstructured basic %

    10 DIM I
    20 LET I = 0
    30 PRINT "HELLO"
    40 LET I = I + 1
    50 IF I < 10 THEN GOTO 30 END IF

    % structured basic %

    DIM I
    FOR I = 0 TO 9
      PRINT "HELLO"
    NEXT

### procedural programming

**procedural programming** is a programming paradigm, derived from `structured programming`, based on the concept of the `procedure call`. `procedures`, also known as `routines`, `subroutines`, or `functions`, simply contain a series of computational steps to be carried out. any given procedure might be called at any point during a program's execution, including by other procedures or itself.

## declarative programming

**declarative programming** is a programming paradigm—a style of building the structure and elements of computer programs—that **`expresses the logic of a computation`** without describing its control flow.

### functional programming

**functional programming** is a programming paradigm where programs are constructed by `applying` and `composing` functions. it is a `declarative programming` paradigm in which function definitions are `trees of expressions` that each return a value, rather than a sequence of imperative statements which change the state of the program or world.

in functional programming, functions are treated as `first-class citizens`, meaning that they can be bound to names (including local identifiers), passed as arguments, and returned from other functions, just as any other data type can. this allows programs to be written in a declarative and composable style, where small functions are combined in a modular manner.

functional programming is sometimes treated as synonymous with **purely functional programming**, a subset of functional programming which treats all functions as `deterministic mathematical functions`, or `pure functions`. when a pure function is called with some given arguments, it will always return the same result, and cannot be affected by any mutable state or other side effects. this is in contrast with impure procedures, common in imperative programming, which can have side effects (such as modifying the program's state or taking input from a user). proponents of purely functional programming claim that by restricting side effects, programs can have fewer bugs, be easier to debug and test, and be more suited to formal verification.

functional programming has its roots in academia, evolving from the lambda calculus, a formal system of computation based only on functions. functional programming has historically been less popular than imperative programming, but many functional languages are seeing use today in industry and education, including `Common Lisp`, `Scheme`, `Clojure`, `Wolfram Language`, `Racket`, `Erlang` `OCaml`, `Haskell`, and `F#`.

functional programming is also key to some languages that have found success in specific domains, like `R` in statistics, `J`, `K` and `Q` in financial analysis, and `XQuery`/`XSLT` for `XML`. `domain-specific` declarative languages like `SQL` and `Lex`/`Yacc` use some elements of functional programming, such as **not allowing mutable values**. in addition, many other programming languages support programming in a functional style or have implemented features from functional programming, such as `Perl`, `PHP`, `C++11`, `Kotlin`, and `Scala`.

## versus

## imparative vs procedural

**imperative programming** means that the computer get a list of commands and executes them in order, when **procedural programming** (which is also imperative) allows splitting those instructions into procedures (or functions).

## declarative vs functional

in practice, these two concepts tend to align, but it is entirely possible to write `an expression involving composition of pure functions that describe an explicit process to perform a computation` (**functional, but not declarative**), and it is possible to write `sequential, impure, code that describes constraints on an intended result rather than a process for obtaining it` (**declarative, but not functional**).
</details>
<details><summary><strong>lock, mutex, and semaphore</strong></summary><br>

a **lock** allows only one thread to enter the part that's locked and the lock is not shared with any other processes.

a **mutex** is the same as a lock but it can be system wide (shared by multiple processes).

a **semaphore** does the same as a mutex but allows x number of threads to enter, this can be used for example to limit the number of cpu, io or ram intensive tasks running at the same time.

[resource](https://stackoverflow.com/questions/2332765/lock-mutex-semaphore-whats-the-difference)

## mutex vs semaphore (the toilet example)

**mutex:**<br>
is a key to a toilet. one person can have the key - occupy the toilet - at the time. when finished, the person gives (frees) the key to the next person in the queue.

officially: "mutexes are typically used to serialise access to a section of re-entrant code that cannot be executed concurrently by more than one thread. a mutex object only allows one thread into a controlled section, forcing other threads which attempt to gain access to that section to wait until the first thread has exited from that section." *ref: Symbian Developer Library*

*(A mutex is really a semaphore with value 1.)*

**semaphore:**<br>
is the number of free identical toilet keys. example, say we have four toilets with identical locks and keys. the semaphore count - the count of keys - is set to 4 at beginning (all four toilets are free), then the count value is decremented as people are coming in. if all toilets are full, ie. there are no free keys left, the semaphore count is 0. now, when eq. one person leaves the toilet, semaphore is increased to 1 (one free key), and given to the next person in the queue.

officially: "a semaphore restricts the number of simultaneous users of a shared resource up to a maximum number. threads can request access to the resource (decrementing the semaphore), and can signal that they have finished using the resource (incrementing the semaphore)." *Ref: Symbian Developer Library*

[resource](http://niclasw.mbnet.fi/MutexSemaphore.html), [mirror](https://stackoverflow.com/questions/62814/difference-between-binary-semaphore-and-mutex/346678#346678)

</details>
<details><summary><strong>paradigm</strong></summary><br>

a paradigm is a set of rules and regulations that does two things:
1. it establishes and defines boundaries; and
2. it tells you how to behave inside those boundaries to be successful.

words that represent subsets of the paradigm concept: theory, model, methodology, principles, standards, protocol, routines, assumptions, conventions, patterns, habits, common sense, conventional wisdom, mind-set, values, frames of reference, traditions, customs, prejudices, idealogy, inhibitions, superstitions, rituals, compulsions, addictions, doctrine, dogma.

words like culture, organization, worldview, business, education did not appear because they are forests of paradigms.

*Discovering the Future: The Business of Paradigms, Joel Arthur Barker*
</details>
<details><summary><strong>recursions and recursive functions</strong></summary><br>

`recursion` is a way of programming or coding a problem, in which a function calls itself one or more times in its body. usually, it is returning the return value of this function call. if a function definition fulfils the condition of recursion, we call this function a `recursive` function.

**termination/stopping condition**:
a recursive function has to terminate to be used in a program. a recursive function terminates, if with every recursive call the solution of the problem is downsized and moves towards a `base case`. a base case is a case, where the problem can be solved without further recursion. a recursion can lead to an infinite loop, if the base case is not met in the calls.

[resource](https://www.python-course.eu/recursive_functions.php)

</details>
<details><summary><strong>referential transparency</strong></summary><br>

an expression is called referentially transparent if it can be replaced with its corresponding value without changing the program's behavior. This requires that the expression be pure, that is to say the expression value must be the same for the same inputs and its evaluation must have no side effects. An expression that is not referentially transparent is called referentially opaque.

</details>
<details><summary><strong>scalability, fault-tolerance</strong></summary><br>

**scalability** is the property of a system to handle a growing amount of work by adding resources to the system.

**fault-tolerance** is the property that enables a system to continue operating properly in the event of the failure of (or one or more faults within) some of its components.

</details>
<details><summary><strong>scope and closure</strong></summary><br>

  **scope** defines what variables you have access to.

  whenever you create a function within another function, you have created a **closure**. the inner function is the closure. this closure is usually returned so you can use the outer function’s variables at a later time.

</details>
<details><summary><strong>serial, parallel, sequential, and concurrent</strong></summary><br>

**concurrency** means, essentially, that `task A` and `task B` both need to happen independently of each other.

there are various different ways of accomplishing concurrency. one of them is **parallelism**. having multiple CPUs working on the different tasks at the same time. but that's not the only way. another is by task switching, which works like this: `task A` works up to a certain point, then the CPU working on it stops and switches over to `task B`, works on it for a while, and then switches back to `task A`. if the time slices are small enough, it may appear to the user that both things are being run in `parallel`, even though they're actually being processed in **serial** by a multitasking CPU.

**sequential** in other hand, means, that `task B` depends on the result of previous task, for example `task A`.

concurrent statements can be parallelized but sequential statements cannot be parallelized.

**resources:**
- [stackexchange concurrent vs parallel](https://softwareengineering.stackexchange.com/questions/190719/the-difference-between-concurrent-and-parallel-execution)
- [blogspot serial vs parallel vs concurrent vs sequential](http://s1l3n0.blogspot.com/2013/04/serial-vs-parallel-sequential-vs.html)

</details>
<details><summary><strong>statically/dynamically strongly/weakly typed</strong></summary><br>

*there is no universally accepted definition of what these terms mean*

**Static/Dynamic Typing is about when type information is acquired**
- a language is statically-typed if the type of a variable is known at compile-time instead of at run-time.
- a language is dynamically-typed if the type of a variable is checked during run-time.

**Strong/Weak Typing is about how strictly types are distinguished** whether the language tries to do an implicit conversion from strings to numbers.
- a strongly-typed language is one in which variables are bound to specific data types, and will result in type errors if types do not match up as expected in the expression — regardless of when type checking occurs.
- a weakly-typed language on the other hand is a language in which variables are not bound to a specific data type; they still have a type, but type safety constraints are lower compared to strongly-typed languages.

![languages by type system chart](./assets/type_dynamic_static_strong_weak.png)
[resource](https://android.jlelse.eu/magic-lies-here-statically-typed-vs-dynamically-typed-languages-d151c7f95e2b)

</details>
<details><summary><strong>symmetric and asymmetric multiprocessing</strong></summary><br>

![multiprocessing symmetric vs asymmetric](./assets/multiprocessing_symmetric_vs_asymmetric.jpg)

**symmetric multiprocessing** (`SMP`) involves a multiprocessor computer hardware and software architecture where two or more identical processors are connected to a single, shared main memory, have full access to all input and output devices, and are controlled by a single operating system instance that treats all processors equally, reserving none for special purposes. most multiprocessor systems today use an SMP architecture. in the case of multi-core processors, the SMP architecture applies to the cores, treating them as separate processors.

**asymmetric multiprocessing** (`AMP`) system is a multiprocessor computer system where not all of the multiple interconnected central processing units (CPUs) are treated equally. for example, a system might allow (either at the hardware or operating system level) only one CPU to execute operating system code or might allow only one CPU to perform I/O operations. other AMP systems might allow any CPU to execute operating system code and perform I/O operations, so that they were symmetric with regard to processor roles, but attached some or all peripherals to particular CPUs, so that they were asymmetric with respect to the peripheral attachment.

asymmetric multiprocessing was the only method for handling multiple CPUs before symmetric multiprocessing (SMP) was available. it has also been used to provide less expensive options on systems where SMP was available. additionally, AMP is used in applications that are dedicated, such as embedded systems, when individual processors can be dedicated to specific tasks at design time.

basis of comparison | symmetric | asymmetric
---|---|---
basic | each processor run the tasks of operating system | only `master` processor run the tasks of operating system
process | processor takes processes from a common ready queue, or there may be a private ready queue for each processor | master processor assign processes to the slave processors, or they have some predefined processes
architecture | all processor has the same architecture | all processor may have same or different architecture
communication | all processors communicate with another processor by a shared memory | processors need not communicate as they are controlled by the master processor
failure | if a processor fails, the computing capacity of the system reduces | if a master processor fails, a slave is turned to the master processor to continue the execution. if a slave processor fails, its task is switched to other processors
ease | is complex as all the processors need to be synchronized to maintain the load balance | is simple as master processor access the data structure

**symmetric multiprocessing** has proper **load balancing**, better **fault tolerance** and also reduces the chance of CPU **bottleneck**. it is complex as the memory is shared among all the processors.

**resources:**
- [wikipedia symmetric multiprocessing](https://en.wikipedia.org/wiki/Symmetric_multiprocessing)
- [wikipedia asymmetric multiprocessing](https://en.wikipedia.org/wiki/Asymmetric_multiprocessing)
- [techdifferences symmetric vs asymmetric-multiprocessing](https://techdifferences.com/difference-between-symmetric-and-asymmetric-multiprocessing.html)

</details>
<details><summary><strong>taxonomy</strong></summary><br>

taxonomy is the practice and science of classification of things or concepts, including the principles that underlie such classification.
</details>
<details><summary><strong>two-phase commit protocol</strong></summary><br>

**`coordinator`**
- `multicast` => `ok to commit?`
  - `collect replies`
    - `all ok` => `send commit`
    - `else` => `send abort`

**`participant`**
- `ok to commit` =>
  - `save to temp area`
  - `reply ok`
- `commit` =>
  - `make change permanent`
- `abort` =>
  - `delete temp area`

[educative](https://www.educative.io/edpresso/what-is-the-two-phase-commit-protocol), [shekhargulati](https://shekhargulati.com/2018/09/05/two-phase-commit-protocol/)

</details>
<details><summary><strong>variable shadowing</strong></summary><br>

**shadowing** is the term used to describe the act of defining a new variable that has the same name as one that was in the parent scope.

    Fn =
      fun() -> A = 1,
        fun(A) -> A = 2 end
      end.

    (Fn())(2).
    -> 2

</details>
