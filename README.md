# Filecoin Onchain Cloud <> ENS

[![Publish decentralized content with ENS and Filecoin
Onchain Cloud](slides.png)](https://embed.figma.com/slides/a90Tn6ZLzG4RUWKYXvRAZR/Filecoin-%3C%3E-ENS-at-Code-n--Corgi---DevConnect-2025?node-id=3-7107&embed-host=share)

## Simplest happy path
1. Create a HTML file called `index.html`. To keep things simple, everything is inline.
2. Upload it to https://pin.filecoincloud.eth.limo/
3. Set the content hash field: https://app.ens.domains/filecoin.ses.eth?tab=records 

## Using omnipin.eth.limo

_Note:_ `0xDD55F1be37A22f2B535911CbCF7FbdBfD0a5d39e` is the example address I used. Create a new address/private key and use it accordingly

1. `npm i -g omnipin`
2. Set .env
```
export OMNIPIN_FILECOIN_TOKEN=[hidden]
export OMNIPIN_PK=[hidden, but same as above]
export OMNIPIN_FILECOIN_SP_URL=https://main.ezpdpz.net
export OMNIPIN_FILECOIN_SP_ADDRESS=0xDD55F1be37A22f2B535911CbCF7FbdBfD0a5d39e
```
3. `source .env`
4. Create `/dist` folder and move the `index.html` file there
5. `omnipin deploy --providers Filecoin`
6. Add `0xDD55F1be37A22f2B535911CbCF7FbdBfD0a5d39e` as a manager to any ENS name. For example: [filecoin.ses.eth](https://app.ens.domains/filecoin.ses.eth?tab=ownership)
7. Redeploy and update contentHash automatically: `omnipin deploy --providers Filecoin --ens filecoin.ses.eth`

## Using Synapse SDK and ENSjs (WIP)
- https://docs.filecoin.cloud/getting-started/#finding-service-providers 
- https://github.com/ensdomains/ensjs/blob/main/docs/wallet/function.setContentHashRecord.md 