# Gambling dapp

General Description:​ This web application is designed to allow gambling in a decentralized way. Users can place their bets on certain random events (e.g. Coin Flip, Dice roll, etc). Once the outcome of the random event is revealed, users that predicted the outcome will be automatically disbursed.
Motivation: ​Gambling is never a fair game, people are always losing in the long run because of the house edge. Whatsmore, the outcome of the game itself might be manipulated by the house especially in online gambling. How do we ensure the results of the game won’t be changed by the online casino in the backend? Does the online casino truly randomize the outcome? Will they actually give the return if I win? All in all, these are all about the banker’s trust issue. However, using blockchain technology might be a suitable solution as there will be no “middle man” when gambling. Hence, people will have a more safe environment and they do not have to pin their hope on the reliability of the casino.
Why Blockchain:
1. Trust issues with the casino are eliminated with the characteristics of blockchain.
2. No “middleman” is needed. Fees for the casino do not apply. There is no house edge.
3. Protect the outcome so that manipulating the odds in the backend become impossible.
4. User with correct bets are guaranteed to get their reward since all the bets are held by the blockchain. With
the smart contract, the reward will be automatically released.
Workflow/Technical approach: ​Sources of Randomness are a major issue in Blockchain Applications. Ethereum in particular offers no in-built pseudo random number generator. We will use a commit-reveal scheme similarly as described in this article under “Commit-reveal approach”: ​https://bit.ly/2GoZDJp
1. Commit Phase: Participants generate a seed, hash it and submit it’s hash to the contract, alongside the number they are betting on and the amount of currency they place on it.
2. Reveal Phase: Once all participants have submitted their hashed seed, they reveal their seed by sending it in cleartext to the contract, which in turn verfies them.
3. Then these seeds and a blockhash are hashed together. This hash is in turn used to generate a pseudo random number. The submitted currency is distributed among the winners.
The commit-reveal scheme suffers from participants being able to withhold their cleartext seed after they have submitted their hash. However in the context of a gambling game participants are incentivised to reveal their seed as they will have had to place their bet and commit with currency during the first seed submission.
Challenges:
1. Generate random event on the blockchain to ensure the result is secure and can not be manipulated
2. Implement a sufficient User Interface enabling easy interaction with the blockchain/smart contract
Project Schedule:
1. Create a Dice gambling system based on blockchain with a built-in random number generator.
2. Implement our own random number generator on that system.
3. Implement the frontend part, UI design, connecting with the backend, etc.
4. Test all functionality together with frontend and backend.
