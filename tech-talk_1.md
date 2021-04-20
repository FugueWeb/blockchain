# Blockchain for the Initiated

- link to slides in the chat

## How to think
- Maximalism vs multi-chain world
    - ETH killer, BTC killer
    - First mover advantage
- If you don't get it, focus on decentralization as a value prop

## Proof of Work & Proof of Stake
- Trying to achieve consensus and maintain security
- Trying to prevent sibil attacks
- PoS; sustainability = no miners, security = harder to do 51% attack (need 51% of all ETH), scalable = unlocks sharding
    - Sharding - spliting DB into multiple instances each containint portion of whole dataset
- Results in less HW requirements to run a node = more decentralization, security

### Scaling

- Blockchain trilema
- Heats up after major periods of congestion, results in high gas fees
    - Causes 2017 (ICOs, crypto kitties) and today (defi, yield farming)
- TX Street - network congestion
- Taproot / soft forks / 
    - Privacy -> data compression/ommision -> scaling

### Layer 1/2

- Scale base layer 1 or offloading to another layer (off chain)
    - OSI model
    - layer 2 anchors its state into layer 1
- ETH Layer 2 Ecosystem
    - ETH 1 layer 1 = 15 tx/sec, layer 2 = 2-4k, ETH2 (w/ sharding) will still need layer 2 to handle 100k-million tx

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
Why scale? We're creating an entirely new, decentralized internet
- WWW != internet
- History - 1 (read), 2 (read-write), 3 (read-write-execute)
- Web3: Semantic Web - AI, 3d graphics, ubiquity, IOT
- TCP/IP, HTTP (not secure) - ipv4 vs ipv6; no payment layer of original internet
    - Fat protocol (TCP doesn't capture value, rather it's the apps built on top of it)

### P2P Messaging
- Status
- Deplatforming, deep fakes
- decoupling username from physical persona

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
    - Risk - bugs in smart contracts, protocol changes, is it really decentralized (admin key, on chain goverance), systemic risk (cascade of liquidation, flash loans, arbitrage), network fees/congestion, cutting edge/unknown issues in nascent industry

- new financial system, open to everyone, no banks
- relies heavily on cryptography and smart contracts
- developed on Ethereum, Solidity, lots of devs

### Lending/borrowing

1. Dex
    - don't have to give up custody of the coins
    - liquidity pool (tokens locked in a smart contract)
        - Provider sets price of exchange pair, if price diverges creates arbitrage op, ratio of tokens dictates price
        - Provider receives a certain type of LP token, burn tokens to get back original tokens and receive fees
            - price adjustment determinist algorithm
        - larger pools mean less price impact on large trades, thus less slippage
        
    - Order books
        - buy/seller come together and place orders
        - market makers provide liquitity as buyer/seller try to converge on price
        - difficult to reproduce in defi model due to reliance on market makers, which can make an exchange illiquid
            - also trouble with tx speed and block time, plus gas fees for MM to update orders, must be Layer 2
2. Lending and borrowing
- Compound, MakerDAO
    - algorithmic, autonmous interest rate protocol
    - supply assets and make interest or use as collateral
    - collateralized debt position, over-collateralized
    - margin trading: use borrowed funds to increase a position in a certain asset
3. Stable coins
    - peg to USD without having to use dollars
    - non-algorithmic stable coins (like USDC), company holds equivalent of USD (centralized, can be censored)

4. More
    Derivatives
        - derive value from performance of underlying asset
        - wrapped tokens
    Prediction Markets
    Insurance
        - protection against smart contract failures
    Oracles
        - bring in outside info
        - Chainlink
    Yield Farming

=========================================

## Environment
- 51st anniversary Earth Day
- Green Team, article
- skeptical of those using hyperbole and sentionalism

Proof of Work
Historical background
    - Promethean
    - Humble origins, cypher punks, bootstrapped from 0 to Trillion
    - beset on all sides, Crying wolf

* Data Driven Analysis
    - data can't speak for itself
    * Areas of agreement
        - empirically/theoretically consume energy in proportion to the value of the coin
        - energy use is non-rivalrous
        - BTC network does not care about geographic location
        - lower bound and upper bound of data aggregation
            - incorporates mining hardware used, presumed energy source relative to the miner's geographic location, and much more.
            - hyper-transparency of the Bitcoin network's metrics
    * Transactional volume
        - Bitcoin only can handle about 350,000 transactions a day and so it would require 14x the world's total electricity just to process the 1 billion credit card transactions that take place every day
            - blocks, not tx
            - 1 tx can represent many things
        - U.S. Markets are walled gardens with inconsistent access to resources among participants and are open 253 days per year for 6.5 hours a day, which equals 1,644 trading hours. Crypto markets, however, are open 365/24/7, which equals 8,760 trading hours. In other words, generating bitcoin transactions are not only permissionless (i.e., open to everyone with an internet connection) but are available approximately 5x that of traditional brokerage.
        <!-- - The "Bitcoin is a battery" argument is interesting, though contested. Energy producers themselves can plug in mining equipment, and store their excess power as bitcoin, which is conceivably analogous to, for example, aluminum smelting in Iceland as an "energy export" making use of stranded and abundant renewable energy resources. Those who contest this analogy tend to dispute the arguments supporting bitcoin as a store of value. -->
    * Payment vs Settlement
        - Explain
        - Conclude: The Bitcoin network now transfers $137,000 per second around the world without requiring a bank, government, or third party. Bitcoin transfers are not like Visa or PayPal, that only shift around a few numbers on their database. This is final settlement, with no liablities or credit. 
    * China
        - Bitcoin annually consumes approximately 135.59 TWh of electrcity with total carbon dioxide emissions not exceeding 58 million tons of CO2, or roughly 0.17% of the world’s total emissions. At least 40% is believed to have originated from renewable sources, with an estimated 65% of BTC mining occuring within China.
            - hyper-transparency of the Bitcoin network's metrics
            - Chinese mining pools do not always reflect the geographic diversity of its participants
        - e-Waste created by next generation ASICs being introduced (and out-dating older hardware) is another dimension to this conversation worth considering
        <!-- - U.S. electrical grid is (for the most part) interconnected in such a way so that power can be re-distributed across state lines as necessary or practical. However, this is often not the case in China. Rather, it is a country comprised of 1000s of energy plants supporting their immediate (often lower income) surroundings, which is to say that unused power is equivalent to wasted power (so-called "stranded energy"). Since the physical location of mining centers is not important to the functioning of the Bitcoin network, miner operations in China frequently make use of these plants due to the economic incentives (cheap and abundant electricity) -->
* Normative Psychology
    - Normative behavior or thinking is the phenomenon in human societies of designating some actions or outcomes as good or desirable or permissible and others as bad or undesirable or impermissible. Naturally, this line of thought leads to ends-justify-the-means arguments, both white and green washing of events or facts, and what-about-isms.
    - Bitcoin is consuming more energy than ever, irrespective of whether that energy comes from renewable or stranded sources. As the price rises so too does the electricity consumption. If you don't believe Bitcoin is useful, you're inclined to believe all the energy it uses is a waste. Whether entity "X" has an entitlement to consume any of the world's resources is effectively a rhetorical question with an answer that is somewhat irrebuttable. If you fundamentally contest the validity or relevance of a network, you will naturally consider its energy usage illegitimate.
    - An interesting counter-narrative here is that PoW incentivizes more power consumption as the aggregate crypto market capitalization increases. The price of bitcoin goes up, so more people mine. The same could not be said for hanging Christmas lights. However, it could for example be argued against gold mining or, more broadly, against meat consumption, both of which have a tremendous detrimental impact on the environment.
    * Politics
        - One's response here will vary radically depending on national identity, intellectual honesty, economic incentives, access to traditional financial resources or stable sovereign currencies, and much more.
        - Inflation
            - Turkey - 500% spike in bitcoin searches as Lira dropped 14%
        - XinJiang
    - Sources
    - Solutions: Is crypto accelerating the transition to renewable energy

## China

* To Control
    - What does it mean to have control in a decentralized environment
        - PoW vs PoS
    - Incentives for attack -> MAD
        - Very game theoretical, if not hypothetical
    - What is implied here? What is meant by "control"?
        - Can you make money doing it? Leverage as blackmail?
            - Very expensive, undercut value of network
        - Concerned about 51% attacks and double spends
            - Delegitimize? e-Yuan
            - Hard forks, render attacker equipment obsolete
 
- Mining
    - Miners do not control the network
        - Miners + Devs + Nodes + Wallets + Exchanges + increasingly wall st/institutions
        - non-block producing nodes
        - Segwit, block size wars
    - Distinction between citizens vs PRC
        - Seizure of private property
        - Mining pools
        - Ban on mining - Difficulty adjusts
    - 65% of mining power
        - decreasing each quarter
        - 60%, of the mining machines sold (sic) in the past two quarters or so have been outside of China
- Semi conductors
    - Biden Chips Shortage Summit
    - TSMC (Taiwan) - tiered purchasing priority (bitcoin mining companies are not Tier 1)
        - mining companies as customers are cyclical and account for 1% of revenues [WSJ](https://www.wsj.com/articles/bitcoin-and-chip-makers-are-caught-in-a-bad-romance-11615536301)
    - Nvidia tweaking graphics cards
    - shortage driven by skyrocketing demand for consumer electronics and cloud during Covid
- Firewall attack - network level attack (not hardware level)
    - nodes need to be able to communicate with one another to achieve consensus
    - put up firewall but continue to allow mining
    - Block port 8333; Devs do port randomizer; China does deep packet inspection; Embed it within SSH or HTTPS - back and forth
    - "China" chain periodically attempts to sync with "rest of world" chain, causing conflicts
        - chain reorg

## Quantum

- not just a question of quantum, but how many Qbits we have (need more than what we have)
- still a long way off from this being a legitimate threat
    - bits - 1 or zero
    - qubits - 1, 0, or combination of two 
        - information encoded on photons, measuring the spin of the particles
        - need about 4000 qubits to crack bitcoin, currently at 50

<!-- - quantum key distribution (uses quantum physics)
    - measuring the spin of particles (up or down)
    - don't know the spin, have to guess, then receive orientation (through unencrypted channel)
        - intercepting changes spins, no way of knowing if this happens
    - quantum mechanics: impossible to copy an arbitrary state without destroying it (no cloning theorum)

- currently public key cryptography
    - key exchanges - Diffie Helman
    - RSA and prime numbers
    - use public key to encypt message, takes time to break -->

- Change algorithms from ECDSA and SHA256
    - different problems for each (reversing a hash vs. shortcutting an elliptic curve)
    - one year warning before hard fork, move your coins!
        - But can't change them on wallets with lost keys/Satoshi's coins
            - maybe burn these coins?
        - Incidentally, with Satoshi, never spent coins he mined, thus no digital signature (ECDSA), only an address (double hash), quantum doesn't necessarily impact SHA256 the same
            - Another reason to not re-use addresses

- Coventry
    - background
    - nation state or research/edu facility
    - secret weapon, don't just use it right away
    - Works on everything else, not just bitcoin

## Wall Street
- Coinbase IPO - 86B valuation

* Concerns
    - volatility risk (historical) and implied volatility
    - options pricing, futures market, rehypothecation
        - debt based type of thinking
    - custody
    - non-correlated asset (diversification) - near zero with S&P, also with gold
        - negative correlation with dollar = hedge on inflation
- How to regulate a decentralized network
    - Edges, on/off ramps into dollars, taxes, who can hold it and how
    - How is the asset class portrayed

* Corporate Balance Sheets
    - Tesla
    https://bitcointreasuries.org/
    - MicroStrategy playbook
    - PayPal

* Financial Institutions
    - Morgan Stanley, GM Sachs
        - acquring stake in exchanges, publishing reports, btc exposure in mutual funds, filings with SEC to purchase/custody btc, offerings to private wealth clients
    - JPMorgan (called BTC a fraud, now has $130k price target)
    - Crypto market 0 to 1T in about a decade years, hit 2T three months later
        - Inflation
    - 3 BTC ETFs on Toronto stock exchange
        - help by Gemini, insured
    - Half dozen US companies file with SEC for ETF
        - Fidelity https://www.sec.gov/Archives/edgar/data/1852317/000119312521092598/d133565ds1.htm
        - Goldman (ETF that can have "exposure" to bitcoin) - https://www.sec.gov/Archives/edgar/data/0000886982/000156459021014786/gs-424b2.htm

* Regulatory Bodies
    - Gary Gensler, MIT professor, understands BTC
        - concerns: ETFs being rejected by the SEC citing manipulation and market size/lack of liquidity as concerns; clarity is still needed “at the federal, fiscal, tax and other regulatory levels”; mandate to protect investors
        - forks, changes to protocol (added privacy)
        - Ripple vs SEC
    - FinCEN new acting director Michael Mosier (form Chainalysis CTO)
        - Chainalysis: In 2019, illicit activity represented 1.1% of all cryptocurrency transaction volume or roughly $11.4 billion worth of transfers. In 2020, the illicit share of all cryptocurrency activity fell to just 0.34%, or $10.0 billion in transaction volume. One reason the percentage of illicit activity fell is because overall economic activity nearly tripled between 2019 and 2020.
            <!-- - Crypto crime is starting to look more like white collar crime. 
            - Money laundering is the key to crypto crime. 
            - Scams are the biggest threat in crypto crime -->
    - Michael Morrel
        - "Boon for Surveillance" as a forensic tool, and "concern over BTC use for illicit finance is signifcantly overstated"
        - “We need to make sure that the conventional wisdom that is wrong about the illicit use of Bitcoin doesn’t hold us back from pushing forward the technological changes that are going to allow us to keep pace with China.”

## CBDCs and Regulation

A central bank digital currency (CBDC) uses an electronic record or digital token to represent the virtual form of a fiat currency of a particular nation (or region). A CBDC is centralized; it is issued and regulated by the  monetary authority of the country.
- store of value, means of exchange, unit of account

- Bretton Woods II
    - historical background - IMF and World Bank
        - 90% of foreign exchange tx involve dollars; 60% of global reserves are held in dollar denominated assets
            - https://data.imf.org/?sk=E6A5F467-C14B-4AA8-9F6D-5A09EC4E62A4
        <!-- - Cross-border deals, even for deals not involving the U.S. itself. For instance, 86% of India’s imports are paid for in dollars, while only 5% of them actually originate in the U.S.
            - https://www.eximbankindia.in/blog/blog-content.aspx?BlogID=9&BlogTitle=Dollar%20Dominance%20in%20Trade:%20Facts%20and%20Implications -->
    - Davos, global reset, debt jubilees
- Cross-border settlement
    - “One aspect to CBDCs is helping streamline cross-border payments to create frictionless borderless trade, but the second major benefit of widespread adoption is geopolitical and means greater competition for global trade and thus greater sovereignty over the global economy.”
    - Competition with other central banks and private sector (and crypto?)

- BIS
    - Agustín Carstens, General Manager, Bank of International Settlements
    - central bank will have absolute control on the rules + regs that will determine the use + the technology to enforce that
    - consolidation of power by the sovereign

- Digital Yuan
    - Not necessarily replace role of dollar, but rather weaken power of American sanctions
        - compete with SWIFT
    - Smart cities; 2022 Olympics
    - Programable money: Beijing has tested expiration dates to encourages users to spend quickly, for jumpstarting the economy
    - "controlled anonymity"
    - surveillance aparatus, money as a system of control
    - Proposing standards to BIS
        - “Governance — How is its value determined and maintained? What is its monetary policy? How is it backed? What KYC/AML rules apply? Who supervises and regulates it? Is it a private or public venture? Who ensures privacy, consumer protection? Solving them is a major task in and of itself.”
- China-HK-Thailand-UAE
        - Coalitions/cross-borders: https://cointelegraph.com/news/major-asian-banks-unite-to-form-multiple-cbdc-pact-on-blockchain
            - China-HK-Thailan-UAE
        - Eastern Caribbean - https://cointelegraph.com/news/eastern-caribbean-central-bank-s-dcash-digital-currency-goes-live
- Digital Euro
    - public consultation https://www.ecb.europa.eu/paym/digital_euro/html/index.en.html
    - more retail focused, not replace cash
- Digital Dollar
    - Powell: more concerned with getting it right, than being first
        - Need for Digital Dollar Is an Issue for Congress, Public
    - https://www.digitaldollarproject.org/
    - Privacy as a central concern
    - Role of private banks diminished?
    - Dollar as reserve currency

## Open Source Projects
- Passion to get regulatory environment correct

=================