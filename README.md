# Guide on creating an open chat bot

- Check out the official docs and sdk on open chat bots [here](https://github.com/open-chat-labs/open-chat-bots?tab=readme-ov-file#open-chat-bots)

- Once you have an understanding of the bots. You can now proceed to run open chat locally which is the first step 

### Running open chat locally: 

N/B: Ensure you're using ``node >= 20.0.0`` and ``dfx >= dfx 0.25.1-beta.0`` 

1. Clone the main open chat repo: 
```bash
git clone https://github.com/open-chat-labs/open-chat 

cd open-chat
``` 

2. Start dfx and install necessary canisters (Open chat and NNS): 
```bash 
dfx start --clean --background 

./scripts/deploy-local.sh
``` 

3. Once the script executes succesfully, run the frontend: 
```bash 
cd frontend 

npm run dev 
``` 

<!-- la@Steves-MacBook dice % dfx identity new testbot_identity --storage-mode=plaintext 
Your seed phrase for identity 'testbot_identity': dwarf solve protect bronze sport neglect spice much saddle asset bread dentist argue occur demand page paddle twelve language join super profit armor story
This can be used to reconstruct your key in case of emergency, so write it down in a safe place.
Created identity: "testbot_identity".
la@Steves-MacBook dice % dfx identity export testbot_identity
-----BEGIN EC PRIVATE KEY-----
MHQCAQEEID5N3LzzjOs9kDMrFtYIESoYweFqBbKXLEG0r4xMhxCwoAcGBSuBBAAK
oUQDQgAEygRlx5tFVZpvsulHqC6ooFtVm0T10nN+4d1ySUPrMtyjpJyYwXPA937o
NXmVIjd10SdAYqyaL+b1Qb0Mc1wRoQ==
-----END EC PRIVATE KEY-----
la@Steves-MacBook dice %  -->


dfx identity new testbot_identity --storage-mode=plaintext 

dfx identity export testbot_identity

dfx --identity testbot_identity identity get-principal

principal is used to authenticate the bot and the jwt and off chain token - or the API key used to authorize the bot 

