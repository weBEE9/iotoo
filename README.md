# IOToo

This is a case study of a online course [The Complete Guide to Becoming a Software Architect](https://www.udemy.com/course/the-complete-guide-to-becoming-a-software-architect/), and I try to implment it as a developer.

## Functional Requirements
1. Receive status updates from IOT devices
2. Store the updates from future use
3. Query the updates

## Non-functional Requirements
### What we know
1. Messages are received from IOT devices
2. Probably a lot of messages
3. Affects the lode
4. Affects the data volume

### What we ask
- Data Volume
	- "What is the total number of messages per month?"
		- 15 million
	- "What is the average size of a message?"
		- 300 Bytes
	-  **54 GB annually**
- Message Loss
	- **1%**
- Users
	- "How many users will the system have?"
		- **2 million users**
	- "How many concurrent users should we expect?"
		- 40 concurrent users
- Load
	- "How many concurrent messages should the system expect in peak time?"
		- 500 concurrent messages
	- Total **540 concurrent requests**
		- 500 concurrent IOT devices message request
		- 40 concurrent users requests
- SLA
	- "What is the maximum downtime allowed?"
	- Three layer of SLA
		- Sliver
		- Gold
		- **Platinum**
			- Fully stateless
			- Easily scaled out
			- Logging & Monitoring
	- There is no point in discussing specific uptime numbers