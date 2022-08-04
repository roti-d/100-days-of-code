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

### Day 9: July 13, 2022 (Wed)

**Today's Progress**: 
- Had a pretty long day with work and interview, didn't get as much done as I wanted to. 
- Finished Day 21 of 100 days of code to finish off the snake game. 
- Started Day 22 to set up the Pong game, got the gameboard, scoreboard and the two players setup. Messing around with the balls and angles.

**What I learned**:
- How to pass in arguments when inheriting a class.

**Thoughts:** Not getting as much done as I would love to, but progress is progress :) 

### Day 10: July 14, 2022 (Thurs)

**Today's Progress**: 
- Had a long day of interviews and team match so didn't get too much time to study. 
- Finished off Day 22 of 100 days of code to finish off the pong game. 
- Finally got the ball to bounce right and got the scoring board to work. I watched the solution after building out the game myself and the solution was much simplier! I definitely overthink the ball bouncing logic and was trying to determine the incoming and outgoing angle. 

**What I learned**:
- A much simplier way to get the ball to bounce

**Thoughts:** Need to book the AWS exam soon, I wanna take it before mid-Aug, so at most one more month to go.

### Day 11: July 15, 2022 (Fri)

**Today's Progress**: 
- Another long day with team match calls and had to work a bit so didn't get much done.
- Started Day 23 of 100 days of code to build a Turtle crossing game.
- Got the turtle and cars to move but kind of "hack" together a way for making a stream of cars. This needs to be revised. 

**What I learned**:
- More practice in python.

**Thoughts:** Goal for python is to do a hackathon by the end of this year.


### Day 12: July 16, 2022 (Sat)

**Today's Progress**: 
- Finsihed day 23 of 100 days code to build the Turtle crossing game. Figured out a way to get the stream of the cars to work soon after I woke up :) 
- Finished day 24 of 100 days to read, write and merge files. 

**What I learned**:
- how to read, write and merge files in python.
- play around with Google gmail API; keep getting permission error, not wokring yet.

**Thoughts:** I probably need to spend a bit more time on AWS, will focus more on that.

### Day 13: July 17, 2022 (Sun)

**Today's Progress**: 
- Half way through the 25th days of code..learning about how data manipulation.
- Continue to watch the videos on AWS hybrid mode and migration.

**What I learned**:
- AWS site-to-site VPN: 
  - easies way to connect on-perm network with VPC
  - fast to set up (within an hour)
  - encryption via IPSec
  - run over public internet
  - latency: 1.25Gbps
  - Not HA by default as CGW can be a single point of failure
  - architecture: 
    - VPC and on-perm router
    - CGW (customer gateway)
    - VGW (vitual private gateway)=> has two physical endpoints that can be connected to CGW
    - Connection between CGW and VPG
- Direct connect (DX)
  - Takes weeks or months to set up
  - Usually people first set up site-to-site VPN while waiting for DX
  - Data no encrypted. 
    - To make it encrypted, instead of connceting to public VIPS, connect it with VGW endpoints then leverage IPSec encryption.
  - latency: 40 Gbps
  - Not HA by default as it involves many single physical failure point
  - architecture: 
    - AWS port in AWS site
    - Customer or partner port in AWS site
    - Fiber to connect AWS port and customer port
    - Fiber to connect customer port in AWS site to customer on-perm router
    - VIFS (virtual interfaces = one VLAN adn one BGP session on customer side
- Transit gateway (TGW)
  - Transit hub to connect VPCs and/or customer on-perm networks via attachments like peering, site-to-site VPN, DX. 
  - Simplify the network design a lot
  - HA by default
  - Support cross-region or cross account peering
  - For any AZs within VPC that wants to use TGW, each needs its own VPC attachment
  - Support static and dynamic routing. If dynamic routing is enabled, routes will be propagate to route tables use BGP (boarder gateway protocol) => only best route is communicated to other networks. 
- Snowball, Snowball Edge and Snowball mobile
  - all use for moving large amount of data in/out of AWS.
  - Snowball: 
    - data around 10TB to 10PB
    - suitcase size boxes mail to customer 
    - data is encrypted at rest
    - can be multiple site
  - Snowball edge:
    - data > 10PB
    - can be multiple site
    - Use when data neeeds to be processed upon ingestion or in a remote site
  - Snowball mobile
    - physical truck => only go to on-site and plug-in directly to data centers
    - need special order
    - data between 10PB to 100PB
- Storage gateway
  - use case:
    - Migration to AWS
    - Backup data (Tape or file)
    - Extending on-perm storage to AWS
  - Types:
    - File stored gateway
    - Volume stored / volume cached gateway
    - Tape stored gateway

**Thoughts:** Never give up!



### Day 14: July 18, 2022 (Mon)

**Today's Progress**: 
- Finsihed day 25 of 100 days of code, which builds a "Guess state name game" using Turtle. 
- Watched 2 AWS videos (AWS directory service and DataSync)

**What I learned**:
- Python:
  - How to use Turtle to show pictures.
  - Got some practice with Pandas DataFrame, played around with .loc
- AWS:
  - AWS directory service
    - What is directory? An inverted tree that stores identity objects (e.g. users, groups, servers etc.) Common ADs are Microsoft AD and SAMBER
    - Use by ITs to manage multi-device logins using same passwords
    - Some AWS services (e.g. Workspace) needs AD
    - Runs with in VPC as private service, can be deployed to multi-AZ.
    - Waht are the different types of AWS directory services? 
      - Simple AD: should be used by default
      - Microsoft AD: use when there is already an on-perm system and need full implementation of AD. 
      - AD connectors: use when only 1 or few AWS services need AD, AD connectors act as proxy. The primary AD still runs on-perm.
 - DataSync
    - Use for transferring data IN or OUT of AWS
    - Also stores metadata
    - Provides data validation by default
    - Use cases: Data backup, DR, migration to AWS, Data processing transfer
    - Supports scheduled backups or incremental backups.
    - Supports compression and encryption.
    - Pay as you use the product.
    - Can be single AZ or multi-AZ. 
    - Destination can be S3, EFS, FXs (for windows)
    - Design to support large quantity of data (different from Snowball products as those are physical transfer)
    - Support encryption by default
    - Users have ability to throttle the data transfer amount
    - Can be connected via VPC, direct connect, peering
    - Each DataSync agent can transfer up to 10GB/sec (~100TB per day)
    - Components:
      - DataSync agent
      - On-perm file system
      - Destination (S3, EFS, VPC etc.)

**Thoughts:** Not a bad day given I had 3 interviews today. need to protect my morning hours for learning as I tend to get very tired and lose my focus after Noon. 



### Day 15: July 19, 2022 (Tue)

**Today's Progress**: 
- Finsihed day 26 of 100 days of code, which talks about list and dictionary comprehension.
- Finished the AWS section on Hybrid architecture.

**What I learned**:
- Python:
  - List and dictionary comprehension. 
  
- AWS: 
  - AWS FXs for Window
    - Fully managed file share, similar to RDS
    - Can be connected with on-perm AD or AWS directory service
    - Can be multi-AZ or single AZ
    - Support on-demand backup or incremental backup
    - Support file level versioning
    - Can be access via VPC, Peering, Direct conncet or VPN
    - Access to native file system via SMB (Server message block)
    
  - AWS FXs for Lustre
    - Fully managed file system for linux, support POSIX
    - How does this different from EFS? AWS FXs for Lustre is mostly use for workloads that require heavy compute (e.g. ML, financial modeling)
    - Highly perforamnce 
    - Has two modes: 
      - Scratch: fast, but no replication
      - Persistent: has replication, but only within 1 AZ
    - File system => place where data lives when processing
    - (Optinoal) S3 bucket to backup data
    - Can be access via VPN or direct connect
    - [Link](https://tutorialsdojo.com/amazon-efs-vs-amazon-fsx-for-windows-vs-amazon-fsx-for-lustre/)
    
  - AWS secret manager
    - Place where secrets (Passwords/ API etc) are stored
    - Supports key rotation
    - Keys encrypted using KMS
    - Connected to some AWS services like RDS (when key rotates, credentials in RDS also get updated) 

**Thoughts:** Not a bad day given I had 3 interviews today. need to protect my morning hours for learning as I tend to get very tired and lose my focus after Noon. 


### Day 16: July 20, 2022 (Wed)

**Today's Progress**: 
- Finsihed day 27 of 100 days of code, which uses a new package (Tkinter) to build GUI. 
- Started to look into AWS practice exams on Tutorials-Dojo but didn't make much progress

**What I learned**:
- Python:
  - Tkinter: how to add buttons, labels, inputs to GUI; how to position widget in the UI using grid(), pack() and place().
  
- EC2:
  - Default only allows 20 instances within the same region, but this can be lifted if file tickets to AWS. 
  - EC2 on-demand instances doesn't provide reservation and need to pay the instance even when it's not running.
  - EC2 on-demand capacity reservation reserve capacity and charge for the instance on the specified recurring schedule. (e.g. good for batch jobs).

**Thoughts:** 
- Need to do a better job at keeping this journel and instead of writing it the day after. I will try to write this every nighit. 
- Need to put in more time in reviewing AWS, feel like I have forgotten all the previous topics. 

### Day 17: July 21, 2022 (Thurs)

**Today's Progress**: 
- Finished AWS security related videos. 
- Started day 28 of 100 days of code, which uses Tkinter to build a pomodoro. Didn't watch any of the initial promopt and was struggling quite a bit as I couldn't get the counter to work in Tkinter. The counter works fine just as a function itself, but not able to update the label accordingly. 


**What I learned**:
- Python:
  - More practice with Tkinter.
  - Learned about mainloop() and after()..still not very clear though
  
- AWS security products:
  - AWS Shield: 
    - Protect against DDOS attack, Layer 3 and layer 4
    - Understand HTTP, HTTPS and TCP
    - Comes in (1) Free with Route 53 and CloudFront (2) Paid - $3000 per month with EC2,ELB,Cloudfront,Route53 and global accelerator; paid version comes with insurance and incidents response team.
  - AWS WAF (web applciation firewall)
    - Layer 7 protection, can be integrated in ALB, Cloudfront and API gateway using WEBACL (web access control list)
    - Protect against more sphosicated attacks, e.g. SQL injection, cross-site scripting
    - WAF has geo blocks and rate awareneess
  - CloudHSM
    - Different than KMS as AWS doesn't own the key at all. 
    - CloudHSM is genereated in a physical location and can be uesd as the custom KMS.
    - Meets FIPS 140-2 Level3 security standard; KMS is only level2.
    - CloudHSM uses industry standard APIs - PKCS#11, JCE and CryptoNG
    - CloudHSM is the right choice for any non-AWS product that needs HSM. 
  - AWS Config
    - Stores changes related to resources (e.g. Security group of S3 bucket changes)
    - Doesn't protect against the change but can trigger runs to SNS, EventBridge and Lambda
    - Regional service, support cross-region and cross account aggregation
  - AWS Macie
    - Use ML to detect PII/ PHI/ Financial data in S3 buckets
    - Have AWS managed rules or custom data identifiers
    - Generate findings that can be sent to EventBridge or console
    - Is Centrally managed in AWS ORG account or in one Macie accoutn and invite others
  - AWS Inspector
    - Scan EC2 and ECS OS for vulnerabilities and deviation against best practices
    - Check for Network reachability E2E (no agent required)
    - Check for CVS, CIS and Security best practice (required agent)
  - AWS Guardduty
    - Detect suspicious account activity

**Thoughts:** 
- Took it a bit easy last ngiht to spend some time with DJ, so didn't study too much. Also worked a bit more, need to find more time and be more focus. Also started re-watching Jim Kwik's focus course. I have been listening to Brain.fm when working, seems like it helped with my focus. 

### Day 18: July 22, 2022 (Fri)

**Today's Progress**: 
- Finished day 28 of 100 days of code, which uses Tkinter to build a pomodoro. Finally got the pomodoro to work without watching any promopt. Figured out that i need to use time.sleep() and window.update() to get the label updated. I thought I tried it yesterday but not sure why it didn't work.


**What I learned**:
- Python:
  - More practice with Tkinter.
  - How to get the counter working using Tkinter.
  

**Thoughts:** 
- I used this morning usual study time to work so have to study in the evening. Not ideal but happy that I'm making some progress and more importantly showing up every day.
- Did 3 team match calls today and had lots of back-to-back meetings so was a bit tired. Feeling good that I still show up for study :) 

### Day 19: July 23, 2022 (Sat)

**Today's Progress**: 
- Watched the videos for day 28 of 100 days of code. Have more understanding of how tkinter.after() works and found out how to stop the .after loop, which is to call .after_cancel().
- Finished day 29 of 100 days of code to build a password manager. I built the whole thing before watching the video and even built a way to retrieve the password. It was really fun.


**What I learned**:
- Python:
  - More pracetice with list comprehension. [new item for item in list] 
  - More practice with pandas and how to write / read from files.
  - Tkinter:
    - How .after works and how to break out of the .after loop by calling .after_cancel. 
    - grid(): how to create columns that span across more than 1 column by specifying columnspan
    - Add and remove boarders 
    - Show popup box
  
**Thoughts:** 
- Coded for a bit over 5 hours today; not bad. 
- Going to pick up on AWS stuff. 


### Day 20: July 24, 2022 (Sun)

**Today's Progress**: 
- Finished day 30 of 100 days of code which talks about error handling; and build upon the previous NATO project and password manager project.
- Watched a few videos in AWS cloudformation.


**What I learned**:
- Python:
  - How to handle JSON data using JSON.load,JSON.dump and JSON.update.
  - Review error handling (try, except, else and finally).
- AWS:
  - Cloudformation:
    - Templates can be portable and non-portable. 
    - Reason some templates are non-portable can be: have hardcoded S3 bucket name or have AMI names and trying to use the template in other region.
    - Tempalte specify logical resources where AWS will use it to create physical resources.
    - Cloudformation has template parameters (specify by user), Peusdo parameter (inject by AWS) and has Intrinsic function which allows users to reference runtime variables. 
    - Mappings allow user to look up variables.
    - Output: the output message that user will see in console or CLI. 
  
**Thoughts:** 
- Today was okay. This afternoon went to Raz house so didn't have the full day to study. A bit stressed about work and tomorrow's meeting with X, not sure what to expect but I guess I will do my best and not set any expectation. 


### Day 21: July 25, 2022 (Mon)

**Today's Progress**: 
- Started day 31 of 100 days of code which builds a flashcard app. I think I got like 60% done - has UI setup and basic functionality to flip the card on click.


**What I learned**:
- Python:
  - How to update image and text in canvas - Tkinter.
 
**Thoughts:** 
- Didn't get as much study done as I would like to (~1 hour python). Been working a lot today, so will catch up tomorrow! Met with Sulil from X today and had a really good chat. Seems like a great oppotunity to work on and great leader to learn from. Beyond grateful to be this lucky to have a chat with them.

### Day 22: July 26, 2022 (Tue)

**Today's Progress**: 
- Finished day 31 of 100 days of code which builds a flashcard app. Got all the functionality done before watching the solution videos. The hardestk part was to figure out how to wait for 3 seconds when the card is showing french and to wait for user click when the card is showing eng. I also added the ability to randomly insert words that user got wrong back into the stack and be able to save process on exit.


**What I learned**:
- Python:
  - How to trigger actions on tkinter exit
  - Lambda functions: use as functions when some variables are unknown.
 
**Thoughts:** 
- So far studied for ~2 hours on python. Will try to get some work done on AWS later on. :) 

### Day 23: July 27, 2022 (Wed)

**Today's Progress**: 
- Started day 32 of 100 days of code which sends email. Been stuck again with gmail outh, but I know I will figure it out. 
- Watched a few AWS videos on cloudformation.

**What I learned**:
- AWS:
  - DependsOn
    - Most of the time AWS can tell what resources need to be created before other resources, but sometimes this dependency is implicit. E.g. Elastic IP depends on Internet gateway attachment, but Internet gateway attachment depends on first creating "Internet gateway and VPC".
  - Condition
    - Condition is evaluated first before stack creation to determine what type of resources need to be created (e.g. for prod env, use Z1d EC2; for test env. use T1 micro).
  - CreationPolicy and WaitCondition
    - Why do we need this? After CFN creates a stack, it doesn't know whether or not all bootstrap has been completed. It only knows whether or not the EC2 was provisioned successfully. 
    - CreationPolicy ties to resource creation => when to create certain resources?
    - WaitCondition: more general -> explicitly define how long a resource should wait before timing out or how many sucess CFN should receive before marking the stack as completed.
  - Nested stack vs. cross-stack references
    - Cloudformation stacks is by default self contained and isolated.
    - Resources cannot be referenced outside the stack. 
    - Nested stack: have stacks nested within the root stack; resources can be referenced using "Output". All share the same lifecycle.
    - Cross-stack reference: stacks are referencing the same resources using !input and export instead of !ref. can have different lifecycle. 
  - stackset: 
    - use to create stacks in different account and region. 
    - control by one single account (admin account) and stacks are created in target account.
    - stacksets are just containers for stack instnaces, and stack instances are just containers of reference to one stack in one region.
    - permission
 
**Thoughts:** 
- Today was alright, didn't do as much but not too bad. AWS: 1 hour 20 mins, Python: 52 mins.


## Day 24: July 28, 2022 (Thurs)

**Today's Progress**: 
- Still working on day 32 of 100 days of code which sends email. Found a tutorial for using Gmail API; and successfully sent the first email. Been stuck with permission error for a while.
- Watched one video on Deletion policy.
- Watched two rapid learner video on getting started. 

**What I learned**:
- AWS:
  - Deletion policy:
    - when a stack is deleted, all physical resources are deleted, which might lead to data loss.
    - Deletion policy allows users to specfy what to do with each resources. Options:
      - delete (default)
      - retain
      - snapshot (only available for EBS, RDS, Redshift, ElasticCache; not EC2, not S3)
- Rapid learner:
  - Top 10 things about learning:
    - Recall not review. 
    - Space out time, don't cram information
    - Don't memorize something that needs to be understood.
    - Practice closer to what actually needs to be done.
    - Paraphrase and summarize => don't highlight
    - Transform to remember: process the infomation and put my own spin in it (e.g converting into mindmap)
    - Be comfortable with frustration
    - Maintenance Review goes a long way
    - Sleep
    - Be curious
  - Have a project plan
    - Define goal
    - Identify material
    - Estimate time required
    - Set deadlines and milestones
    - Put together week to week plan
    - Update the plan every week
- Python
  - very high level how to auth to googleAPI
  - Oauth2 token and serivce account
    - Oauth2 token: allow users to login using loginID and passwords
    - Servcei account: for bots to perform actions using Oauth2.
 
**Thoughts:** 
- Didn't do much today as my mind kept thinking about Coinbase vs. X offers and been talking to various folks to get advice. Was a bit anxious. 
- Got the googleAPI working but don't think I fully understand it, so going to spend a little more time on it. 
- Started to also watch the Rapid learners video, which I think was pretty good. 
- Time spent: AWS - 15 mins, python - 55 mins.

## Day 25: July 29, 2022 (Fri)

**Today's Progress**: 
- Still working on day 32 of 100 days of code which sends email. Found a way to get around the "Less secure App" in Gmail using App password, which allows me to send email using SMTP.

**What I learned**:
- Thinking in Bets (book)
  - Resulting - a phenomenal where decision quality != decision outcome, and people cannot differentiate between the two. 
  - Game theory can be applied to many things in life.
  - Poker is a game as it involves a luck factor, whereas chess is not. 
- Python
  - App password 
  - Send email using SMTP
 
**Thoughts:** 
- Again didn't do much today as I was negotiating the salary with X and chatted with Coinbase. Finally accepted the offer. Felt like a big relief. 
- Now really have to double down and get back to studying. :)

## Day 26: July 30, 2022 (Sat)

**Today's Progress**: 
- Finally finished day 32 of 100 days of code which sends email. Coded two apps, one to send birthday wishes by going through a csv file using pandas; another one to send motivation quote every Monday.
- Watched a few videos on AWS. Finally finished Cloudformation section and started on Dynamo DB. 

**What I learned**:
- Thinking in Bets (book)
  - Everything in life is like making a bet. Most of the time, you are betting against a future version of yourself. You are evaluating whether this version of yourself would be better than the alternative. 
  - Many people don't natually think this way; and have a bias towards believe everything they see/hear. 
  - By prompting "want to bet?" makes people evaluate their beliefs. 
  - We cannot make decision objectively, but at least we should try. 
  - We should redefine confidence and think in terms of probability. I'm X% certain that Y will happen; instead of saying I'm sure Y will happen. This gives people around us ways to correct us when we are wrong as well as not making ourseleves feel bad when we get it wrong.  
- Python
  - How to use scheduler modudle to have the script run periodically
  - Run code using pythonanywhere (although I didn't quite get it to work.)
  - Dictionary can be used a key for another dictionary (e.g (day, month): row_of_data)
- AWS
  - cnf-init: an alternative way of bootstrapping; uer define desired state instead of providing instructions. 
  - cfn-hup: given cfn-init only runs at launch, cfn-hup watches changes to the metadata and call cfn-init when changes are detected.
  - ChangeSet: allow users to first preview the changes before applying to the cfn stack; users can create many "versions" and only apply the ones they want.
  - Custom resources: allow users to perform actions that AWS doesn't support natively or intergrate with 3rd party. THis is done by invoking lambda function or SNS topics. Example:
    - Load pics into S3 bucket at launch
    - Delete S3 bucket that contains image
  - DynamoDB, key feature:
    - NoSQL, use to start key/value pairs or documents
    - Database-as-a-service product, users don't have to worry about infra/server
    - Highly resilient: automatically backup in multiple nodes across AZs, can be configured to be gloabbly resilient. 
    - Can be provisioned with capacity or pay on-demand
    - Very fast (single digit milliseconds, based on SSD)
    - Support encryption at rest
    - Support point-in-time recovery and manual backup
    - Support event driven 
    - Users only pay for the resources they consume (storage used, RSU, WSU)
      - 1 RSU = read 4KB data/ sec
      - 1 WSU = write 1KB data/sec
    - Capacitity has direct impact on speed
  
  
 
**Thoughts:** 
- Feeling a bit sleepy all day so didn't do as much as I wanted, but still making some progress, so not bad. 
- A bit tempted to start learning the coursera course on AI. Let me think through whether or not I should. I want to make sure I follow through, but at the same time want to start learning for the new role. 


## Day 27: July 31, 2022 (Sun)

**Today's Progress**: 
- Finished all the lectures in the SAA course. 
- Watched 1 video on Day 33 of 100 days of code that talks about API. 

**What I learned**:
- AWS
  - DynamoDB:
    - Backup options:
      - on-demand backup
      - point-in-time backup: allow play back to 1 second granularity, default data retention 35 days
    - Consistency: can be eventual consistent or strong consistent
      - eventual consistent is 50% cheaper
      - Use Master and salves nodes 
      - DynamoDB automatically replicates data in multiple AZs (can config to global)
    - Performance: directly tie with capacity
      - can be paid on demand or provision resources
      - on demand is 5x more expensive
      - the minimum unit is 1 RSU or 1 WSU (round up)
    - Operations: support query and scan
      - query: more efficient, retrieve the whole row; users need to paid for all data retrieved even for those that are filtered out later on.
      - Scan: expansive, pay for all data scanned.
    - Secondary Indexes: create another way for users to access data; e.g. for another team => making data retrieval more efficient and cost effective
      - Local secondary index (LSI)
        - strong consistency
        - user defines another sort key
        - user can only create LSI at table creation
        - a table can have up to 5 LSI
        - share RSU and WSU with the base table
      - Gloabl secondary index (GSI)
        - eventual consistency
        - user defines another primary key and sort key
        - user can create GSI at anytime
        - a table can have up to 20 GSI
        - use their own RSU and WSU 
    - Streams & lambda
      - generate events whenever there is data change in dynamoDB 
      - 24 hours window
      - output can be stored in S3 with records of what data has changed
      - different types of records:
        - New image (record only current state)
        - old image (record only old state)
        - key_only (record only primary and secondary key of the table)
        - new and old image
      - a Lambda function of SNS topics can be triggered to act on the event
    - Global table
      - eventual consistent
      - multi-master model
      - data is replicated within sub-seconds
      - last-write wins
      - provides global HA and global DR/BC
    - DAX (DynamoDB Accelerator)
      - DynamoDB built-in in-memory cache
      - Much less admin overhead
      - write through cache
      - has read-write replicas
      - support item cache and query cache
        - item cache: cache the whole "row"
        - query cache: cache the user query+ output
      - HA
      - Deployed within VPC, needs additional configuration to be used for services outside VPC
    - Athena
      - allow users to query S3 data by providing a schema
      - schema-on-read
      - the original data in S3 remains unchanged
      - Good for ad-hoc use cases
      - Can read data directly from EBS logs, cloudtrail and flow logs. 
    - Elasticache
      - in memory cache
      - Supports redis and memcached
      - Need application code change
      - Support Aurora (not just dynamoDB)
    - Redshift
      - Database query product
      - Use JDBC/ODBC connections
      - Redshift spectrum: query Redshit without first loading data into the database
      - Federation query: allow Redshift to query other data base
      - Support OLAP data (column based; for analytics); usually gets data from OLTP (transactions / rows)
      - Use for data aggregation or analysis
      - Need provisioning
      - Not good for ad-hoc query
      - Run in single AZ in a VPC (user can enable Enhanced VPC routing)
      - Data is automatically backup in S3 every 8 hours or 5GB
- Python: 
  - What's an API: instruction that tells how other applications can communicate with your application 
 
**Thoughts:** 
- Finsihed the coursework for AWS, now needs to start reviewing. Quite a productive day.


## Day 28: Aug 1, 2022 (Mon)

**Today's Progress**: 
- Watched some AWS exams tips.
- Did 1 section of practice exam on IAM. 
- Reviewed notes on AWS basic, IAM and S3. 
- Started Andrew Ng's machine learning course this morning, but a bit unsure whether or not I should study on that. 

**What I learned**:
- AWS
  - STS: single token sign-on: create temporary access tokens 
  - IAM user vs. IAM role vs. IAM group
    - IAM roles can be assumed, use for services and for cross-account or users that are not logged-in
    - IAM user: for long term access
    - IAM group: group of users, cannot be associated with resource policy
  - Different storage tiers in S3
 
**Thoughts:** 
- Not sure it was the best use of my time this morning to go through Andrew Ng's ML intro course. Might be better off finishing AWS exam or start on a course about RL. 

## Day 29: Aug 2, 2022 (Tue)

**Today's Progress**: 
- Started doing practice AWS practice exam questions. Covered S3, IAM, EC2.
- Started watching RL tutorials. 
- Continue on day 33 of 100 days of code; reviewed a bit on API. 

**What I learned**:
- AWS
  - EBS vs. EFS vs. S3
    - EFS is for file storage, more expensive, good for use case multiple EC2 needs to connect to the same DB. (regional service)
    - EBS is for block storage, low-latency; cheaper than EBS, but can only be mounted to 1 EC2. AZ service, data is automatically being replicated to multiple zones within the smae AZ.
    - EC2 is object storage, cheapest among the three. Has multiple storage tier, but cannot be mounted to EC2. Regional service, allow users to create snapshots and can be move across region. 
  - EBS
    - SSD vs. HDD
      - SSD is optimized for IOPS (i.e. like how fast the wheels are spinning)
      - HDD is optimized for thoughput (i.e like how big the wheels are)
      - SSD is good for small and random I/O and HDD is good for largle and consistent IOPs.
- Python
  - How to use the request package to call an API
- RL
  - RL is the intersection of decision making in psychology, machine learning, neuroscience and CS. 
  - The goal for RL is to figure out the best actions to take to maximum the long term expected rewards.
  - Key components in RL:
    - Agent (who makes the decision)
    - Env
    - State
    - Decision
    - Reward 
    - Stocastic component
  - how does RL differ from supervised learning?
    - RL has no labels to learn on
    - Data is dependent on previous data (not IID)
    - Rewards might be delayed.
  - Markov process
  - 3 different types of state
    - env state, which agents can't see
    - agent state => how agents see the world
    - markov state => all history combined and being represented in one single state
  - The job in RL is to be able to better represent the history so both agent and env can act on. 
 
**Thoughts:** 
- Reviewing AWS exam makes me feel like I'm not making as much progress :/ I want to wrap this up asap so I can study more on RL. 
- RL seems really interesting, like the science of decision making. 

## Day 30: Aug 3, 2022 (Wed)

**Today's Progress**: 
- Continue to review on AWS. 

**What I learned**:
- AWS
  - going through practice exam questions
 
**Thoughts:** 
- Again feel like not making as much progress and not sure if I should keep going with the exam given I will have much less chances of using this. But I think I will still keep going and aim to take the exam within the next few days. 

