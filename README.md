# CPU Scheduler and Java System Simulations

This repository contains a set of Java programs focused on operating-system-style scheduling and concurrency problems.

## Project overview

The repo includes:

- `scheduler/`: a Maven project implementing several CPU scheduling algorithms and validating them with JSON-based test cases.
- `Terminal.java`: a lightweight terminal/shell simulation that supports basic filesystem operations and command parsing.
- `ServiceStation.java`: a multithreaded service-station simulation using semaphores to model waiting cars, pumps, and service bays.

## Included scheduling algorithms

The scheduler project evaluates and compares:

- Shortest Job First (SJF)
- Round Robin (RR)
- Preemptive Priority Scheduling
- AG Scheduling

These implementations calculate process metrics such as:

- waiting time
- turnaround time
- execution order
- average waiting time
- average turnaround time

## Repository structure

```text
.
├── README.md
├── ServiceStation.java
├── Terminal.java
└── scheduler/
    ├── pom.xml
    ├── src/
    │   └── main/java/com/scheduler/Main.java
    └── test_cases/
```

## Running the scheduler tests

From the `scheduler` directory:

```bash
mvn test
```

This compiles the project and runs the JUnit test suite that validates the scheduling logic against the bundled JSON test cases.

## Running the terminal simulation

Compile and run the custom terminal implementation from the repository root:

```bash
javac Terminal.java
java Terminal
```

## Running the service station simulation

Compile and run the semaphore-based service station model from the repository root:

```bash
javac ServiceStation.java
java ServiceStation
```

## Notes

- The scheduler project uses Maven and depends on `org.json` and JUnit 5.
- The root-level Java files are standalone examples and can be compiled independently.
- This repository is intended as a learning project for process scheduling, queueing, and synchronization concepts.
