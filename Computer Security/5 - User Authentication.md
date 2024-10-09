### System Identity and Authentication
- An identity on a system is typically a unique identifier 
- All actions on a system are associated with at least one identity 
- This identifier will be used to check what actions a user can perform - Access Control
- This identifier will be associated with the records in log files - Accountability
- The process by which a user, whether human or software, is associated with an identity is User Authentication
- To authenticate, the user is typically required to show evidence that they are who they claim 
- This evidence is the factor

### Four User Identity Attributes
- Something the individuals knows
	- Password, PIN, answers to prearranged questions
- Something individual possesses (token)
	- Smart card, electronic key card, physical key
- Something the individual is (static biometrics)
	- Fingerprint, retina, face
- Something the individual does (dynamic biometrics)
	- Voice pattern, handwriting, typing rhythm

### Risk Assessment for User Authentication
Three separate concepts:
Assurance Level -> Potential impact -> Areas of risk

### Assurance Level
- Describes an organization's degree of certainty that a user has presented a credential that refers to his or her identity 
- More specifically is defined as:
	- The degree of confidence in the vetting process used to establish the identity of the individual to whom the credential was issued
	- The degree of confidence that the individual who uses the credential is the individual to whom the credential was issued
- Four levels of assurance
	1. Little or no confidence in the asserted identity's validity
	2. Some confidence in the asserted identity's validity
	3. High confidence in the asserted identity's validity 
	4. Very high confidence in the asserted identity's validity

## Potential Impact
- FIPS 199 defines three levels of potential impact on organizations or individuals should there be a breach of security:
	- Low : An authentication error could be expected to have a limited adverse effect on organizational operations, organizational assets, or individuals
	- Moderate : An authentication error could be expected to have a serious adverse effect
	- High : An authentication error could be expected to have a severe or catastrophic adverse effect

## Password-Based Authentication
- Widely used line of defense against intruders 
	- User provides name/login and password
	- System compares password with the one stored for that specified login 
	- If passed, user is represented by their identity or user ID within the runtime
- The user ID is the token identifying the user in the system
	- Determines that the user is authorized to access the system
	- Determines the user's privileges
	- Is used in discretionary access control
	- Used as part of the logging entry for logged actions

## Password Storage
- Passwords need to be stored in the system
	- Should they be stored as the actual password
- Can passwords be stored encrypted, e.g., by a Secure Hash Algorithm
	- Hash function applied to password after entry and compared to hashed value in the file
	- Prevents casual password scavenging, but...
- Dictionary Attacks
	- Attackers gets a dictionary, and applies hash function to each entry
	- Most passwords are single words, so attacker can search through password file to match entries 
	- Attacker can apply common password addition rules to generate further match possibilities, such as numbers at the end, punctuation of the end, 1337 speak
- Salt
	- Using a random number prefix on the password reduces the effectiveness of dictionary attacks

## Password Vulnerabilities
1. Offline dictionary attack 
2. Specific account attack 
3. Popular password attack
4. Password guessing against single user 
5. Workstation hijacking
6. Exploiting user mistakes
7. Exploiting multiple password use
8. Electronic monitoring

## UNIX Implementation
#### Original Scheme
- Up to eight printable characters in length 
- 12-bit salt used to modify DES encryption into a one-way hash function
- Zero value repeatedly encrypted 25 times 
- Output translated to 11 character sequence
#### Now regarded as inadequate
- Still often required for compatibility with existing account management software or multi-vendor environments

## Password Cracking
###### Dictionary attacks
- Develop a large dictionary of possible passwords and try each against the password file
- Each password must be hashed using each salt value and then compared to stored hash values
###### Password crackers exploit the fact that people choose easily guessable passwords 
- Shorter password lengths are also easier to crack
###### Rainbow table attacks
- Pre-compute tables of hash values for all salts 
- A mammoth table of hash values
- Can be countered by using a sufficiently large salt value and a sufficiently large hash length 
###### John the Ripper 
- Open-source password cracker first developed in 1996
- Uses a combination of brute-force and dictionary techniques

## Modern Approaches 
- Complex password policy
	- Forcing users to pick stronger passwords
- However, password-cracking techniques have also improved
	- The processing capacity available for password cracking has increased dramatically (e.g., GPUs)
	- The use of sophisticated algorithms to generate potential passwords (e.g., standard Markov modeling techniques from natural language processing)
	- Studying examples and structures of actual passwords in use

Password Selection Strategies
- User education:
	Users can be told the importance of using hard to guess passwords and can be provided with guidelines for selecting strong passwords
- Computer generated passwords
	Users have trouble remembering them. Passwords managers can help.
- Reactive password checking 
	System periodically runs its own password cracker to find guessable passwords
- Complex password policy
	Users is allowed to select their own password; however, the system checks to see if the password is allowable, and if not, rejects it. Goal is to eliminate guessable passwords while allowing the user to select a password that is memorable

## Memory Cards
- Can store but do not process data
- The most common is the magnetic stripe card
- Can include an internal electronic memory
- Can be used alone for physical access
	- Hotel room
	- ATM
- Provides significantly greater security when combined with a password or PIN 
- Drawbacks of memory cards include:
	- Requires a special reader
	- Loss of token
	- User dissatisfaction

## Smart Tokens
- Physical characteristics:
	- Include an embedded microprocessor
	- A smart token that looks like a bank card
	- Can look like calculators, keys, small portable objects
- User interface:
	- Manual interfaces include a keypad and display for human/token interaction
- Electronic interface
	- A smart card or other token requires an electronic interface to communicate with a compatible reader/writer
	- Contact and contactless interfaces
- Authentication protocol which is classified into three categories:
	- Static
	- Dynamic password generator
	- Challenge-response

## Smart Cards
- Most important category of smart token
	- Has the appearance of a credit card
	- Has an electronic interface 
	- May use any of the smart token protocols
- Contain : An entire microprocessor 
	- Processor
	- Memory
	- I/O ports
- Typically include three types of memory:
	- Read-only memory (ROM) : Stores data that does not change during the card's life
	- Electronically erasable programmable ROM (EEPROM)
		- Holds application data and programs
	- Random access memory (RAM)
		- Holds temporary data generated when applications are executed

## Electronic Identity Cards (eID)
1. Use of a smart card as a national identity card for citizens
2. Can serve the same purposes as other national ID cards, and similar cards such as a driver's license, for access to government and commercial services
3. Can provide stronger proof of identity and can be used in a wider variety of applications
4. In effect, is a smart card that has been verified by the national government as valid and authentic - around 3.6 billion worldwide

## Smart Phones
- Physical characteristics:
	- Open market for software applications
	- Standard user interface experience 
	- In 2023, 6.9 billion smart phone subscriptions worldwide
	- By Oct. 2024, 71.85% Android, 27.6% Apple
- Authentication protocol:
	- Can utilize directly for two factor authentication, by SMS or other mechanisms 
	- Install Authenticator apps
- We will discuss more in Internet authentication

## Biometric Authentication
- Attempts to authenticate an individual based on unique physical characteristics 
- Based on pattern recognition
- Is technically complex and expensive when compared to passwords and tokens
- Physical characteristics used include:
	- Facial characteristics 
	- Fingerprints
	- Hand geometry
	- Retinal pattern
	- Iris
	- Signature
	- Voice
## Remote User Authentication
- Authentication over a network, the Internet, or a communications link is more complex 
- Additional security threads such as:
	- Eavesdropping, capturing a password, replaying an authentication sequence that has been observed 
- Generally, reply on some form of a challenge-response protocol to counter threads

## Federated Identity Management
- Relatively new concept dealing with the use of a common identity management scheme across multiple enterprise and numerous applications and supporting many users
- Services provided include:
	- Point of contact
	- SSO protocol services
	- Trust services
	- Key services
	- Identity services
	- Authorization
	- Provisioning 
	- Management

## Identity Management
- A centralized, automated approach to provide enterprise-wide access to resources by employees and other authorized individuals 
- The focus of identity management is defining and identity for each user (human or process), associating attributes with the identity, and enforcing a means by which a user can verify identity
- The central concept of an identity management system is the use of single sign-on (SSO)
- SSO enables a user to access all network resources after a single authentication



 





