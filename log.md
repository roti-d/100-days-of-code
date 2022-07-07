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

