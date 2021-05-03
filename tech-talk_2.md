# Blockchain for the Initiated

- link to slides in the chat

## How to think
- Maximalism vs multi-chain world
    - ETH killer, BTC killer
    - First mover advantage
- If you don't get it, focus on decentralization as a value prop

## Consensus

- Consensus mechanisms, how to achieve source of truth and maintain agreed upon state
- Not the only forms of consensus (POA), most relevant/interesting
- Trying to achieve consensus and maintain security
    - Avoiding double spends (Byzantine fault tolerance), fraudulent tx
    - Trying to prevent sibil attacks (DoS)
        - Tx fee, economic incentives, purpose of native token

Bitcoin and ETH - PoW and PoS
    - Definitions
    - not a deep dive; compare/contrast
    
- PoS
    - validators 
        - deterministic selection, incentivized to cooperate (confirm only valid tx) because of personal stake, locked in escrow
            - slashing - loss part of staked ETH
    - Results in less HW requirements to run a node = more decentralization
        - Still relatively untested at scale
    - sustainability = no miners, relies on economic incentives rather than power consumption
        - Environmental impact
    - security
        - need 51% of all staked ETH, or 51% of hash power
        - 32 ETH per validator, but also staking pools (both ce and decentralized)
    - scalable = unlocks sharding
        - Sharding - spliting DB into multiple instances each containing portion of whole dataset, hard to do with PoW bc of how it would dillute the amount of computing power across multiple shards      

### Layer 1/2

- Scale base layer 1 or offloading to another layer (off chain)
    - OSI model
    - layer 2 anchors its state into layer 1
- ETH Layer 2 Ecosystem
    - ETH 1 layer 1 = 15 tx/sec, layer 2 = 2-4k, ETH2 (w/ sharding) will still need layer 2 to handle 100k-million tx

### Scaling & Upgrading

- Blockchain trilema
- Heats up after major periods of congestion, results in high tx fees
    - Causes 2017 (ICOs, crypto kitties) and today (defi, yield farming)
- TX Street - network congestion
- Implementing solutions in decentralized projects
    - Ethereum roadmap to PoS (part of culture, difficulty bomb)
    - Taproot / soft forks / 
        - Privacy -> data compression/ommision -> scaling

### Examples

- Some are application specific (like state or payment channels)
    - Raiden, Lightning
    - only 2 tx submitted to base layer
- Side chains
    - compatible but independent blockchains
    - Polygon, xDai, Plasma
- Rollups of side chain transactions (1 tx sent to base layer)
    - execute tx outside layer 1, post tx data on layer 1
    - Succinct non-interactive argument of knowledge
    - ZK rollups and optimistic
- Problem to address: Composability and interoperability between different platforms choosing different scaling solutions (i.e., swaps are difficult if one chooses side chain, another chooses rollups)
- Institutional scaling (Coinbase), off chain transactions

## Web 3

Why scale? We're creating an entirely new, decentralized and censorship resistant internet
- WWW != internet
- History - 1 (read only, static), 2 (read-write), 3 (read-write-execute)
- Web3: Semantic Web - AI, 3d graphics, ubiquity, IOT
- Lesson learned, what wins out is not necessarily the "best"
    - TCP/IP, HTTP (not secure) 
    - ipv4 vs ipv6; 4.2B addresses, ipv6 introduced as draft as far back as 1998
        - introduced NAT and CIDR to anticipte ipv4 address exhaustion
    - Fat protocol (TCP doesn't capture value, rather it's the apps built on top of it)

#### Dapps

- interface with blockchain, change to client-server architecture for retrieving info
- permissionless

### P2P Messaging

- Status - Status is a secure messaging app, crypto wallet, and Web3 browser
    - decoupling username from physical persona

Privacy and web freedoms
- Deplatforming, deep fakes
- encryption
    - war on math
- If you have nothing to hide, you have nothing to fear
    - 4th amendment, Bernstein v US Dept of Justice, Carpenter v United States

## NFTs

- data file format for digital scarcity and ownership rights
- Beeple auction (3rd highest living artist) - Everydays — The First 5000 Days
- Jack Dorsey first tweet
- Games
- Top 10 Most Expensive NFT Art Sales (So Far) https://www.youtube.com/watch?v=5_6hRr6qgiw
- API - https://creatures-api.opensea.io/api/creature/1
- https://carbon.fyi/

## DeFi

- Whereas NFTs helps crypto tell its story to the cultural masses, DeFi tells the story of crypto to the financial masses

Defi = permissionless, open, censorship resistant, blockchain based

- new financial system, open to everyone, no banks/gov
- relies heavily on cryptography and smart contracts
- developed on Ethereum, Bitcoin is origin defi, others in the space

### Lending/borrowing

1. Dex
    - don't have to give up custody of the coins
    - liquidity pool (tokens locked in a smart contract)
        - Provider sets price of exchange pair, if price diverges creates arbitrage op, ratio of tokens dictates price
        <!-- - Provider receives a certain type of LP token, burn tokens to get back original tokens and receive fees
            - price adjustment determinist algorithm
        - larger pools mean less price impact on large trades, thus less slippage -->
        
    <!-- - Order books
        - buy/seller come together and place orders
        - market makers provide liquitity as buyer/seller try to converge on price
        - difficult to reproduce in defi model due to reliance on market makers, which can make an exchange illiquid
            - also trouble with tx speed and block time, plus gas fees for MM to update orders, must be Layer 2 -->
2. Stable coins
    - peg to USD without having to use dollars
    - proof of solvency
    - non-algorithmic stable coins (like USDC), company holds equivalent of USD (centralized, can be censored)
3. Lending and borrowing
- What you're about to see...
    - MakerDAO, borrowing DAI from myself by creating CDP with ETH
    - algorithmic, autonmous interest rate protocol
    - supply assets and make interest or use as collateral
    - collateralized debt position, over-collateralized
    - margin trading: use borrowed funds to increase a position in a certain asset

4. Risks
- financial risk (same for any type of investment)
- counterparty risk (how "de" is your defi?)
    - minimized by decentralization (can't seize/freeze/exit scam)
- smart contract risk
    - primary: contract the defi platform itself is based on
    - secondary: any contracts used as building blocks, not part of just this platform
        - composability
    - example: yield farming tool is primary, but employs a governance or multisig from another contract
- platform risk - Ethereum
    - bugs in underlying protocol (i.e., bug in the EVM); matures with time, makes system more stable
    - includes volatility and gas fees
    - example: DAI under collateralized during March crash of ETH
        - have to deleverage position or return DAI, couldn't do it bc gas fees were super high

### More

* Oracles
    - bring in outside info, have to trust source (central point of failure)
    - Chainlink
    - Randomness
        - challenge: computers are deterministic by their nature, blockchains are transparent
* Derivatives
    - derive value from performance of underlying asset
    - wrapped tokens
* Insurance
    - protection against smart contract failures
* Prediction Markets
* Lossless Lottery
* Yield Farming

## Open Source Projects
- Passion to get regulatory environment correct

=================