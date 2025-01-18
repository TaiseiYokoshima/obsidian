
# Imbalance
Imbalance exists between the complexity of modern database management systems and the security technique used to protect these critical systems 

Reasons:
- The increasing reliance on cloud technology to host database (some or all)
- Most enterprise environments consist of a heterogeneous mixture of database platforms, enterprise platforms, and OS platforms, which adds complexity.
- The typical organization lacks full-time database security personnel 
- Effective database security requires a strategy based on a full understanding of the security vulnerabilities of SQL
#  SQL Injection (SQLi)
- One of the most prevalent and dangerous network-based security threats
- Designed to exploit the nature of Web application pages 
- Most common attack goal is bulk extraction of data
- Depending on the environment, SQL injection can also be exploited to:
	- modify or delete data
	- execute arbitrary operating system commands
	- launch DoS attacks

## Injection Technique 
The SQLi attack typically works by prematurely terminating a text string and appending a new command 

Because the inserted command may have additional strings appended to it before it is executed, the attacker terminates the injected string with a comment mark "--"

Subsequent text is ignored at execution time


## Injection Avenues
- User input
	- attackers inject sql commands by providing suitable crafted user input
- server variables 
	- attackers can forge the values that are placed in http and network headers and exploit this vulnerability by placing data directly into the headers 
- Second-order injection 
	-  A malicious user could rely on data already present in the system or database to trigger an sql injection present in the system or database to trigger an SQL injection attack, so when the attack occurs, the input that modifies the query to cause an attack does not come from the user, but from within the system itself
- Cookies
	- attacker could alter cookies such that when the application server builds an sql query based on the cookie's content, the structure and function of the query is modified
- Physical user input
	- Applying user input that constructs an attack outside the realm of web requests 


## Inband Attacks
- Uses the same communication channel for injecting sql code and retrieving results
- The retrieved data are presented directly in application web page include:
	- Tautology 
		- this form of attack injects code in one or more conditional statements so that they always evaluate to true (e.g. 1=1 )
	- End-of-line comment
		- after injecting code into a particular field, legitimate code that follows are nullified through usage of end of line comments
	- Piggybacked queries
		- the attacker adds additional queries beyond the intended query, piggy-backing the attack on top of a legitimate request 

### SQL for Inband Attacks
1. Tautology using a PHP example:
```
$query =" 
SELECT info FROM user WHERE name = '$_GET["name"]' AND pwd = '$_GET["pwd"]' 
"
```
User submits " ' OR 1=1 --" for the name field 
Query becomes:
```
$query =" 
SELECT info FROM user WHERE name = ' ' OR 1=1 -- ...
"
```
The password check is ignored because of the --- 

2. Attacks use the comment field to disable other parts of the SQL 
3. Piggybacked queries use the semi-colon to execute additional statements 

## Inferential Attack
- There is no actual transfer of data, but the attacker is able to reconstruct the information by sending particular requests and observing the resulting behavior of the website / database server
- Include:
	- Illegal/logically incorrect queries 
		- this attack lets an attacker gather important information about the type and structure of the backend database of a web application
		- the attack is considered a preliminary, information-gathering step for other attacks
	- Blind sql injection
		- allows attackers to infer the data present in a database system even when the system is sufficiently secure to not display any erroneous information back to the attacker, by injecting statements which are true or false - false terminates the sql and reveals internal structure

## Inference Detection
1. during database design 
	- Approach removes an inference channel by altering the database structure or by changing the access control regime to prevent inference
	- Techniques in this category often result in unnecessarily stricter access controls that reduce availability
2. at query time
	- Approach seeks to eliminate an inference channel violation during a query or series of queries 
	- If an inference channel is detected, the query is denied or altered

### Out-of-Band Attack
- Data are retrieved using a different channel
- This can be used when there are limitations on information retrieval, but outband  connectivity from the database server is lax, e.g., when the results are returned in an email

# SQLi Countermeasures
Defensive coding:
- manual defensive coding practices
- parameterized query insertion
- sql dom 
Detection:
- signature-based
- anomaly-based
- code analysis
Runtime prevention:
- check queries at runtime to see if they conform to a model of expected queries



# Database Access Control
Database access control system determines:
1. if the user has access to the entire database or just portions of it 
2. what access rights the user has (create, insert, delete, update, read, write)

Can support a range of administrative policies:
- Centralized administration: small number of privileged users may grant and revoke access rights
- Ownership-based administration: the creator of a table may grant and revoke access rights to the table
- Decentralized administration: the owner of the table may grant and revoke authorization rights to other users, allowing them to grant and revoke access rights to the table

### SQL-based Access Controls
- Nearly all DBMS have an inbuilt DAC Mechanism 
- Two commands for managing access rights:
	- Grant
		- Used to grant one or more access rights or can be used to assign a user to a role
	- Revoke 
		- Revokes the access rights
- Typical access rights are:
	- select
	- insert
	- update
	- delete
	- references

### Role-Based Access Control (RBAC)
- Role-based access control eases administrative burden and improves security 
- A database RBAC needs to provide the following capabilities:
	- create and delete roles
	- define permissions for a role
	- assign and cancel assignment of users to roles
- Categories of database users:
	- Application owner: an end user who owns database objects as part of an application
	- End user: an end user who operates on database objects via a particular application but does not own any of the database objects
	- Administrator: user who has administrative responsibility for part or all of the database
- 






















