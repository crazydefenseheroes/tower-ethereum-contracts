TOWER token is based on `ERC20WithOperators`, you can find the audit report from the link below.

The contract source code is nearly identical to the REVV contract source code

[Link to the REVV Audit Report](https://github.com/animocabrands/f1dt-ethereum-contracts/blob/master/contracts/token/ERC20/Animoca_REVV_Token_CertiK_Report_07_22_2020.pdf)

# TOWER - Crazy Defense Heroes Governance and Utility Token

Crazy Kings (CK) and its sequel Crazy Defense Heroes (CDH) are among Animoca Brands most venerable and respected mobile games
They are successful tower defense games boasting millions of downloads, solid financial results and a number of blockchain-friendly features, including the deck building of a collectible card game and an RPG character/equipment system.

We are introducing a new fungible token TOWER for CK and CDH that will have a governance as well as various utility for the entire Crazy Kings franchise and will pave the way for a new blockchain game

Governance: owners of the tokens will be able to fully participate in the governance of the Crazy Kings franchise, including submitting proposals for the games’ direction and voting on those proposals; these are important steps in giving players a true and effective voice in the roadmap of the games

Crypto economy: owners of the tokens will be able to trade them, thus buying and selling the right to influence the development of the game franchise, and even participate in distributed finance (DeFi) initiatives such as staking (details to be determined)

Currency: the token will be accepted as currency within a PC based blockchain native game that will be the newest addition to the Crazy Kings franchise

Tournament entry fees: tournaments are special events that will challenge the skill, strategy, and game assets of players

Tournament prizes: tokens will be distributed as prizes to the victors of competitive multiplayer tournaments, which is a significant step toward full-fledged play-to-earn mechanics.

## The Anatomy of the TOWER ERC-20

The TOWER token is a fungible token that exists on the Ethereum blockchain. A fungible token is an asset that is interchangeable with tokens of the same type - so one TOWER token always has the same value as any other single TOWER token.

TOWER is a standard Ethereum ERC-20 token with commonly used interfaces. It also contains a whitelisted operators feature which enables meta-transactions without requiring pre-approval


TOWER implements ERC165 introspection standard. The following ERC165 interfaces are supported:

| Interface | Specification | ERC165 Interface Id(s) |
| :----     | :---          | :---                   |
| ERC-165   | https://eips.ethereum.org/EIPS/eip-165 | `0x01ffc9a7` |
| ERC-20    | https://eips.ethereum.org/EIPS/eip-20 | `0x36372b07` |
| ERC-20 Detailed   | https://github.com/animocabrands/ethereum-contracts-erc20_base/blob/v3.0.0a/contracts/token/ERC20/IERC20Detailed.sol | `0xa219a025` name():`0x06fdde03` symbol(): `0x95d89b41` decimals(): `0x313ce567` |
| ERC-20 Allowance   | https://github.com/animocabrands/ethereum-contracts-erc20_base/blob/v3.0.0a/contracts/token/ERC20/IERC20Allowance.sol | `0x9d075186` |


### Core Token Feature

TOWER supports the standard features of an ERC-20 token, as described by the interfaces “ERC-20” and “ERC-20 Detailed” in the table above. The “ERC-20 Allowance” brings some usability for managing allowances. 

### Whitelisted Operators

Using an ERC-20 to make a payment through a smart contract requires an initial additional user transaction to explicitly give the contract some allowance of this ERC-20. 

The TOWER token smart contract can whitelist other contracts in its ecosystem, allowing them to implicitly manage tokens for users without the allowance step, enhancing the base user experience.

To manage adding and removal of whitelisted operators, the TOWER contract has an owner account. Ownership is transferable and renounceable. Animoca Brands maintains ownership of the TOWER owner account and will apply changes of whitelisted operators from time to time.

It is essential that only trusted contracts obtain the status of whitelisted operators. Animoca Brands will determine which contracts within the ecosystem are suitable for being used as TOWER whitelisted operators. There are two main types of ecosystem whitelisted operators: 
- Purchase contracts which support payments with TOWER.
- Contracts with TOWER-based meta-transactions which allow the users to pay the transaction gas with TOWER instead of ETH. 