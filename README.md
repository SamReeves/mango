# mango
A look into the Mango Markets takedown


Mango markets is a protocol on Solana that was exploited by an attacker (or a smart trader) for ~100M.  We will take a look at what the attack was, how it was executed, and some approaches to detecting and avoiding losing value to this type of mechanism.

## Some things you will need:

Jupyter notebook for active viewing, along with pip and venv.  To view passively, just navigate to the notebook in the github repo.

From the repo directory root:

    source venv/bin/activate
    pip install -r requirements.txt


# Part 1

* A brief report on attack (it requires understanding of the protocol, perps, oracles and the strategy used by the attacker)

This was not at all something that can be considered a hack.  Avi Eisenberg, the trader behind the liquidation, gives an extensive interview here https://www.youtube.com/watch?v=e-y4WmrndQ4

His team did not implement any exploits on the protocol, they did not coerce anybody to act on their behalf, and they did not engage in any form of cybersecurity gotcha.  They used the platform exactly as directed.

The acount that accepted the value that liquidated the platform was associated with Eisenberg's discord handle ponzishorter.eth, which, apart from being hilarious, is a big clue to what he calls a beneficial trading strategy.


# Part 2

* If we are building a risk management platform for protocols like Mango, how should the product look like? What should it do and what does it take to build?

From the perspective of the platform itself, blockchain forensics is probably the lowest hanging fruit.  By recognizing the difference between a mass market swing and a small collection of whales taking up all the liquidity in a pool, we can maybe pause the activity on a platform and find a way to block the addresses causing major disruptions.
# Part 3

* If we are building a risk management platform for institutonal investors investing in protocols like Mango, how should the product look like? What should it do and what does it take to build?

From the perspective of the investor, I would say that there are two parts to the strategy:

1. Group platforms together based on their similarity to classically established rules for banking and wealth management firms.

This may involve a checklist including things like separation among liquidity markets and lending operations or limits on leverage.  The risk categories could just be tags, however the inherent credit and market risk of each individual platform will play in heavily for any automated detection system.

2. Recognize when a market is being manipulated, and exit immediately.