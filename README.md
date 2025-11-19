# Filecoin Onchain Cloud <> ENS

[![Publish decentralized content with ENS and Filecoin
Onchain Cloud](slides.png)](https://embed.figma.com/slides/a90Tn6ZLzG4RUWKYXvRAZR/Filecoin-%3C%3E-ENS-at-Code-n--Corgi---DevConnect-2025?node-id=3-7107&embed-host=share)

## Simplest happy path
1. Create a HTML file called `index.html`. To keep things simple, everything is inline.
2. Upload it to https://pin.filecoincloud.eth.limo/
3. Set the content hash field: https://app.ens.domains/filecoin.ses.eth?tab=records 

## Using omnipin.eth.limo (WIP)
1. `npm i -g omnipin`
2. Set .env
```
OMNIPIN_FILECOIN_TOKEN=[hidden]
OMNIPIN_FILECOIN_SP_URL=https://main.ezpdpz.net
OMNIPIN_FILECOIN_SP_ADDRESS=0x32c90c26bCA6eD3945De9b29BA4e19D38314D618
```
3. `source .env`
4. `omnipin deploy --providers Filecoin`

## Using Synapse SDK and ENSjs (WIP)
- https://docs.filecoin.cloud/getting-started/#finding-service-providers 
- https://github.com/ensdomains/ensjs/blob/main/docs/wallet/function.setContentHashRecord.md 