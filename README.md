# Full-Stack-Blockchain

<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/krishnakaushik25/Full-Stack-Blockchain">
    <img src="images/logo.jpg" alt="Logo" width="600" height="350">
  </a>

  <h3 align="center">A complete blockchain-powered cryptocurrency Full-Stack Application</h3>

  <p align="center">
    <br />
    <a href="https://protected-sierra-05982.herokuapp.com/">View Demo</a>
    ·
    <a href="https://github.com/krishnakaushik25/Full-Stack-Blockchain/issues">Report Bug</a>
    ·
    <a href="https://github.com/krishnakaushik25/Full-Stack-Blockchain/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a></li>
    <li><a href="#Project Takeaways">Project Takeaways</a></li>
    <li><a href="#Project Challeneges and Further Enhancements">Further Improvements</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
    
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project



Star⭐ the repo if you like what you see😉.

I’m a firm believer in the concept of building a technology from scratch to learn it thoroughly and know what it is doing under the hood.The best way to understand blockchain is to build one..
Naturally, my interest in blockchain technology has led me to try to build a blockchain and its concepts from scratch. The blockchain has become a magic bullet in the software world throughout the past few years. 
It’s proven that it has the power to revolutionize economic systems and so much more.

The blockchain basic work flow can be seen in this below picture.
[![Product work Flow][product-work-flow]](https://www.linkpicture.com/q/Blockchain-work.jpg)

The project includes building a full backend,testing suite,a frontend web app and deploying the project.Before we deploy our application, we should thoroughly test it.
I’ve included sample integration tests with JavaScript by using [Jest JS framework](https://jestjs.io/). Writing code in test-driven manner makes the application fully fucntional and unique too.
The tests are written in .test.js files in various folders and its simple to confirm the functionality of every code segment.

The project is deployed in [Heroku](https://www.heroku.com) - platform as a service (PaaS) tool that  operates applications entirely in the cloud.
The project application sample picture can be seen below.

[![Product Name Screen Shot][product-screenshot]](https://www.linkpicture.com/q/blockchain.png)

The list of resources that I used for building this project are listed in the acknowledgements.

Built With [Node.js](https://nodejs.org/en/), JavaScript, [Express](https://expressjs.com/), APIs, Publish/Subscribe, [React](https://reactjs.org/) - all these technologies are incorporated in this full-stack project.


<!-- Project Takeaways -->
## Project Takeaways
- Code a full-on backend with test-driven development.
- Write a full test suite for the backend.
- Build a Blockchain in the object-oriented programming style.
- Create a full frontend React.js web application.
- Deploy the application to production (with multiple servers).
- Create an API around the Blockchain.
- Create a real-time connected peer-to-peer server with a pub/sub implementation.
- Implement a proof-of-work algorithm.
- Sign Transactions with cryptography and digital signature.
- Create a Transaction Pool for a real-time list of incoming data.
- Include transactions in core blocks of the chain.


<!-- Further Improvements -->
## Project Challeneges and Further Enhancements

##### I want to extend some of the below ideas in the future to make it more effective.

- Download the Blockchain to the File System

Currently, the blockchain completely lives in the JavaScript memory. Luckily, as long as there is one node in the system running, a copy of the current blockchain is stored. 
But if all nodes go down, the blockchain progress will die. One solution is to implement blockchain backups by adding a feature to download the blockchain to the file system. 
A straightforward option is to download the blockchain as json.


- Load the Blockchain from the File System

This follows up the previous challenge, which is to implement a feature where the blockchain can be downloaded from the file system. 
This challenge is to reload the blockchain in memory using an existing json file representing a chain. The benefit is quicker synchronization on startup for new peers, 
as well as restoring lost data if the JavaScript memory somehow loses the blockchain.



- Transaction Pool Socket Updates

Replace the polling logic in the transaction pool with real-time updates through socket.io. Continually polling the pool, even when there haven’t been any updates, 
could be overkill and eventually overload the server. But using socket.io for real-time updates is an alternate and more clean solution.


- Refactor the React app to use Redux

There are certain places in the application, where certain API requests are overdone. For example, the known-addresses, and wallet-info section are fetched on 
every component visit. But this can be fixed by redux which maintains an internal store. Plus, if the app has any logic where a smaller component needs to update
global state, redux would definitely come in handy.


- Fresh Keys Per Transaction

This challenge is to implement a solution to a possible attack vector which tracks a public key’s usage throughout many transactions, and attempts to decrypt its 
private key. A solution to this, is to implement a wallet, that creates a fresh set of keys on every transactions. It’s a lot more overhead - but perhaps more secure.

- Beef Up the Proof-of-Work and Display Mining Progress:

Beef up the proof-of-work algorithm by significantly increasing the MINING_RATE. Display real-time feedback of the proof-of-work algorithm in 
the frontend (socket.io could come in handy).



- Permissioned Access

Currently, anyone can visit the frontend so long as they know its public url. This means that anyone can issue a mining request on that frontend’s behalf.
With permissioned access, only authorized users should be able to access a frontend, and call its api requests (every api should check for an encrypted authorization header).


- Redis Clusters

To get servers communicating, they are all connecting to the same redis server. This has a limited number of connections.
A solution is implement a cluster of redis urls as the connections increase. That way, a different redis server can handle other servers.
The key is making sure that each redis server itself, communicates with each other, in a cluster fashion.


<!-- CONTRIBUTING -->
## Contributing
Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [Awesome github repo of BLockchain implementation in javascript](https://github.com/yjjnls/awesome-blockchain#implementation-of-blockchain)
* [The complete Youtube series of Creating a blockchain with Javascript with Angular front end](https://www.youtube.com/watch?v=zVqczFZr124&list=PLzvRQMJ9HDiTqZmbtFisdXFxul5k0F-Q4&index=1)
* [Github reference of David Katz cryptochain](https://github.com/15Dkatz/cryptochain)



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[product-screenshot]: images/blockchain.png
[product-work-flow]: images/Blockchain-work.jpg
