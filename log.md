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

### Day 6: July 10, 2022 (Sun)

**Today's Progress**: 
- Finished Cloudfront (CDN) section of the AWS course
- Half way for Day 20 of 100 days of code, writing snake game

**What I learned**:
- Cloudfront is the AWS version of global CDN.
- There are two types of connections in cloudfront: client to edge location, and edge location to origin
- Origin type can be S3 buckets or custom origin.
  - To secure S3 connection, use OAI (origin access identity)
  - To secure custom origin, use firewalls around origin or custom header.
- Global accelerator is a network product; goal is to get requests onto AWS network ASAP. 

**Thoughts:** Not too bad, not as much progress as I would like to, but still not bad. Keep it up! Getting AWS certified and becoming VERY GOOD at python would set up me in becoming a software developer / devops or a very good TPM.

### Day 7: July 11, 2022 (Mon)

**Today's Progress**: 
- Finished day 20 of 100 days of code to build a snake game.
- It wasn't suppose to take that long, but I was playing around with it to make the snake move around, the add target and increase the length of the snake whenever it meets the target.
- Watched two AWS videos.

**What I learned**:
- Refresher on how to create object.
- Read a bit on object inheritance and lambda funcition.
- Egress-only internet gateway: 
  - is for IPv6 as NAT gateway doesn't work for IPv6. 
  - Egress-only gateway allows traffic going out but block external initated traffic. 
- VPC flow logs:
  - captures traffic in and out VPC, only logs metadata like source & dest IP address, port number, packet size but not the packet content.
  - Flow logs destination can be S3 or Cloudwatch logs (if S3, it can be queried by Athena).
  - Flow logs is NOT REALTIME. 
  - Flow logs can be set at different level: VPC, subnets or ENI (elastic network interface). 

**Thoughts:** Didn't have enough sleep last nigth so felt pretty slow today, but kind of manage to power through. Didn't work much though and feeling a bit stress about job search. Was a youtube video yesterday about "the shortest path of becoming a software engineer" is to learn AWS and Python..I think I'm on the right track, now just have to stick with it! 
- Goal for the month is to: Get AWS certified.
- Goal for the 3 month is to: Get very good with Python. (i.e. be able to contribute to open source project or take freelance job).

### Day 8: July 12, 2022 (Tue)

**Today's Progress**: 
- Completed Advanced VPC session in AWS course and did the VPC peering demo and interface endpoint, gateway endpoint and egress demo.

**What I learned**:
- VPC peering only connects TWO and Only TWO VPCs.
- VPC peering is not transitive, if more than 2 VPCs need to be connected, need to set up separate peering connection. 
- VPC peering can be same or cross account; and same or cross regions.
- For VPC peering in the same region, the VPC can refer to each other's SGs. For cross region, needs to refer to IP or IP ranges. 
- how does VPC peering work? Logical gateway is set up in each VPC; and thus needs to configure route tables and SG and/NACL. 

**Thoughts:** Okay progress so far, definitely feel better today after getting more sleep. Probably need to start doing some practice exams and review to make sure I don't forget previous content. 
