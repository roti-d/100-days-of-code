# 100 Days Of Code - Log

### Day 0: July 4, 2022 (Monday, holiday)

**Today's Progress**: Studied AWS solution architect associate; started 100 days of code in Python

**What I learned**:
- AWS lambda function
  - Can be invoke synchronously (using CLI or API gateway), asynchronously (by other AWS services) or via event source mapping (e.g. aws kinesis, dynamoDB)
  - Function-as-servce produce: A piece of code that run in a runtime environment, users only have to specify the memory and don't have to manage the servers. 
  - Lambda times out in 15 mins (900s).
  - Lambda function needs to be stateless.
  - Public lambda can access everything in the internet but not things in VPC. 
  - Private lambda behaves just like other AWS services within VPC.
  - Lambda needs to assume execution role as well as have resource policy (for other service to invoke lambda).
  
- Serverless architecture
  - users don't manage any severs
  - Applications only bill when they are running.
  - Mostly FasS products like lambda
  - Applications are ephemeral and stateless. 
 
- SNS
  - SNS = simple notification service
  - regional resilience
  - Pub-sub service
  - Producers send events to TOPICS
  - Consumers consume events from TOPICS
  - TOPICS uses resource policy to control permission; and config cross account access.
  - Support delivery retry, delivery status and server side encryption (SSE).

- Python
  - started coffee machine project
  - installed Pycharm.

**Thoughts:** I miss coding, especially the feeling of learning and using my brain. I pretty much have forgotten everything I learned in the past; I had to look up how to define functions, how to write if...else statements; but that's okay, that's part of the learning. I want to keep up with the learn and can't wait to see where I will be in 100 days. 

**Link to work:** 

### Day 1: July 5, 2022 (Tuesday)

**Today's Progress**: Finished off "Day 15 of 100 days of code - make a coffee machiine" project, watched 1-2 AWS videos

**What I learned**:
- Reminded myself of using while loop
- AWS step function: has state machine that allows users to run functions that are longer than 15 mins (tracks the state)

**Thoughts:** Didn't make much progress today as I wasn't feeling well. I was in bed pretty much the entire day. 

### Day 2: July 6, 2022 (Wed)

**Today's Progress**: Worked on OOP in python, finished rewriting the make coffee machine project in OOP (Day 16 lecture), finished AWS demo for setting up state machine with serverless architecture

**What I learned**:
- How to configure AWS to send emails and SMS
- How to configure state machine to trigger lambda function
- How to set up API gateway and REST API in AWS

**Thoughts:** Dealing with objects in python is tricky. Need more work. 

### Day 3: July 7, 2022 (Thurs)

**Today's Progress**: 
- Rewrite OOP coffee machine project that I was working on yesterday to get the object working. 
- Finished Day 17 of 100 days of code that uses OOP to create a quiz game.
- Watched AWS Kinesis videos
 

**What I learned**:
- How to define class in Python
- How to add attribute and methods to class
- More practice in how to write while loops
- Learned about Kinesis stream, Kinesis firehose and Kinesis analytics; and also AWS Cognito
  - Kinesis stream: use for data streaming, multiple producer and multiple consumers, real time
  - Kinesis firehose: near real time as data is batch into 60 seconds or 1MB buffer, support data transformation like Lambda; use for data persistent; can be sent to HTTP, Splunk, Redshift, Elastic Search or S3. 
  - Kinesis analytics: use for real time data processing using SQL

**Thoughts:** Feeling a bit more comfortable with coding in Python, this is fun.

### Day 4: July 8, 2022 (Fri)

**Today's Progress**: 
- Almost finish Day 18 of 100 days of code (Drawing using Turtle package in Python).
- Was stuck when drawing Spirograph
- Didn't make as much progress as I would like to as I went out last night with coworkers. It was fun though.
 
**What I learned**:
- Got more comfortable using the turtle modeules and writing functions / loops.  

**Thoughts:** Daily progress is important. Didn't log yesterday so have to do it today (Sat).


### Day 5: July 9, 2022 (Sat)

**Today's Progress**: 
- Wrapped up Day 18 (woke up with a much clear head and was able to do it pretty fast).
- Finished Day 19; using Turtle package to build a turtle racing game. 

**What I learned**:
- Learned how to have multiple turtles moving at the same time. 
- Learned about instances and object state.

**Thoughts:** This is fun!
