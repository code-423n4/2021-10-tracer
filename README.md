# ✨ So you want to sponsor a contest

This `README.md` contains a set of checklists for our contest collaboration.

Your contest will use two repos: 
- **a _contest_ repo** (this one), which is used for scoping your contest and for providing information to contestants (wardens)
- **a _findings_ repo**, where issues are submitted. 

Ultimately, when we launch the contest, this contest repo will be made public and will contain the smart contracts to be reviewed and all the information needed for contest participants. The findings repo will be made public after the contest is over and your team has mitigated the identified issues.

Some of the checklists in this doc are for **C4 (🐺)** and some of them are for **you as the contest sponsor (⭐️)**.

---

# Contest setup

## 🐺 C4: Set up repos
- [X] Create a new private repo named `YYYY-MM-sponsorname` using this repo as a template.
- [ ] Get GitHub handles from sponsor.
- [ ] Add sponsor to this private repo with 'maintain' level access.
- [ ] Send the sponsor contact the url for this repo to follow the instructions below and add contracts here. 
- [ ] Delete this checklist and wait for sponsor to complete their checklist.

## ⭐️ Sponsor: Provide contest details

Under "SPONSORS ADD INFO HERE" heading below, include the following:

- [ ] Name of each contract and:
  - [ ] lines of code in each
  - [ ] external contracts called in each
  - [ ] libraries used in each
- [ ] Describe any novel or unique curve logic or mathematical models implemented in the contracts
- [ ] Does the token conform to the ERC-20 standard? In what specific ways does it differ?
- [ ] Describe anything else that adds any special logic that makes your approach unique
- [ ] Identify any areas of specific concern in reviewing the code
- [ ] Add all of the code to this repo that you want reviewed
- [ ] Create a PR to this repo with the above changes.

---

# ⭐️ Sponsor: Provide marketing details

- [ ] Your logo (URL or add file to this repo - SVG or other vector format preferred)
- [ ] Your primary Twitter handle
- [ ] Any other Twitter handles we can/should tag in (e.g. organizers' personal accounts, etc.)
- [ ] Your Discord URI
- [ ] Your website
- [ ] Optional: Do you have any quirks, recurring themes, iconic tweets, community "secret handshake" stuff we could work in? How do your people recognize each other, for example? 
- [ ] Optional: your logo in Discord emoji format

---

# Contest prep

## 🐺 C4: Contest prep
- [X] Rename this repo to reflect contest date (if applicable)
- [X] Rename contest H1 below
- [X] Add link to report form in contest details below
- [X] Update pot sizes
- [X] Fill in start and end times in contest bullets below.
- [ ] Move any relevant information in "contest scope information" above to the bottom of this readme.
- [ ] Add matching info to the [code423n4.com public contest data here](https://github.com/code-423n4/code423n4.com/blob/main/_data/contests/contests.csv))
- [ ] Delete this checklist.

## ⭐️ Sponsor: Contest prep
- [ ] Make sure your code is thoroughly commented using the [NatSpec format](https://docs.soliditylang.org/en/v0.5.10/natspec-format.html#natspec-format).
- [ ] Modify the bottom of this `README.md` file to describe how your code is supposed to work with links to any relevent documentation and any other criteria/details that the C4 Wardens should keep in mind when reviewing. ([Here's a well-constructed example.](https://github.com/code-423n4/2021-06-gro/blob/main/README.md))
- [ ] Please have final versions of contracts and documentation added/updated in this repo **no less than 8 hours prior to contest start time.**
- [ ] Ensure that you have access to the _findings_ repo where issues will be submitted.
- [ ] Promote the contest on Twitter (optional: tag in relevant protocols, etc.)
- [ ] Share it with your own communities (blog, Discord, Telegram, email newsletters, etc.)
- [ ] Optional: pre-record a high-level overview of your protocol (not just specific smart contract functions). This saves wardens a lot of time wading through documentation.
- [ ] Designate someone (or a team of people) to monitor DMs & questions in the C4 Discord (**#questions** channel) daily (Note: please *don't* discuss issues submitted by wardens in an open channel, as this could give hints to other wardens.)
- [ ] Delete this checklist and all text above the line below when you're ready.

---

# Tracer contest details
- $28,500 USDC (+ $19,000 in tokens) main award pot
- $1,500 USDC (+ $1,000 in tokens) gas optimization award pot
- Join [C4 Discord](https://discord.gg/EY5dvm3evD) to register
- Submit findings [using the C4 form](https://code423n4.com/2021-10-tracer-contest/submit)
- [Read our guidelines for more details](https://docs.code4rena.com/roles/wardens)
- Starts October 7, 2021 00:00 UTC
- Ends October 13, 2021 23:59 UTC

Contracts can be found [here (note: commit 646360b)](https://github.com/tracer-protocol/perpetual-pools-contracts/tree/646360b0549962352fe0c3f5b214ff8b5f73ba51).

# Tracer Perpetual Pools
Project base generated with the Typescript Solidity Dev Starter Kit. See [Blog Post](https://medium.com/@rahulsethuram/the-new-solidity-dev-stack-buidler-ethers-waffle-typescript-tutorial-f07917de48ae) for more details

## C4 Audit Known Issues
In `PoolCommitter::commit`, `shadowPools[_commitType]` is passed in as a parameter to this function, but that's already been incremented yet the tokens haven't yet been burnt.

[Perpetual Pools - Documentation](https://tracerdao.notion.site/Perpetual-Pools-Documentation-ee935f325a9a448d9ed44e333dff0e74)

## Contract Addresses

These are the current contracts that are being used on Arbitrum One.

| Contract | Pool | Address |
| -------- | -------- | ------- |
| `OracleWrapper` for the BTC/USD oracle | N/A | [0xE973E6400B44fd20fc4752c03D112274A1374bA0](https://arbiscan.io/address/0xE973E6400B44fd20fc4752c03D112274A1374bA0) |
| `OracleWrapper` for the ETH/USD oracle | N/A | [0xeceaea7e0408606714b2559ac9b1d3d51a327afe](https://arbiscan.io/address/0xeceaea7e0408606714b2559ac9b1d3d51a327afe) |
| `PoolFactory` | N/A | [0x98C58c1cEb01E198F8356763d5CbA8EB7b11e4E2](https://arbiscan.io/address/0x98C58c1cEb01E198F8356763d5CbA8EB7b11e4E2) |
| `PoolKeeper` | N/A | [0x759E817F0C40B11C775d1071d466B5ff5c6ce28e](https://arbiscan.io/address/0x759E817F0C40B11C775d1071d466B5ff5c6ce28e) |
| `LeveragedPool` | 3p BTC/USD | [0x70988060e1FD9bbD795CA097A09eA1539896Ff5D](https://arbiscan.io/address/0x70988060e1FD9bbD795CA097A09eA1539896Ff5D) |
| `PoolCommitter` | 3p BTC/USD | [0xFDE5D7B7596AF6aC5df7C56d76E14518A9F578dF](https://arbiscan.io/address/0xFDE5D7B7596AF6aC5df7C56d76E14518A9F578dF) |
| `LeveragedPool` | 1p BTC/USD | [0x146808f54DB24Be2902CA9f595AD8f27f56B2E76](https://arbiscan.io/address/0x146808f54DB24Be2902CA9f595AD8f27f56B2E76) |
| `PoolCommitter` | 1p BTC/USD | [0x539Bf88D729B65F8eC25896cFc7a5f44bbf1816b](https://arbiscan.io/address/0x539Bf88D729B65F8eC25896cFc7a5f44bbf1816b) |
| `LeveragedPool` | 3p ETH/USD | [0x54114e9e1eEf979070091186D7102805819e916B](https://arbiscan.io/address/0x54114e9e1eEf979070091186D7102805819e916B) |
| `PoolCommitter` | 3p ETH/USD | [0x759E817F0C40B11C775d1071d466B5ff5c6ce28e](https://arbiscan.io/address/0x759E817F0C40B11C775d1071d466B5ff5c6ce28e) |
| `LeveragedPool` | 1p ETH/USD | [0x3A52aD74006D927e3471746D4EAC73c9366974Ee](https://arbiscan.io/address/0x3A52aD74006D927e3471746D4EAC73c9366974Ee) |
| `PoolCommitter` | 1p ETH/USD | [0x047Cd47925C2390ce26dDeB302b8b165d246d450](https://arbiscan.io/address/0x047Cd47925C2390ce26dDeB302b8b165d246d450) |

## Frontend Notes
### Calculating ABDKMathQuad values
The `PoolSwapLibrary` contains several methods for generating, converting, and using the raw ratio values. These can be used in the frontend to estimate the result of a transaction. It is vital when estimating the result of a transaction that the shadow pool amount for the commit type's opposite is included in the token total supply.

## Environment variables
The environment variables used in this project are documented in the `example.env` file at the root of the project. To configure, create a copy of `example.env`, rename to `.env`, and replace the placeholders with the correct values. 

## Using this Project

Install the dependencies with `yarn`. 
Build everything with `yarn compile`. 
Run the tests with `yarn test`.

## Available Functionality

### Build Contracts and Generate Typechain Typeings
You'll need to run this before running tests if typescript throws an error about not finding the typechain artifacts.

`yarn refresh`

### Run Slither for static analysis report
If you have `slither` installed and on your PATH, you can run `npm run slither` to get a report on the current codebase.

 
### Deploy to Ethereum

Create/modify network config in `hardhat.config.ts` and add API key and private key, then run:

`npx hardhat run --network rinkeby scripts/deploy.ts`
**Note:** As of this commit, deploys are out of sync with the current contract set-up and therefore will not work.

### Verify on Etherscan

Using the [hardhat-etherscan plugin](https://hardhat.org/plugins/nomiclabs-hardhat-etherscan.html), add Etherscan API key to `hardhat.config.ts`, then run:

`npx hardhat verify --network rinkeby <DEPLOYED ADDRESS>`

PRs and feedback welcome!

## Frequently Asked Questions

**How are pool keepers to be chosen? How many keepers are there?** 

The Pool Keeper is simply a contract that enforces the correct keeper behaviour. Anyone may be a keeper by calling the keeper function on that contract with a pool that is valid for upkeep. We will initially be adding wrappers for Chainlink keepers as well as having custom keepers.

**The leveraged pool fee is represented as a `bytes16` value. Why is this chosen over something like `uint`? What denomination does this represent?**

The leveraged pool fee is a `bytes16` value simply due to the maths library used. We often represent values in WAD values (popularised by the Maker DAO team). WAD values are the integer value multiplied by 10^18 (e.g. `1 = 1*10^18`). The maths library we currently use represents values in IEEE quad precision numbers and uses bytes as way of storing this. A good primer on the above can be found [here](https://medium.com/coinmonks/math-in-solidity-part-1-numbers-384c8377f26d) and WAD / RAY maths is introduced [here](https://docs.makerdao.com/other-documentation/system-glossary).

**How many different type of tests are there? There are unit tests in the test suite. Are there also end to end tests?**

Most tests are unit tests. There is a single E2E test in `e2e.spec.ts` right now. We plan to add more.

**Whats the `deployments/kovan` folder for? They seem to be different from the ABIs I get from `artifacts` folder when I compile.**

We use a plugin for hardhat called hardhat deploy that helps with deployment. They recommend you commit the `deployments` folder to have consistent data across deploys. The deploys you find there will be deploys that have been run from old versions of the contract, hence the ABI difference.
