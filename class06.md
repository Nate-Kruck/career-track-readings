# Class 06 Readings (Sept. 15th)

## Redis

- Redis, which stands for Remote Dictionary Server, is a fast, open-source, in-memory key-value data store for use as a database, cache, message broker, and queue.

### Benefits of Redis

- In-memory data store
- Flexible data structures
- Simplicity and easy to use
- Replication and persistence
- High availability and scalability
- Extensibility

### Redis Uses

- Caching
- Chat, messaging, and queues
- Gaming Leaderboards
- Session store
- Rich media streaming
- Geospatial
- Machine Learning
- Real-time analytics

## Queue

- A queue is another common data structure that places elements in a sequence, similar to a stack. A queue uses the FIFO method (First In First Out), by which the first element that is enqueued will be the first one to be dequeued.

### Basic operations of a queue

- Enqueue() — Inserts an element to the end of the queue

- Dequeue() — Removes an element from the start of the queue

- isEmpty() — Returns true if queue is empty

- Top() — Returns the first element of the queue

## Task Queues

- When handling requests from web clients, sometimes operations take more time to
execute than we want to spend immediately. We can defer those operations by putting
information about our task to be performed inside a queue, which we process later.
This method of deferring work to some task processor is called a task queue. 

## FIFO (first in first out queue)

- In the world of queues beyond task queues, normally a few different kinds of queues
are discussed—first-in, first-out (FIFO), last-in first-out (LIFO), and priority queues.

## Bull

- Bull is a Node library that implements a fast and robust queue system based on redis.

### Getting Started

- Bull is a public npm package and can be installed using either npm or yarn:

```
$ npm install bull --save
or

$ yarn add bull
```

- In order to work with Bull, you also need to have a Redis server running. For local development you can easily install it using docker.

- Bull will by default try to connect to a Redis server running on localhost:6379