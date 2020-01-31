
Install Aragon CLI
```bash
npm install --global @aragon/cli
```

Make sure you have cloned the fundraising repo (this repo) and also cloned the Aragon client repo.

```bash
mkdir aragon && cd aragon;
git clone https://github.com/aragon/aragon.git aragon-client
git clone https://github.com/AragonBlack/fundraising.git
```

In two separate terminal processes do the following:

Start the devchain.
```bash
npx aragon devchain
```

Start ipfs.
```bash
npx aragon ipfs start
```

From the Aragon Client directory
```bash
cd aragon-client
npm install
env ARAGON_APP_LOCATOR=fundraising npm run start:local

```

Publish Fundraising Apps from the Aragon Fundraising Monorepo directory
```bash
cd fundraising
npm install
npm run bootstrap
npm run publish
```

Deploy a test DAO
```bash
cd template/multisig
npm run deploy:dao:rpc
#  You'll get an address to a DAO
```

Start the fundraising frontend
```bash
cd ../../apps/aragon-fundraising/app
```
