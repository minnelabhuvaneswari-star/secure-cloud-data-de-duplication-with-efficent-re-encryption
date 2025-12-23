# secure-cloud-data-de-duplication-with-efficent-re-encryption
Data de duplication technique has been widely adopted by commercial cloud storage providers, which is both important and necessary in coping with the explosive growth of data. To further protect the security of users’ sensitive data in the outsourced storage mode, many secure data de duplication schemes have been designed and applied .
Secure Cloud Data De duplication with Efficient Re-Encryption
ABSTRACT
Data de duplication technique has been widely adopted by commercial cloud storage providers, which is both important and necessary in coping with the explosive growth of data. To further protect the security of users’ sensitive data in the outsourced storage mode, many secure data de duplication schemes have been designed and applied in various scenarios. Among these schemes, secure and efficient re-encryption for encrypted data de duplication attracted the attention of many scholars, and many solutions have been designed to support dynamic ownership management. In this Project, focus on the re-encryption de duplication storage system and show that the recently designed lightweight rekeying-aware encrypted de duplication scheme (REED) is vulnerable to an attack which call it stub-reserved attack. Furthermore, propose a secure data de duplication scheme with efficient re-encryption based on the convergent all-or-nothing transform (CAONT) and randomly sampled bits from the Bloom filter. Due to the intrinsic property of one-way hash function, our scheme can resist the stub-reserved attack and guarantee the data privacy of data owners’ sensitive data. Moreover, instead of re-encrypting the entire package, data owners are only required to re-encrypt a small part of it through the CAONT, there by effectively reducing the computation overhead of the system. Finally, security analysis and experimental results show that our scheme is secure and efficient in re-encryption.
Keywords : secure, property, analysis, transform.








INTRODUCTION
In the recent decades, cloud-based storage service has attracted considerable attention from both academia and industries. It may be widely used in many Internet-based commercial applications (e.g., Apple iCould) due to its long-list benefits including access flexibility and free of local data management. Increasing number of individuals and companies nowadays prefer to outsource their data to remote cloud in such a way that they may reduce the cost of upgrading their local data management facilities/devices. However, the worry of security breach over outsourced data may be one of the main obstacles hindering Internet users from widely using cloud-based storage service. In many practical applications, outsourced data may need to be further shared with others. For example, a Dropbox user Alice may share photos with her friends.
To prevent shared photos being accessed by the “insiders” of the system, a straightforward way is to designate the group of authorized data users prior to encrypting the data. In some cases, nonetheless, Alice may have no idea about who the photo receivers/users are going to be. It is possible that Alice only has knowledge of attributes w.r.t. photo receivers. In this case, traditional public key encryption (e.g., Paillier Encryption), which requires the encryptor to know who the data receiver is in advance, cannot be leveraged. Providing policy-based encryption mechanism over the outsourced photos is therefore desirable, so that Alice makes use of the mechanism to define access policy over the encrypted photos to guarantee only a group of authorized users is able to access the photos.
A strawman solution to the control of download request is to leverage dummy ciphertexts to verify data receiver’s decryption rights. It, concretely, requires data owner, say Alice, to upload multiple “testing” ciphertexts along with the “real” encryption of data to cloud, where the “testing” ciphertexts are the encryptions of dummy messages under the same access policy as that of the “real” data. After receiving a download request from a user, say Bob, cloud asks Bob to randomly decrypt one of the “testing” ciphertexts. If a correct result/decryption is returned (i.e. indicating Bob is with valid decryption rights), Bob is authorized by Alice to access the ”real” data, so that the cloud allows Bob to download the corresponding ciphertext.


LITERATURE SURVEY

Author Name
	Title of the Paper
	Techniques Used
	Limitations

W Lou and Y T Hou	Charm: a framework for rapidly prototyping cryptosystems	Modular Design	Although Charm integrates with optimized C libraries (such as PBC and GMP)
Y Lang and W Young	Innovative Technology for CPU Based Attestation and Sealing	Trusted Execution Environments	Attacks that occur after the attestation process may go undetected
D Kamwar and M Schlosser	Modern Family: A Revocable Hybrid Encryption Scheme Based on Attribute-Based Encryption, Symmetric Searchable Encryption and SGX	Symmetric Searchable Encryption	Only users whose attributes match the policy defined in the encryption key can decrypt the data.
S Pope	Secure Schemes for Secret Sharing and Key Distribution	Verifiable Secret Sharing	This is crucial in scenarios where participants may not trust the dealer
X. Chen	Verifiable computation over large database with incremental updates	Merkle Trees	The root hash is a compact representation of the entire dataset.
M. Gerla	Pics-on-wheels: Photo surveillance in the vehicular cloud	Vehicular Cloud Computing	The data captured by vehicles is processed and stored either locally on vehicles or in centralized cloud systems
J. Li, J. Ma	New algorithms for secure outsourcing of modular exponentiations	Blinding Techniques	Outsourcing requires sending inputs to an external server and receiving the results back.
H. Yuan	Dedupdum: Secure and scalable data deduplication with dynamic user management	Hashing Techniques	This may introduce latency, especially during initial uploads or large data migrations.










EXISTING SYSTEM
In Existing System, To apply fine-grained policy-based control over encrypted data, Attribute Based Encryption has been introduced in the literature. Concretely, Attribute Based Encryption has two main research branches: one is Ciphertext Policy-Attribute Based Encryption, and the other is KP-ABE which refers to as keypolicy ABE. Existing System mainly deals with the former. In a Ciphertext Policy-Attribute Based Encryption, decryption key is associated with attribute set and ciphertext is embedded with access policy. This feature makes Ciphertext Policy-Attribute Based Encryption quite suitable for secure cloud data sharing. Note this is so because KP-ABE requires decryption key to be associated with access policy which yields heavy storage cost for cloud user. Although being able to support fine-grained data access, Ciphertext Policy-Attribute Based Encryption, acting as a single solution, is far from practical and effective to hold against EDoS attack. However, suffers from two disadvantages. First, the data owner is required to generate a set of challenge ciphertexts in order to resist the attack, which enhances its computational burden. Second, a data user is required to decrypt one of the challenges ciphertexts as a test, which costs a plenty of expensive operations (e.g., pairing). Here the computational complexity of both parties is inevitably increased and meanwhile, high network bandwidth is required for the delivery of ciphertexts. The considerable computational power of cloud is not fully considered
DISADVANTAGES OF EXISTING SYSTEM
Potential Information Leakage
Low Efficiency
More Computational Burden
Plenty of Expensive Operations
No Confidentiality on outsourced data



PROPOSED SYSTEM
In Proposed System, Presenting two secure and efficient cloud-based dual access control systems in different contexts. With the aim of providing an efficient way of dual access control, we briefly introduce the technical roadmap as follows. To guarantee the confidentiality of outsourced data without loss of policy-based access control, we start with a Ciphertext Policy-Attribute Based Encryption system, which is seen as one of the building blocks. We further employ an effective control over data users’ download request on the top of the Ciphertext Policy-Attribute Based Encryption system. We design a new approach to avoid using the technique of “testing” ciphertext. Specifically, we allow data user to generate a download request. Upon receiving the download request, with help of the authority, a cloud server is able to check if the data user is authorized to gain access to the data. No other information is revealed to the cloud server except the knowledge of whether the user is authorized
ADVANTAGES OF PROPOSED SYSTEM
No Potential Information Leakage
High Efficiency
Confidentiality on outsourced data
Fine-grained access control over outsourced (encrypted) data
Control over anonymous download request







SYSTEM REQUIREMENTS
HARDWARE REQUIREMENTS
Processor- Intel (R) Core (TM) i3-4200U
CPU - 1.6GHz
RAM:4 GB
Hard Disk: 40 GB.
SOFTWARE REQUIREMENTS
Operating System 		-	Windows 10
Server                                      -           Apache Tomcat
Front End			-	HTML, CSS,  JS
Back End		            -           JSP
Data base                                  -           MYSQL Server 5.0














BLOCK DIAGRAM















MODULES

There are Four Modules in the Proposed System:
1.Cloud
2.Data Owner 
3.End User
4.Trusted Authority

1.Cloud
In this module, the functionalities are as follows: View & Authorize Data Owner, View & Authorize End user, View Files with Master Secret key, View MSK Req / Res Time, View files with out master secret key
2.Data Owner
In this module, the data owner uploads their data in the cloud server. For the security purpose the data owner encrypts the file and then store in the cloud. The data owner can have capable of updating and deleting of a specific file. And also he can view the transactions based on the files he uploaded to cloud.
 3. End User 
In this module, receivers logs in by using his/her user name and password. After Login receiver will Search for files and request for secret key of a particular file from Authority, and get the secret key. After getting secret key he is trying to download file by entering file name and secret key from cloud server. 
4. Trusted Authority
In this module, the  authority helps to check transaction of files and also. If receiver exists and the profile. Authority also view the requests from the receivers and generates the secret key and send to the requested data receivers.
ALGORITHM
AES
These days, security is the primary concern for everyone in IT. Given that $155 billion in expenditure on information security and risk management is expected to increase to $172 billion in 2022, according to Gartner, it must be. While there are many tools you can purchase to protect your data, encryption is one security tool that every computer user should be familiar with. A cryptographic "break" for cryptographers is anything quicker than a brute-force assault, which involves decrypting one trial key at a time. Thus, a break can produce outcomes that are now technologically impossible. Although theoretical breakdowns are useless, they occasionally reveal vulnerability patterns. In 2006, distributed.net conducted the greatest known successful brute-force assault on a widely used block-cipher encryption technique using a 64-bit RC5 key.
Why Encryption Is Useful?
Encryption is a technique for making data messages or files unreadable, guaranteeing that only a person with the proper authorization may access that data. Data is encrypted using sophisticated algorithms, and the same data is then decrypted using a key that is supplied by the message's sender. Information is kept secret and confidential by encryption while it is being stored or sent. Any unauthorized access will just reveal a disorganized collection of bytes.
You should be familiar with the following concepts related to encryption:
Algorithm:
Algorithms, sometimes referred to as ciphers, are the guidelines or directions for the encryption procedure. The efficiency of the encryption depends on the key length, capabilities, and characteristics of the employed encryption method.
Decryption:
Decryption is the process of turning unintelligible cipher text into understandable data.


Key:
A random string of bits called an encryption key is used to encrypt and decode data. Longer keys are more difficult to break, and each key is different. Public keys typically have a length of 2048 bits, whereas private keys often have 128 or 256 bits.
Asymmetric and symmetric cryptographic key schemes are both available.
Symmetric Keys Systems:
Everyone who accesses the data in a symmetric key system uses the same key. To maintain anonymity, encryption and decryption keys must also be kept a secret. While this is technically conceivable, it is impracticable to employ symmetric encryption for extensive commercial usage due to the need for securely distributing the keys to guarantee the right controls are in place.
Asymmetric Keys Systems
A public/private key system, sometimes referred to as an asymmetric key system, employs two keys. The private key is the only key that is kept a secret, although everyone else has access to the other key. The public key is what is known as. Due to the mathematical connection between the private and public keys, only the appropriate private key may decode data that has been encrypted with the help of the public key.










UML DIAGRAMS
The Unified Modelling Language (UML) is a standard language for specifying, visualizing, constructing, and documenting the artifacts of software systems, as well as for business modeling and other non-software systems. The UML represents a collection of best engineering practices that have proven successful in the modeling of large and complex systems. The UML is a very important part of developing objects oriented software and the software development process. The UML uses mostly graphical notations to express the design of software projects. Using the UML helps project teams communicate, explore potential designs, and validate the architectural design of the software.
As the strategic value of software increases for many companies, the industry looks for techniques to automate the production of software and to improve quality and reduce cost and time-to-market. These techniques include component technology, visual programming, patterns and frameworks. Businesses also seek techniques to manage the complexity of systems as they increase in scope and scale. In particular, they recognize the need to solve recurring architectural problems, such as physical distribution, concurrency, replication, security, load balancing and fault tolerance. Additionally, the development for the World Wide Web, while making some things simpler, has exacerbated these architectural problems. The Unified Modeling Language
 
(UML) was designed to respond to these needs. Simply, Systems design refers to the process of defining the architecture, components, modules, interfaces, and data for a system to satisfy specified requirements which can be done easily through UML diagrams.
Object-Oriented Concepts
UML can be described as the successor of object-oriented (OO) analysis and design.
An object contains both data and methods that control the data. The data represents the state of the object. A class describes an object and they also form a hierarchy to model the real-world system. The hierarchy is represented as inheritance and the classes can also be associated in different ways as per the requirement.
Objects are the real-world entities that exist around us and the basic concepts such as abstraction, encapsulation, inheritance, and polymorphism all can be represented using UML.
UML is powerful enough to represent all the concepts that exist in object-oriented analysis and design. UML diagrams are representation of object-oriented concepts only. Thus, before learning UML, it becomes important to understand OO concept in detail.
Following are some fundamental concepts of the object-oriented world −
Objects − Objects represent an entity and the basic building block.
Class − Class is the blue print of an object.
Abstraction − Abstraction represents the behavior of an real world entity.
Encapsulation − Encapsulation is the mechanism of binding the data together and hiding them from the outside world.
Inheritance − Inheritance is the mechanism of making new classes from existing ones.
Polymorphism − It defines the mechanism to exists in different forms.
OO Analysis and Design
OO can be defined as an investigation and to be more specific, it is the investigation of objects. Design means collaboration of identified objects.
Thus, it is important to understand the OO analysis and design concepts. The most important purpose of OO analysis is to identify objects of a system to be designed. This analysis is also done for an existing system. Now an efficient analysis is only possible when we are able to start thinking in a way where objects can be identified. After identifying the objects, their relationships are identified and finally the design is produced.
The purpose of OO analysis and design can described as −
Identifying the objects of a system.
Identifying their relationships.
Making a design, which can be converted to executables using OO languages.
There are three basic steps where the OO concepts are applied and implemented. The steps can be defined as
OO Analysis → OO Design → OO implementation using OO languages
The above three points can be described in detail as −
During OO analysis, the most important purpose is to identify objects and describe them in a proper way. If these objects are identified efficiently, then the next job of design is easy. The objects should be identified with responsibilities. Responsibilities are the functions performed by the object. Each and every object has some type of responsibilities to be performed. When these responsibilities are collaborated, the purpose of the system is fulfilled.
The second phase is OO design. During this phase, emphasis is placed on the requirements and their fulfilment. In this stage, the objects are collaborated according to their intended association. After the association is complete, the design is also complete.
The third phase is OO implementation. In this phase, the design is implemented using OO languages such as Java, C++, etc.
ROLE OF UML IN OO DESIGN
UML is a modeling language used to model software and non-software systems. Although UML is used for non-software systems, the emphasis is on modeling OO software applications. Most of the UML diagrams discussed so far are used to model different aspects such as static, dynamic, etc. Now whatever be the aspect, the artifacts are nothing but objects.
Hence, the relation between OO design and UML is very important to understand. The OO design is transformed into UML diagrams according to the requirement.
In this project ,basic UML diagrams have been explained
 
Use Case Diagram
Class Diagram
Sequence Diagram
Collaboration Diagram
Activity Diagram
Deployment Diagram
1.CLASS DIAGRAM
UML class diagrams model static class relationships that represent the fundamental architecture of the system. Note that these diagrams describe the relationships between classes, not those between specific objects instantiated from those classes. Thus the diagram applies to all the objects in the system.
 
A class diagram consists of the following features:
 
Classes: These titled boxes represent the classes in the system and contain information about the name of the class, fields, methods and access specifies. Abstract roles of the Class in the system can also be indicated
Interfaces: These titled boxes represent interfaces in the system and contain information about the name of the interface and its methods. Relationship Lines that model the relationships between classes and interfaces in the system.
Dependency: A dotted line with an open arrowhead that shows one entity depends on the behavior of another entity. Typical usages are to represent that one class instantiates another or that it uses the other as an input parameter



Fig 1. Class Diagram
2.USECASE DIAGRAM
A use case diagram in the Unified Modelling Language (UML) is a type of behavioural diagram defined by and created from a Use-case analysis. Its purpose is to present a graphical overview of the functionality provided by a system in terms.
A use case is a methodology used in system analysis to identify, clarify, and organize system requirements. The use case is made up of a set of possible sequences of interactions between systems and users in a particular environment and related to a particular goal. It consists of a group of elements (for example, classes and interfaces) that can be used together in a way that will have an effect larger than the sum of the separate elements combined. The use case should contain all system activities that have significance to the users. A use case can be thought of as a collection of possible scenarios related to a particular goal, indeed, the use case and goal are sometimes considered to be synonymous.The main purpose of a use case diagram is to show what system functions are performed for which actor. Roles of the actors in the system can be depicted.
Parts of Use Case Diagram
System boundary boxes (optional)
 
A rectangle is drawn around the use cases, called the system boundary box, to indicate the scope of system. Anything within the box represents functionality that is in scope and anything outside the box is not 
Relationships.
 
Include
In one form of interaction, a given use case may include another. "Include is a Directed Relationship between two use cases, implying that the behavior of the included use case is inserted into the behavior of the including use case”.
 
The first use case often depends on the outcome of the included use case. This is useful for extracting truly common behaviours from multiple use cases into a single description. The notation is a dashed arrow from the including to the included use case, with the label "«include»". This usage resembles a macro expansion where the included use case behavior is placed inline in the base use case behavior. There are no parameters or return values. To specify the location in a flow of events in which the base use case includes the behavior of another, you simply write include followed by the name of use case you want to include, as in the following flow for track order.
Extend
 
In another form of interaction, a given use case (the extension) may extend another. This relationship indicates that the behavior of the extension use case may be inserted in the extended use case under some conditions. The notation is a dashed arrow from the extension to the extended use case, with the label "«extend»". The notes or constraints may be associated with this relationship to illustrate the conditions under which this behavior will be executed. Modelers use the «extend» relationship to indicate use cases that are "optional" to the base use case. Depending on the modeler’s approach "optional" may mean "potentially not executed with the base use case" or it may mean "not required to achieve the base use case goal".


2.1 Use case Diagram for  Data Owner























Fig 2.1 Use case Diagram for Data Owner






2.2 Use case Diagram for End user 












Fig 2.2 Use case Diagram For End user
2.3 Use case Diagram for Trusted Authority 














Fig 2.3 Use case Diagram For Trusted Authority

2.4 Use case Diagram for Cloud 


























Fig 2.4 Use case Diagram For Cloud



3.SEQUENCE DIAGRAM
A sequence diagram in Unified Modelling Language (UML) is a kind of interaction diagram that shows how processes operate with one another and in what order. It is a construct of a Message Sequence Chart. A Sequence diagram depicts the sequence of actions that occur in a system. The invocation of methods in each object, and the order in which the invocation occurs is captured in a Sequence diagram. This makes the Sequence diagram a very useful tool to easily represent the dynamic behavior of a system.
Elements of sequence diagram
The sequence diagram is an element that is used primarily to showcase the interaction that occurs between multiple objects. This interaction will be shown over certain period of time. Because of this, the first symbol that is used is one that symbolizes the object.
Lifeline
A lifeline will generally be generated, and it is a dashed line that sits vertically, and the top will be in the form of a rectangle. This rectangle is used to indicate both the instance and the class. If the lifeline must be used to denote an object, it will be underlined.
Messages
To showcase an interaction, messages will be used. These messages will come in the form of horizontal arrows, and the messages should be written on top of the arrows. If the arrow has a full head, and it’s solid, it will be called a synchronous call. If the solid arrow has a stick head, it will be an asynchronous call. Stick heads with dash arrows are used to represent return messages.
Objects
Objects will also be given the ability to call methods upon themselves, and they can add net activation boxes. Because of this, they can communicate with others to show multiple levels of processing. Whenever an object is eradicated or erased from memory, the "X" will be drawn at the lifeline's top, and the dash line will not be drawn beneath it. This will often occur as a result of a message. If a message is sent from the outside of the diagram, it can be used to define a message that comes from a circle that is filled in. Within a UML based model, a Super step is a collection of steps which result from outside stimuli.


Steps to Create Sequence Diagram
Set the stage for the interaction by identifying which objects play a role in interaction.
Set the lifetime for each object.
 


 
                                         
Fig 3. Sequence Diagram





4.ACTIVITY DIAGRAM
Activity diagram is another important diagram in UML to describe dynamic aspects of the system. Activity diagram is basically a flow chart to represent the flow form one activity to another activity. The activity can be described as an operation of the system. So the control flow is drawn from one operation to another. This flow can be sequential, branched or concurrent. Activity diagrams deals with all type of flow control by using different elements like fork, join etc.
How to draw Activity Diagram?
Activity diagrams are mainly used as a flow chart consists of activities performed by the system. But activity diagram are not exactly a flow chart as they have some additional capabilities. These additional capabilities include branching, parallel flow, swim lane etc. Before drawing an activity diagram we must have a clear understanding about the elements used in activity diagram. The main element of an activity diagram is the activity itself. An activity is a function performed by the system. After identifying the activities we need to understand how they are associated with constraints and conditions. So before drawing an activity diagram we should identify the following elements.
 
Activities
Association
Conditions
Constraints
 
The following are the basic notational elements that can be used to make up a diagram:
Initial state
An initial state represents a default vertex that is the source for a single transition to the default state of a composite state. There can be at most one initial vertex in a region. The outgoing transition from the initial vertex may have a behavior, but not a trigger or guard. It is represented by Filled circle, pointing to the initial state.
Final state
A special kind of state signifying that the enclosing region is completed. If the enclosing region is directly contained in a state machine and all other regions in the state machine also are completed, then it means that the entire state machine is completed. It is represented by Hollow circle containing a smaller filled circle, indicating the final state.
Rounded rectangle
It denotes a state. Top of the rectangle contains a name of the state. Can contain a horizontal line in the middle, below which the activities that are done in that state are indicated.
Arrow
It denotes transition. The name of the event (if any) causing this transition labels the arrow body.
4.1 Activity Diagram for Data Owner

                             












Fig 4.1 Activity Diagram for Data Owner

4.2 Activity Diagram for Cloud 

                                 













Fig 4.2 Activity Diagram for Cloud



4.3 Activity Diagram for End User

                                 














Fig 4.3Activity Diagram for End User



4.4 Activity Diagram for Trusted Authority

                                 














Fig 4.4 Activity Diagram for Trusted Authority



5.DEPLOYMENT DIAGRAM
Deployment diagram represents the deployment view of a system .It is related to the Component diagram. Because the components are deployed using the deployment diagrams. A deployment diagram consists of nodes. Nodes are nothing but physical Hardware’s used to deploy the Applications.
 

 
 
Fig 5. Deployment Diagram
 
 
 
 
 
 
 
 
 


6.COLLABORATION DIAGRAM
A collaboration diagram, also known as a communication diagram, is an illustration of the relationships and interactions among software objects in the Unified Modeling Language (UML). These diagrams can be used to portray the dynamic behavior of a particular use case and define the role of each object.
 


 
 
 
Fig 6. Collaboration Diagra
