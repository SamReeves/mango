# mango
#### A look into the Mango Markets takedown

Mango markets is a protocol on Solana that was exploited by an attacker (or a smart trader) for ~100M.  We will take a look at what the attack was, how it was executed, and some approaches to detecting and avoiding losing value to this type of mechanism.

## Usage Instructions

Jupyter notebook for active viewing, along with pip and venv.  To view passively, just navigate to the notebook in the github repo.

From the repo directory root:

    source venv/bin/activate
    pip install -r requirements.txt


Now, begin with part1.ipynb.  This is the initial report on the Mango Markets attack.  Parts 2 and 3 try to address risk mitigation from the perspective of protocol operators and investors.


## Data Sources

Mango Markets MNGO price data:
    https://coincodex.com/crypto/mango-markets/historical-data/

Interview with Avraham Eisenberg:
    https://www.youtube.com/watch?v=e-y4WmrndQ4

Mango Markets docs: 
    https://docs.mango.markets/

Solana docs: 
    https://docs.solana.com/history

List of large scale 2022 crypto hacks: 
    https://milkroad.com/hacks

Mango Markets Neodyme Security Audit: 
    https://1610690202-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MVID3wF97zSdsTruiIC%2Fuploads%2FNJ586BURL5wI6mPgIX05%2FMango%20Markets%20audit.pdf?alt=media&token=03d4956b-6f29-4371-8d6a-b2c432de7949

