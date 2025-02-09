# Realtime-Bluetooth-Networks
Software - TI Rtos
Hardware - The hardware used was the TM4C123 Launchpad (Cortex M4F) and TI MKII Booster Pack. 

**Description** -
The fitness device records four parameters in real time.
That are steps, sound magnitude, temperature, light intensity.
Fitness device is connected to mobile over Bluetooth.
With a mobile Bluetooth app the fitness device is controlled.

Task rate are handled to keep all task rate maintained.

Round robin scheduler is used to maintain two periodic task and
four main task. Resource sharing is achieve with mutex and semaphore.

Change semaphore spinlock to blocking. Periodic task start on timer
interrupt. Put task in sleep. Use fifo queue for data flow between
producer task and consumer task.

Implement priority based scheduling. Signal semaphore with edge trigger
interrupt. Periodic task are assign high priority to reduce latency.

Write data to file.

**Reference** - 
Teaxs University UTAustinX-UT.RTBN.12.01x

**Parts of project** -
Part 1 - Introduction to RTOS
Part 2 - Thread Management
Part 3 - Blocking, Sleeping and FIFO Queues
Part 4 - Priority Scheduler
Part 5 - File Systems
