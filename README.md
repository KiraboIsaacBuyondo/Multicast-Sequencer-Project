# Multicast-Sequencer-Project
A Java-based program that enables multicasting of messages using a sequencer-based approach, implemented with Java RMI and multicast sockets.
## Project Overview
The goal of this project is to create a sequencer-based multicasting service. The sequencer ensures that the messages are delivered to the recipients in a specific order, providing reliable message ordering in a distributed environment.

## Key Features
**Multicasting:** Multiple users can send messages to a group of recipients simultaneously, enabling efficient communication within a distributed system.
**Sequencer:** The program employs a sequencer that guarantees the delivery of messages in a specific order, ensuring consistency among the recipients.
**Classes:**
- TestSequencer.java: Allows users to enter messages and sends them to a group of TestSequencer instances. It can also stress-test the system by sending messages rapidly.
- Group.java: Provides group communication services. TestSequencer uses an instance of this class. It uses multicast sockets to receive incoming messages and communicates with the sequencer using RMI.
- Sequencer.java and SequencerImpl.java: Define the interface and implementation of the sequencer.
- History.java: Keeps track of the sequencer's history. It dynamically removes old entries when it exceeds a certain threshold.

  ## Project Setup
Follow these steps to set up and run the project:
- Ensure that the rmiregistry is running.
- Compile all the classes by executing javac *.java.
- Start the server by running java SequencerImpl.java.
- Start the TestSequencer clients. For example, run java TestSequencer localhost Client1, java TestSequencer localhost Client2, and so on.

Feel free to contribute to the project by submitting pull requests or reporting issues.
