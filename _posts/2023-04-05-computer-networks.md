---
toc: true
comments: true
layout: post
title: Computers and Networks (Unit 4)
description: Add Definitions from Unit 4 Computer Systems and Networks
---

## Requirements
> Work through College Board Unit 4... blog, add definitions, and pictures.  Be creative, for instance make a story of Computing and Networks that is related to your PBL experiences this year.


### How a Computer Works
> As we have learned, a computer needs aa program to do something smart.  The sequence of a program initiates a series of actions with the computers Central Processing Unit (CPU). This component is essentially a binary machine focussing on program instructions provided.  The CPU retrieves and stores the data it acts upon in Random Access Memory (RAM). Between the CPU, RAM, and Storage Devices a computer can work with many programs and large amounts of data.

List specification of your Computer, or Computers if working as Pair/Trio
- Processor GHz:
- Memory in GB:
- Storage in GB:
- OS:

Define or describe usage of Computer using Computer Programs. Pictures are preferred over a lot of text.  Use your experience.
- Input devices
- Output devices
- Program File
- Program Code
- Processes
- Ports
- Data File
- Inspect Running Code
- Inspect Variables


![Computer Hardware]({{site.baseurl}}/images/cpu.png)


### The Internet
> Watch/review College Board Daily Video for 4.1.1

- Essential Knowledge
    - A computing device is a physical artifact that can run a program. Some examples include computers, tablets, servers, routers, and smart sensors.
    - A computing system is a group of computing devices and programs working together for a common purpose.
    - A computer network is a group of interconnected computing devices capable of sending or receiving data.
    - A computer network is a type of computing system. 
    - A path between two computing devices on a computer network (a sender and a receiver) is a sequence of directly connected computing devices that begins at the sender and ends at the receiver.
    - Routing is the process of finding a path from sender to receiver.
    - The bandwidth of a computer network is the maximum amount of data that can be sent in a fixed amount of time.
    - Bandwidth is usually measured in bits per second


- Complete Vocabulary Matching Activity.  Incorporate this into your learnings from the year. To analyze measure path and latency use `traceroute` and `ping` commands from Linux Terminal.  
    - Path- a: is a sequence of directly connected computing devices that begins at the sender and ends at the receiver.
    - Route- e: is the process of finding a path from sender to receiver.
    - Computer System- b: a group of computing devices and programs working together for a common purpose.
    - Computer Device- c: a physical artifact that can run a program. some examples include computers, tablets, servers, routers, and smart sensors.
    - Bandwidth- d: the maximum amount of data that can be sent in a fixed amount of time.
    - Computer Network- f: a group of interconnected computing devices capable of sending or receiving data.

> Watch/review College Board Daily Video 4.1.2

- Complete True of False Questions
    - Open standards and protocols enable different manufacturers and developers to build hardware and software that can communicate with hardware and software on the rest of the internet: **True**
        - Open standards and protocols are technical specifications that are publicly available and not proprietary to any specific company or organization
    - IETF is a task force used to enforce laws to keep manufacturers out of the internet: **False**
        - IETF stands for "Internet Engineering Task Force." It is not a task force used to enforce laws, nor is it intended to keep manufacturers out of the internet. 
        - it is a community of engineers and technical experts who work together to develop and promote internet standards and protocols. 
    - Routes are determined in advance and are not flexible: **False**
        - Routing is the process of selecting the best path for data to travel through a network
        - it is based on factors such as network congestion, available bandwidth, and the number of hops between devices thus it varies
    - A protocol is an agreed upon set of rules that specify the behavior of a system: **True**
    - UDP guarantees transfers and is faster: **False**
        - UDP does not guarantee the delivery of data 
        - UDP ,however, is generally faster than TCP due to its lack of error-checking and retransmission mechanisms
    - The world wide web is the internet: **False**
        - The World Wide Web is an information system that operates over the Internet
        - it is one of many applications that run over the Internet
    - HTTP is a protocol used by the world wide web: **True**
        - used for transferring data between web servers and web clients


- Essential Knowledge
    - The internet is a computer network consisting of interconnected networks that use standardized, open (nonproprietary) communication protocols.
    - Access to the internet depends on the ability to connect a computing device to an internet connected device.
    - A protocol is an agreed-upon set of rules that specify the behavior of a system.
    - The protocols used in the internet are open, which allows users to easily connect additional computing devices to the internet.
    - Routing on the internet is usually dynamic; it is not specified in advance
    - The scalability of a system is the capacity for the system to change in size and scale to meet new demands.
    - The internet was designed to be scalable
    - Information is passed through the internet as a data stream. Data streams contain chunks of data, which are encapsulated in packets. 
    - Packets contain a chunk of data and metadata used for routing the packet between the origin and the destination on the internet, as well as for data reassembly.
    - Packets may arrive at the destination in order, out of order, or not at all
    - IP, TCP and UDP are common protocols used on the internet.
    - The world wide web is a system of linked pages, programs, and files.
    - HTTP is a protocol used by the world wide web
    - The world wide web uses the internet

- Go over AP videos, vocabulary, and essential knowledge. Draw a diagram showing the internet and its many levels. A preferred diagram would using your knowledge of frontend, backend, deployment, etc.  Picture would highlight vocabulary by illustration. The below illustration have some ideas

![Internet]({{site.baseurl}}/images/internetdiagram.png)

![Full Stack]({{site.baseurl}}/images/fullstack.png)

- Often we draw pictures of machines communicating over the Internet with arrows.  However, the real communication goes through protocol layers and the machine and then is transported of the network. For College Board and future Computer Knowledge you should become familiar with the following ...

```
     User Machine  <---> Frontend Server <---> Backend Server
    +-----------+         +-----------+         +-----------+
    |  Browser  |         |  GH Page  |         |   Flask   |
    +-----------+    ^    +-----------+    ^    +-----------+
    |    HTTP   |    |    |    HTTP   |    |    |    HTTP   |
    +-----------+    |    +-----------+    |    +-----------+
    |    TCP    |    |    |    TCP    |    |    |    TCP    |   
    +-----------+    |    +-----------+    |    +-----------+
    |     IP    |    V    |     IP    |    V    |     IP    |
    +-----------+         +-----------+         +-----------+
    |  Network  |  <--->  |  Network  |  <--->  |  Network  |
    +-----------+         +-----------+         +-----------+
```

The "http" layer is an application layer protocol in the TCP/IP stack, used for ***communication between web browsers and web servers***. It is the protocol used for transmitting data over the World Wide Web.

The "transport" layer (TCP) is responsible for providing reliable data transfer between applications running on different hosts.  The TCP protocol segments the data into smaller ***chunks called "segments"***. Each segment contains a sequence number that identifies its position in the original stream of data, as well as other control information such as source and destination port numbers, and checksums for error detection.

The "ip" layer is responsible for packetizing data received from the TCP layer of the protocol stack, and then ***encapsulating the data into IP packets***. The IP packets are then sent to the lower layers of the protocol stack for transmission over the network.

The "network" layer is responsible for ***routing data packets between networks*** using the Internet Protocol (IP). This layer handles tasks such as packet addressing and routing, fragmentation and reassembly, and ***network congestion*** control.


### Fault Tolerance
- in class activity
![Computer Networks]({{site.baseurl}}/images/networks.png)

> Watch both Daily videos for 4.2
- Complete the network activity, summarize your understanding of fault tolerance.
    - fewer direct connections means that you dont have to expend as many resources, however if one connection breaks, the whole system might be unconnected
    - if every device has a direct connection to one another, this means there is redundancy. redundancy is good in ensuring that if one connection goes down, there are more to support it. 
    - However, having a lot of direct connections uses up more resources
    - redundancy is the inclusion of extra components that can be used to mitigate failure of a system if other components fail

![network1]({{site.baseurl}}/images/network1.png)
- for each of the devices, there are at least two other paths to the other devices so this network is **fault tolerant**

![network2]({{site.baseurl}}/images/network2.png)
- most of the devices have two paths which it can use to communicate to other devices. 
- however, device F has only once connection, so if that connection is cut off, it can no longer communicate with other devices thus this network is **faulty**

![network3]({{site.baseurl}}/images/network3.png)
- every single connection is made through the path A-G so if the connection between A and G were to be broken, the entire network would be down. Thus this network is **faulty**

### Parallel and Distributed Computing
> Review previous lecture on Parallel Computing and watch Daily video 4.3. Think of ways to make something in you team project to utilize Cores more effectively.  Here are some thoughts to add to your story of Computers and Networks...

- What is naturally Distributed in Frontend/Backend architecture? 
    - workload: The frontend and backend components typically run on separate machines or servers, allowing them to handle different tasks independently. This distribution of workload can help improve performance and scalability, as each component can be optimized for its specific tasks and resources can be allocated more efficiently.
    - data storage: The backend component typically handles data storage and retrieval, allowing the frontend component to focus on presentation and user interaction.
    - communication: The two components communicate via APIs or other protocols, allowing them to exchange data and coordinate their actions. 

- Analyze this command in Docker: ```ENV GUNICORN_CMD_ARGS="--workers=1 --bind=0.0.0.0:8086"```.   Determine if there are options in this command for parallel computing within the server that runs python/gunicorn. Here is an [article](https://medium.com/building-the-system/gunicorn-3-means-of-concurrency-efbb547674b7)
    - The command sets an environment variable `GUNICORN_CMD_ARGS` with the value `--workers=1 --bind=0.0.0.0:8086` in a Dockerfile.
    - The option `--workers=1` in `GUNICORN_CMD_ARGS` specifies the number of worker processes that Gunicorn should spawn. In this case, it is set to 1, meaning that Gunicorn will only use a single worker process to handle incoming requests.
    - Therefore, this command does not enable parallel computing within the server that runs Python/Gunicorn. Instead, it restricts Gunicorn to using only one worker process, which may limit its ability to handle multiple requests concurrently. However, setting the number of workers to 1 may be appropriate for some applications with low traffic volume or for development purposes.


> Last week we discussed parallel computing on local machine.  There are many options. Here is something to get parallel computing work with a tool called Ray.

- Review this [article](https://www.anyscale.com/blog/writing-your-first-distributed-python-application-with-ray)...  Can you get parallel code on images to work more effectively?  I have not tried Ray.
    - For image processing tasks, the appropriate parallelization strategy might involve using a data parallel approach, where the same computation is applied to different parts of the image simultaneously. 

- Code example from ChatGPT using squares.  This might be more interesting if nums we generated to be a lot bigger.

```python
import ray

# define a simple function that takes a number and returns its square
def square(x):
    return x * x

# initialize Ray
ray.init()

# create a remote function that squares a list of numbers in parallel
@ray.remote
def square_list(nums):
    return [square(num) for num in nums]

# define a list of numbers to square
nums = [1, 2, 3, 4, 5]

# split the list into two parts
split_idx = len(nums) // 2
part1, part2 = nums[:split_idx], nums[split_idx:]

# call the remote function in parallel on the two parts
part1_result = square_list.remote(part1)
part2_result = square_list.remote(part2)

# get the results and combine them
result = ray.get(part1_result) + ray.get(part2_result)

# print the result
print(result)

```