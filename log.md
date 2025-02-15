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

## Day 31: Aug 4, 2022 (Thurs)

**Today's Progress**: 
- AWS
  - Completed 1 AWS timed practice exam, scored 76% (barely passed).
  - The second exam attempt that I completed 30% only got 8 out of 25. 
- RL
  - Started reading "Introduction to RL"; seems like a pretty hard read. I was falling asleep after reading 1-2 pages. I might need to find another way to learn RL. 
- Rapid learner
  - It is important to plan projects ahead and continue to update the plan. 
  - Key takeaway:
    - Reframe frustraction as part of learning (i.e. brain is working hard)
    - Have a plan and keep it updated
    - Learn the minimum and start implementing

**What I learned**:
- AWS
  - going through practice exam questions
 
**Thoughts:** 
- Scheudled the exam for Sunday! 
- Reinforcement learning seems really interesting; I need to find a way to get mastery at it. 

## Day 32/33: Aug 5-6, 2022 (Fri & Sat)

**Today's Progress**: 
- AWS
  - Studied AWS exam and did practice test

**What I learned**:
- AWS
  - going through practice exam questions
  - CloudWatch vs. CloudTrail vs. S3 server log:
    - CloudWatch for metrics like CPU utitlization, Network in/out
    - CloudTrail for monitoring activities like API calls, actions taken by users
    - S3 Server log: detailed record of request made to S3
  - AWS storage gateway vs. DataSync => both for moving on-perm data to AWS
    - Storage gateway for integration (keeping on-perm DC)
    - DataSync for migration
  - AWS Control Tower: a central place for managing multiple account
  - Secruity products
    - Shield: for DDoS attack (free and advanced version)
    - WAF: for SQL injection and other layer 7 attack
    - Maice: for detecting PII data in S3
    - GuardDuty: for detecting unexpected account activity
  - ECS Fargate vs. ECS EC2 => both for container management
    - Fargate: AWS managed infra
    - ECS EC2: users controlling what kind of EC2 to use (type, size and network)
  - What are the ways to connect on-perm with AWS?
    - Direct connect: take weeks or months, physical connection, not encrypted by default, not HA by default
    - Site-to-site VPN: easy to set up, secure via IPSec, not HA by default (need to add Customer gateway)
  - Transit gateway: a way to connect all VPC, VPN and direct connect together to simplify the network 
  - Storage gateway: to connect on-perm storage with AWS storage products
    - Volumne gateway
      - Cached mode: primary data stores in AWS
      - Stored mode: primiary data stores in on-perm DC
    - Tape gateway
    - file gateway
  - ELB vs. R53:
    - ELB: route within region
    - R53: route across region
  - VPC endpoints:
    - connect EC2 within VPC to services outside VPC
      - Gateway endpoint: connect EC2 with S3 and DynamoDB
      - Interface endpoint: everything else
  - Identity pool vs. user pool
    - identity pool for authentication => logging users in via SSO
    - user pool for authorization => allowing users to use what resources
**Thoughts:** 
- Seems to have a better understanding of AWS, but still lots of things to learn. 

## Day 34: Aug 7, 2022 (Sun)

**Today's Progress**: 
- AWS: Completed AWS SAA exam. 
- RL: Watched David Silver's RL class lecture 1. 
- Deep Learning: Watched FastAI lecture 1. 

**What I learned**:
- RL:
  - The goal for RL is to maximize the long term reward that the agent gets via trial and error (long term planning, require strategy)
  - Key component: 
    - agent: takes action in the env, get rewards, determine next steps and repeat
    - env
    - action
    - reward
  - State: a way to capture history that helps the agent to decide what actions to take. 3 main types of states:
    - Agent state: what the agent view of the world is
    - Env state
    - Markov state: a state that fully captures the histroy. That is, by having markov state, the decision that the agent makes would be the same as if they have all the history. (e.g. env state and keep all history are both Markov).
  - What's inside an agent (some are optional)? 
    - Policy (behavior): mapping state to action
    - Value function: predicting what's the reward for future actions 
    - Agent's view of env state
  - Three main types of agent:
    - policy based (store policy)
    - value based (store value)
    - Active critic (store both policy and value) 
  - Two main types of env:
    - fully observerd env (MDP - Markov decision process)
    - partially observed env (POMDP)
  - Two main types of RL:
    - Model based: a model first built to understand the env (e.g. when modeling helicopter, first build an env with wind condition, airflow etc.)
    - Model free: use value and/or policy
  - RL problem = sequential decision making
    - explore vs. exploit
    - learning vs. control?
- Deep Learning:
  - FastAI is a libaray that built on top of Pytouch
  - Can train an model within seconds.
  - steps of building a model:
    - DataLoader(): getting data in the right form to ingest in model
    - Learner(): Train model
    - Fine_tune(): adjust model using tranform learning to improve error (given model was trained based on a different dataset).

**Thoughts:** 
- Wasn't sure if I was going to pass the AWS exam so a bit nervous. RL and DL are really fun! The more I read about it, the more I want to know about it! 

## Day 35: Aug 8, 2022 (Mon)

**Today's Progress**: 
- AWS: Did a few practice question on AWS developer associate exam.
- Deep Learning: Half way through reading FastAI chapter 1.

**What I learned**:
- AWS
  - stage variable: 
    - set in stage configuration during the deployment stage of REST API
    - similar to env variable but can be passed onto mapping templates, lambda or other HTTP backends.
    - key value pair
  - Lambda: 
    - has execution context that can act as "cache" to store some bootstrap info (e.g. download package from 3rd party)
    - use for minimiziing the setup time when lambda is triggered the second time.
- RL paper:
  - Multi-agent RL can be used in supply chain, but this is only usable when the model has fully e2e data visiablity. 
- RL podcast:
  - Multi-agent RL can be modeled with social influence. That is, agents don't see each others value function but instead, only observe their behavior, which is more realistic. 
  - Multi-agent problem faces Prisoner's dilemma as agents are all in partial observable env. 

**Thoughts:** 
- Met with Cathy and went to gym. Didn't do as much as I would love to but better than not doing anything. RL podcast seems very interesting!

## Day 35: Aug 9, 2022 (Tue)

**Today's Progress**: 
- RL: read search paper on Adaptive learning, multi-agent DRL on supply chain. Watched about 20 mins of David Silver's lecture 2. 
- AWS: did a few AWS exam questions. 

**What I learned**:
- AWS
  - Lambda integration proxy: a easy and powerful way to intergate API gateway and use Lambda as backend. 
    - The API call is passed directly to Lambda, but the order is not preserved. 
    - The response format MUST BE in JSON. 
    - 502 error if format is not in JSON. 
    - 504 error if request timed out. 
    - To monitor backend and overall responsiveness, monitor IntegrationLatency and Latency. 
  - SQS long polling vs. short polling:
    - Long polling: more cost efficient, only poll messages when it arrives. 
    - Short polling: poll messages as soon as they arrive to SQS. 
  - Cloudfront:
    - Self signed certificate is not needed between Cloudfront and origin. 
    - ELB / ALB doesn't have default SSL. 
    - To use HTTPs in cloudfront, change VIEWER POLICY to `USE HTTPS` and `REDIRECT HITTP TO HTTPS`.
  - DynamoDB:
    - Has TTL settings at item level?
    - Atomic counter: use when Idempodent is NOT needed. 
    - Condition Writes is used when multiple users are editing the same item. 
  - AWS X-Ray:
    - Has active tracing for Lambda, use for debugging applications
  - AWS inspector: 
    - use to detect vulnerability or unintended network accessibility
- RL paper:
  - The paper uses PPO (proximity policy optimization) which doesn't require extensive hyperparameter tuning and defined action space. 
  - The model outperfroms base-stock model when env is challenging. 
  - The agent showed exploited behavior at the end by not restocking as they know they cannot sell it before the time ends. This needs to be addressed if the model is used in real world. 
  - The paper uses active-critic approach, where it has two models. One for determining actions and one for rewards.
- David silver's lecture 2: 
  - Markov process:
    - Markov process (MDP): a memoryless set of random actions + transition matrix
      - Markov properties: given the current state, it captures all the information from the previous states and the action will take the same action as if they have all the history. 
      - All RL models can be treated as MDP, even in partial observable env. 
      - Prob(reward at new state) = function(current state, transition matrix)
        - Transition matrix represents the prob(state X -> state Y)
        - Episode: samples of the markov process (from start to terminate state)
    - Markov reward process: Markov process + reward + decay function
      - Decay function is used to keep the reward finite, future is uncertain (model is not perfect) and mimic humna thinking (i.e. present value)
      - Decay fucntion is between (0, 1); where 0 is being short-sighted and 1 is being extremely far-sighted. 


**Thoughts:** 
- Pretty productive day. Very exitied to learn more about RL. 


## Day 36: Aug 10, 2022 (Wed)

**Today's Progress**: 
- RL: started reading search paper on DRL application on supply chain. Only finisihed introduction though. Continue watching David Silver's lecture 2. 
- AWS: did a few AWS exam questions. 

**What I learned**:
- AWS
  - ElasticBeanstalk is used to orchastraic different AWS services (i.e to setup, config and provision resources). 
  - ElasticBeanstalk worker env can be used for decoupling long running applications. 
    - It creates a SQS and put long response message there. It installs a daemon set on each of the EC2. Once the message is polled from the queue, the daemonsets sends a response to the client with the message. 
- RL paper:
  - Multi-agent, independent learner RL performs better than base-stock policy in challenging env. 
  - Beer distribution game = classic supply-chain case study where there are 4 parties (manufactuor, distributor, warehouse, retailers). Each have to set their quantity to order. 
  - Base-stock policy = "on-hand inventory + on-orders delivery" equals to demand??
  - Base-stock policy is the optimal policy when all players act rationally (follow the same base-stock policy) and the market condition is not uncertain. However, if some players are not rational, there is no known optimal policy.
- David silver's lecture 2: 
  - Markov reward process: markov process + decay factor + reward
    - Becaman equation: your expected return = immediate return + discounted return from future steps.
  - Markov decision process: markov process + decay factor + reward + actions
    - actions can be finitie/ infinite, discrete/ continuous
    - Becaman equation:
      - Value function:
        - State value function: how good is it to be in state X given the agent continue to follow certain policy 
        - Action value function: how good is it to take action A given state X given and the agent continue to follow certain policy 
    - Policy: determines agent's behavior
    - Optimal value policy: 
      - optimal state-value function: what's the maximum return that can be extracted from the system.
      - optimal action-value function: what's the best action to take given State X to maximize the return (goal for MDP is to solve for this)


**Thoughts:** 
- Didn't have good sleep the night before, only 2-3 hours; so the mind is noticeably more easy to get distrated. I caught myself couple times browsing on random website when I was watching RL videos. Given the amount of sleep, not too bad day. 

## Day 37: Aug 11, 2022 (Thurs)

**Today's Progress**: 
- RL: finished David Silver's lecture 2, I think it took me 3 hours in total. Started reading the RL intro book, halfway through chapter 1. 
- Python: attempted to code a bit but probably only got 10 mins

**What I learned**:
- David silver's lecture 2: 
  - Optimal Reward function:
    - Optimal State-value function: what's the most value I can extract from being in this state
      - 2 steps look ahead:
        - Step 1: Based on the actions that I can take, what states will I end up in.
        - Step 2: Based on the state I ended up in step 1, what the env will bring me to in the next step? what the value function for that step?
        - Back probagate the rewards and take max
    - Optimal Actin-value function: what action gives me the most value from this point onward
        - Two steps look ahead but take average
- Optimal policy: the best way to behave. i.e. for value function at each state following the optimal policy is >= any other policy 
  - For every MDP:
    - There must be one or more optimal policy.
    - In the same MDP, all optimal policy share the same optimal value function and optimal action-value function. 

- Bellman Optimality equation (a way to solve MDP):
    - Q* => Optimal action
    - v* => Optimate state function
  - Bellman equation is not linear, and has not closed solution. Thus needs to be solved using dynamic programming or q-learning.

**Thoughts:** 
- Didn't have good sleep the night before, only 2-3 hours; so the mind is noticeably more easy to get distrated. I caught myself couple times browsing on random website when I was watching RL videos. Given the amount of sleep, not too bad day. 


## Day 38: Aug 12, 2022 (Fri)

**Today's Progress**: 
- RL: rewatched David Silver lecture 2, started watching lecture 1.
- AWS: did about 8-10 questions

**What I learned**:
- David silver's lecture 2: MDP
  - Markov Process: memoryless sets of steps => The future is independent of the past given present
    - The goal for RL is to maximize the long term return. 
    - Return = sum of rewards 
    - All RL problems can be formalized as MDP. 
  - Markov reward process (MRP): Markov process + reward + discount factor
    - value function => How good is it to be in this state? 
    - Bellmon equation => breaks down value function into: the value fo being in state S = immediate reward of being in State S + rewards from State S onwards. 
  - Markov decision process (MDP) = Markov Reward Process + Actions
    - Policy = guide the agent what actions to take => prob of actions over all states
    - Bellmon expectation equation:
      - value state function = sum of (prob of action * value function from that action) following the same polcy
      - action state function = immediate reward + discount factor * sum of (transition matrix * value function from next state) following the same polcy
  - Optimal value function => what's the best policy to take in this MDP? 
    - Bellmon optimality equation: 
      - value state function = what's the max value function given all actions that can be taken? 
      - action state function = immediate reward + discount factor * sum of (transition matrix * value function from next state based on the optimal polcy)
  - David silver's lecture 3: Dynamic programming
    - Dynamic programming = a way to breakdown large problems and solve them sequentially and recursively. Two properties:
      - problems can be broken down into smaller pieces. => Bellmon equation
      - solutions can be "cached" and use later => value function
    - MDP can be solved using dynamic programming.

- AWS 
  - environmental variables: similar to stage variables but can be used by Lambda (stage variable is only for API gateway)
    - can be used to pass variables to functional code 
  - AWS Serverless Application Manager (AWS SAM): similar to cloudformation that uses templates to help dev build and manager stacks. But AWS SAM also allows devs to build, test and debug in local env.
  - Kinessis data stream: uses KCL (Kinesis client library) worker to monitor and prcocess data from each shard. 
    - 1 shard can only be processed by 1 worker
    - 1 worker can process more than 1 shard.
  - ElasticBeanstalk deployment mode: all at once, rolling, rolling with new, green/blue world, immutable.


**Thoughts:** 
- Rewatching the RL video defintiely helped a lot to help me put the piece back together. I was confused between 1 step look ahead and 2 steps look ahead and a few other major concepts.



## Day 39: Aug 13, 2022 (Sat)

**Today's Progress**: 
- RL: continue watching DS lecture 3.
- AWS: did about 8-10 questions

**What I learned**:
- David silver's lecture 3: Dynamic Programming
  - Dynamic programming = a sequential way of solving a probelm. 
    - The problem can be subdivided into smaller problems.
    - The solution can be "cached" 
  - MDP can be solved using dynamic programming
    - Bellmon equation => breakdown into smaller probles recursivly
    - Solution can be "cached" => value function
  - How to solve MDP?
    - Policy iteration
      - first evaluate the policy using Bellman expectation equation (i.e. taking average)
      - then apply greedy algorithm
    - Value iteration
      - apply bellmon optimality equation (i.e taking max) 

**Thoughts:** 
- Took it a bit easy yesterday. Had lunch with Keith, went to gym and spent the night with DJ. Will get back to it today!



## Day 40: Aug 14, 2022 (Sun)

**Today's Progress**: 
- RL: finished DS lecture 3; read the slides for lecture 4 and watched for ~10 mins.
- Deep learning: Almost finishing reading chaper 1 of fastAI. 
- AWS: did about 8-10 questions

**What I learned**:
- David silver's lecture 3: Dynamic Programming
  - Dynamic programming can be used to solve KNOWN MDP, where env (transition matrix, rewards) is given. 
  - There are two main types of probelms.
    - Predict: given a policy, how good is it? (how much reward can we get by following this policy?)
      - Use policy evaluation: i.e. to apply Bellmon expectation equation to all states and update v(s)
        - v(s) = r + sum[prob(s')*v(s')]
      - This guarantee converges; the updates can be done sync or async. 
    - Control: what's the optimal policy for this MDP? (how to act optimally to get the max rewards?)
      - either use policy iteration or value iteration. 
        - policy iteration: do policy evaluation, then act greedily at every step
        - value iteration: apply Bellmon optimality equation 
          - we are not explicitiy building policy. i.e. any intermediate steps might not lead to any policy.
    - Time complexity is O(mn^2) where m is number of acions and n is number of states
      - n^2 because we have to consider update every state in each iteration and for each state, there is n other possible states to the agent can transition to.
  - Async update: to save compuational cost
    - in-place DP: don't keep previous copy of v(s)
    - Prioritise sweeping: largest delta: only update parts where v(s) changes the most
    - real time DP: have a robot wander around the env and only update the parts it passes

- David silver's lecture 4: Model free prediction
  - DP can only be used when the env is known. For env that's unknown, we need to use either Monte Carlo learning or Temporal Difference.
  - Monte Carlo learns from episode.
    - as long as all states are covered, the order of which states the agent visited doesn't matter.
    - Uses emperical mean => v(s) = average v(s) from all iterations.

- FastAI: 
  - 4 main steps in using FastAI for deep learning:
    - dataLoader() => get the data into the right format
    - learner() => tell the model what pre-trained model to use
    - fit() or fine_tune() => the model will drop the last layer of NN to fit it specically to this new dataset. 
    - predict() 
  - epoach => 1 full iteration of the data
  - Image classification can be applied to many other areas outside classifying photos. Many real world problems can be represented as picture. e.g. fraud detection. 
  - Transfer learning = Taking a pre-trained model and applying it to another use case that it wasn't initially trained on 
  - Stochastic gradient descent (SGD): use to update the weights in Neural network
  - Difference between loss and metrics?
    - loss => use for SGD to update weights
    - metrics => use for human to evaluation model performance


- AWS:
  - In AWS SAM (Serverless application manager), an application can have one or more nested application. This is specified in the configuration as AWS::SERVERLESS::APPLICATION.
    - AWS::SERVERLESS::API: for API gateway
    - AWS::SERVERLESS::Layer for passing into to lambda
    - AWS::SERVERLESS::Function = for lambda function
  - To connect custom API endpoint with API gateway: can use either proxy intergration or custom intergration
    - HTTP: for HTTP custom integration where we need to map incoming request with integration response. 
    - HTTP Proxy: for HTTP proxy intergration, where there is no need to map incoming request with integration response.
    - AWS: for AWS custom integration
    - AWS Proxy: for AWS proxy intergration


**Thoughts:** 
- Studied for about 4 hours; probably the max amount I can study over the weekend if I want to spend sometime with DJ. 



## Day 40: Aug 14, 2022 (Sun)

**Today's Progress**: 
- RL: finished DS lecture 4
- Deep learning: finished reading FastAi chapter 1

**What I learned**:
- David silver's lecture 4: Model free prediction
  - Model free prediction, where env (transition matrix and rewards) is unknown, can be done using Monte-Carlo learning or Temporal learning.
  - Monte Carlo: 
    - learn from the whole episode,  only works when episode terminates
    - zero bias but large variance
    - basic idea: run many episodes and record the total rewards, then take average. Update the current estimated total reward by a little based on the new sample reward.
      - first visit MC: only count the reward when the agent first passes the state
      - every visit MC: count the reward fro every visit that the agent made pass the state.
      - when to use first visit vs. every visit depends on the domain
    - incremental mean: incrementally increase the estimated mean by a little based on the sample reward. 
    - Still converge using function approximation.
  - Temporal learning:
    - learn from bootstrapping => i.e. updating guessed value function using a new guessed function => works also for non-terminating episodes.
    - more efficient than MC
    - larger bias but small variance. 
    - TD(0): update guessed value function based on 1 step look ahead.
      - substituting estimated mean based on bellmon equation: reward + discounted expected reward at t+1. 
    - might not converge when using function approximation.
  - TD(lambda)
    - instead of doing 1 step look ahead in TD(0), TD works at n-step look ahead. 
    - When n = terminate state, then TD(n) = MC
    - Two ways of doing TD(lamdba)
      - forward looking => suffers the same draw back as MC where rewards only get updated at the end of episode. 
      - backward looking => using eligiblity curve to update the states that contributes the most error (i.e. sample mean - prev est. mean)

**Thoughts:** 
- I printed out all the slides and took notes there via watching the video. I think this works better as I can later transfer the notes to REM notes. 


## Day 41: Aug 15, 2022 (Mon)

**Today's Progress**: 
- None, spent majority of the day reviewing Fractal's doc. 

**What I learned**:
- Overview of Fractal, how they are thinking about the problem.

**Thoughts:** 
- Need to get back to this today. Can't go on two days without self-study.

## Day 42: Aug 16, 2022 (Tue)

**Today's Progress**: 
- None, spent majority of the day reviewing Fractal's doc. 

**What I learned**:
- Tech roadmap and RL design doc. 

**Thoughts:** 
- Will get back to RL studying today. 

## Day 43: Aug 18, 2022 (Thurs)

**Today's Progress**: 
- Rewatched the 2nd half of David Silver lecture 4 on forward looking TD and backward looking TD. 

**What I learned**:
- 2 main dimensions in predicting MDP => i.e. calculating the value function of an MDP  
  - Sampling
    - MC and TD sample
    - DP doesn't sample
  - Bootstrap (i.e. use patial path instead of going to the end of the episode)
    - MC and DP don't bootstrap
    - TD bootstrap
- TD lambda
  - Besdies TD(0), which is one-step look ahead, we can also sue TD(lamdba).
  - Foward looking
    - TD(lambda) takes geometry means of all lambda. i.e. for every lambda, use (1-lambda)*(lambda^n) as weight.
    - However, this approach suffers the same downside as MC as we have to wait till the end of the episode to update the value function. 
    - Thus, we can use "backward looking TD(lambda).
  - Backward looking
    - In backward looking TD, we use eligibility trace to see what states had contribute to the most error and update those. 
    - i.e. first do 1 step look ahead like TD(0), then udpate state based on TD error and eligibility trace.

**Thoughts:** 
- My ADD was very severe yeseterday and wasn't able to study much nor even focus. I guess my body just really wanted to sleep. The sleep last night (Friday) was amazing, and I feel a lot better today. Will put back in more time to study. 


## Day 44: Aug 19, 2022 (Fri)

**Today's Progress**: 
- Finally got back to studying. Watched ~20mins of David Silver's lecture 5. 

**What I learned**:
- Model free control:
  - 2 main types:
    - on-policy: "learn on the job", the actions that you take influence the policy you learn
    - off-policy: "watch over someone else's shoulder", like a robot watching other robot to do the job then learn about the policy.
  - on-policy
    - using Monte Carlo + act greedy
      - won't work due to 1) given this is model free, we don't know the transiton matrix to act greedy; 2) won't be able to explore enough. 
      - To solve problem #1: instead of using state-value function (V), use action value function (Q)
        - i.e. at every state, compute q(s,a)
      - To solve problem #2: use ∈ greedy algorithm.
        - i.e for ∈ probabilty, take random action. For 1-∈ prob, act greedy. 

**Thoughts:** 
- Feels good to be able to study again. Need to find back to rhythm and get more study time. 


## Day 45: Aug 20, 2022 (Sat)

**Today's Progress**: 
- Finally finished David Silver lecture 5, studied for ~4.5 30 mins promodoro yesterday.
- Let's try to do at least 5 total everyday with 1 for studying.

**What I learned**:
- Model free control:
  - On-policy learning:
    - MC:
      - Can't directly use Monti-Carlo on state-value function + Greedy to do model free control because we don't know the transition matrix and we might not have explored enough. 
      - To solve the not knowing model dynamics, we use MC on action value function + "∈ greedy policy". 
    - SARSA(lambda)
      - Another approach is to use TD instead of MC. 
      - SARSA(lambda) uses eligibility trace to propagate the "learnings" backward. The larger lambda is, the further it propagates (i.e. higher variance but less bias). 
      - We keep track of the eligibilty trace for all (s,a). 
        - everytime we pass by a certain (s,a); we increment the counter at that (s,a) by 1. 
        - at every step, we decay all (s,a) by a little. 
        - SARSA can be done with forward view or backward view. 
          - Backward view Q(s,a) = Q(s,a)+ (alpha* TD error* E(s,a))
            - alpha = fixed constant => learning rate
            - TD-error = R(t+1) + "discount factor"Q(s,a)(t+1) - Q(S,A)
    - Off-plolicy learning
      - Why do we want to do that? 
        - can learn from old policy
        - batch update
        - can learn from alternative path while following one path
        - can learn from some other robots/humna
      - How to do it? 
        - Importance sampling
        - Q-learning

**Thoughts:** 
- Didn't studied or worked as much as I would like to; but still alright. Better than not doing it at all. met with Kat and Jon yesterday for dim sum; it was really nice. 


## Day 46: Aug 21, 2022 (Sun)

**Today's Progress**: 
- Didn't do much studying today. Spent most of the time with DJ and the rest of time watching FR videos. 

**What I learned**:
- n/a

**Thoughts:** 
- It is tough to balanace between work, study and family. I need to find a good way to do this and not burn myself out. 



## Day 47: Aug 22, 2022 (Mon)

**Today's Progress**: 
- Rewatched a bit of David Silver's lecture 5 on Model free learning. 

**What I learned**:
- Model free learning can be done on-policy or off-policy. 
  - On-policy:
    - Monte Carlo on Q-value + ∈ greedy policy.
      - need to use Q value because this is model free and we don't know the transition matrix.
      - need to use ∈ greedy instead of greedy because we don't want to get stuck in local maximum.
      - To do MC efficiently, we can do policy optimization after every episode instead of wait till the q-value for that q(s,a) converges
      - Greedy in the Limiit with Infinite Exploration(GLIE): 
        - all states, actions must be explored infinite number of times, 
        - The policy converges on a greedy policy
      - GLIE Monte Carlo control
        - GLIE MC => uses 1/k
        - Every time a state-action is visited, increment the counter by 1. 
        - Update the q(s,a) by `estiamated q(s,a) - current-q(s,q)/counter`

**Thoughts:** 
- Feel like I'm getting lazy, and not spending enough time at work and study. Need to get back to it!!!



## Day 48: Aug 23, 2022 (Tue)

**Today's Progress**: 
- Didn't ended up studying at all as I was in the office yesterday. My plan is to at least attempt one coding question every day just to keep it fresh. 

**What I learned**:
- n/a

**Thoughts:** 
- Need to get back to it today. 



## Day 49: Aug 24, 2022 (Wed)

**Today's Progress**: 
- Did one python question on codewar.

**What I learned**:
- n/a

**Thoughts:** 
- Will put in more time on Fri or over the weekend. 


