TOWER token is base on `ERC20WithOperators`, you can find the audit report from the link below.

[Link to Audit Report](https://github.com/animocabrands/f1dt-ethereum-contracts/blob/master/contracts/token/ERC20/Animoca_REVV_Token_CertiK_Report_07_22_2020.pdf)


REVV implements ERC165 introspection standard. The following ERC165 interfaces are supported:

| Interface | Specification | ERC165 Interface Id(s) |
| :----     | :---          | :---                   |
| ERC-165   | https://eips.ethereum.org/EIPS/eip-165 | `0x01ffc9a7` |
| ERC-20    | https://eips.ethereum.org/EIPS/eip-20 | `0x36372b07` |
| ERC-20 Detailed   | https://github.com/animocabrands/ethereum-contracts-erc20_base/blob/v3.0.0a/contracts/token/ERC20/IERC20Detailed.sol | `0xa219a025` name():`0x06fdde03` symbol(): `0x95d89b41` decimals(): `0x313ce567` |
| ERC-20 Allowance   | https://github.com/animocabrands/ethereum-contracts-erc20_base/blob/v3.0.0a/contracts/token/ERC20/IERC20Allowance.sol | `0x9d075186` |


### Core Token Feature

REVV supports the standard features of an ERC-20 token, as described by the interfaces “ERC-20” and “ERC-20 Detailed” in the table above. The “ERC-20 Allowance” brings some usability for managing allowances. 

### Whitelisted Operators

Using an ERC-20 to make a payment through a smart contract requires an initial additional user transaction to explicitly give the contract some allowance of this ERC-20. 

The REVV token smart contract can whitelist other contracts in its ecosystem, allowing them to implicitly manage tokens for users without the allowance step, enhancing the base user experience.

To manage adding and removal of whitelisted operators, the REVV contract has an owner account. Ownership is transferable and renounceable. Animoca Brands maintains ownership of the REVV owner account and will apply changes of whitelisted operators from time to time.

It is essential that only trusted contracts obtain the status of whitelisted operators. Animoca Brands will determine which contracts within the ecosystem are suitable for being used as REVV whitelisted operators. There are two main types of ecosystem whitelisted operators: 
- Purchase contracts which support payments with REVV.
- Contracts with REVV-based meta-transactions which allow the users to pay the transaction gas with REVV instead of ETH. 