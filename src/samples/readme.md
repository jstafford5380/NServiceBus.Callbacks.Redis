## Demo Instructions
- You must be running Redis locally on port 6379. I recommend just running it in docker, but as long as it's reachable, it should be fine.
- Make sure that Reciever and Sender1 are set as startup projects and then run all three at the same time.
- Observe the console windows for Sender1. It is waiting for you to press enter before they send the commands to the Receiver. This is just to make sure the receiver is running first. Feel free to manipulate this any way that makes sense for testing.
- When the sample is finished, it shows that each instance of the bus only processed the message that it was expecting. This is seen by the difference in the instance IDs.
- NSB will output an exception saying it couldn't find a file. This is just flaw in the LearningTransport. Feel free to reconfigure this to use a real transport such as RabbitMQ and the error shouldn't occur. I've included the setup for RMQ, just uncomment the setup and comment out the learning transport lines in the sender and receiver projects.