# csci368-network-security-session-4-assignment-1-solution
**TO GET THIS SOLUTION VISIT:** [CSCI368 Network Security Session 4 Assignment 1 Solution](https://www.ankitcodinghub.com/product/csci368-network-security-session-4-assignment-1-solution/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;8010&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;5&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (5 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSCI368 Network Security Session 4 Assignment 1 Solution&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (5 votes)    </div>
    </div>
Objectives

On completion of this assignment you should be able to:

 Understand some basic techniques for building a secure channel.

 Understand network programming.

Task description

You will implement a simplified version of the TLS/SSL protocol in this assignment. Write (Java or C/C++)

UDP programs allowing two parties to mutually authenticate each other and establish a secure communication

channel. For simplicity, let us call the programs “Host” and “Client”, which are executed by Alice and Bob,

respectively.

Alice and Bob share a common password PW, which contains 6 alphanumeric characters. Alice also has a

public and privacy key pair (pk, sk) for the RSA encryption scheme. They want to establish a secure

communication channel that can provide data confidentiality and integrity. This will be done via the following

steps: (1) perform a mutual authentication and key exchange protocol; and (2) use the shared session key

derived from the first step to secure the real communication.

Step 1 is done via the following mutual authentication and key exchange protocol:

1: A  B: pk

2: B  A: C1 = PKE pk(RK), C2 = SKERK(“Bob”||PW)

3: Alice decrypts C1 using sk to get RK, and then decrypt C2 to get “Bob”||PW. Alice checks PW and accepts

the connection if and only if the PW is correct.

Alice sends either “Successful” or “Unsuccessful” to Bob to indicate whether the connection is successful or

not.

In the above protocol, || denotes the string concatenation, PKE denotes the RSA encryption and SKE denotes

the RC4 stream cipher. RK is a random value selected from the message space of the PKE. Alice and Bob then

compute the shared session key as K = H(RK||PW) where H denotes the SHA-1 hash algorithm.

After establishing the session key, step 2 is achieved as follows:

1. whenever Alice wants to send a message M to Bob, Alice first computes h = H(K||M||K), and then computes

C = SKEK(M||h) and sends C to Bob;

2. upon receiving a ciphertext C, Bob first runs the decryption algorithm to obtain M||h. After that, Bob

computes h’ = H(K||M||K) and checks if h = h’. If the equation holds, then Bob accepts M; otherwise, Bob

rejects the ciphertext;

3. the same operations are performed when Bob sends a message to Alice.

Implementation guidelines

 Place Host and Client in two separate directories: Alice and Bob. The shared information (PW) is located

in a file under each directory.

 Generate a public and private key pair for the Host (i.e., Alice), and store the generated public and private

key pair in a file under Alice’s directory. The RSA modulus N must have at least 32 bits (i.e., the factors

p and q of N should have at least 16 bits).

 Alice executes Host.

– Host is running and listening to the opened port (you need to select a port for your code).

 Bob executes Client.

– Client (Bob) sends a connection request to Host.

– Client is ready and listens to the port.

 Alice and Bob perform the mutual authentication and key exchange protocol as outlined in Step 1.

 If Alice cannot successfully authenticate Bob in Step 1(3), then Alice quits the program after sending

“Unsuccessful” to Bob. Bob also quits the program after receiving “Unsuccessful” from Alice.

 If the connection is successfully established,

– Either Alice or Bob can send a message encrypted and authenticated by the key K. They type the

message on their own terminal. The message is processed by their code (Host or Client) according to

the step 2 given above.

– The received message is printed on the screen if decryption is successful. Otherwise, print

“decryption error” on the screen.

– To quit the program, the client should type “exit”.

You can choose to use some existing libraries or free source code to implement RC4 and SHA-1. You

should cite the source if you use a downloaded code.

How to run?

Your programs should run according to the protocol. Host and Client should be executed on different windows.

For convenience of marking, please use the local IP: 127.0.0.1 for the submitted version. For simplicity, there is

no GUI required in this assignment. That is, messages are simply typed on the window and printed on the

receiver’s window.

Files to be submitted:

All source codes (Do not submit any executable).

A readme file (text/ACSII only): instructions about how to compile and run your code.

A Makefile: for C++ programmers. Alternatively, you provide the compilation instruction in the readme.

Submission

Compress all the files to be submitted into a zip file and submit it via the submission link provided in the Moodle

site.

Late Submission: Penalty is 25% deduction per day (including weekends).

Marking

Mark distribution:

1. RSA key generation: 4 marks

2. Authentication and Key Exchange (Step 1): 8 marks

3. Data Communication (Step 2): 8 marks

The code that cannot be compiled or executed will receive a zero mark.

Plagiarism

A plagiarised assignment will receive a zero mark and be penalised according to the university rules. Plagiarism

detection software will be used.
