
# SYMM IO contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Q&A

### Q: On what chains are the smart contracts going to be deployed?
BNB, Arbitrum, Polygon, Base, opBNB, zkEVM, Optimism
___

### Q: Which ERC20 tokens do you expect will interact with the smart contracts? 
USDT, USDC
___

### Q: Which ERC721 tokens do you expect will interact with the smart contracts? 
None
___

### Q: Do you plan to support ERC1155?
None
___

### Q: Which ERC777 tokens do you expect will interact with the smart contracts? 
None
___

### Q: Are there any FEE-ON-TRANSFER tokens interacting with the smart contracts?

None
___

### Q: Are there any REBASING tokens interacting with the smart contracts?

None
___

### Q: Are the admins of the protocols your contracts integrate with (if any) TRUSTED or RESTRICTED?
Trusted
___

### Q: Is the admin/owner of the protocol/contracts TRUSTED or RESTRICTED?
Trusted
___

### Q: Are there any additional protocol roles? If yes, please explain in detail:
DEPOSITOR_ROLE: Responsible for transferring users' deposited funds into the Symmio contract.
BALANCER_ROLE: Tasked with processing users' withdrawal requests and providing necessary funds in the contract, if required.
SETTER_ROLE: In charge of setting contract parameters, including depositLimit, solverAddress, and symmioAddress.
PAUSER_ROLE: Authorized to pause the main functions of the contract.
UNPAUSER_ROLE: Authorized to unpause the main functions of the contract.

These are all trusted roles
___

### Q: Is the code/contract expected to comply with any EIPs? Are there specific assumptions around adhering to those EIPs that Watsons should be aware of?
EIP-1967: Proxy Storage Slots (Upgradable contracts)
___

### Q: Please list any known issues/acceptable risks that should not result in a valid finding.
None
___

### Q: Please provide links to previous audits (if any).
None
___

### Q: Are there any off-chain mechanisms or off-chain procedures for the protocol (keeper bots, input validation expectations, etc)?
None
___

### Q: In case of external protocol integrations, are the risks of external contracts pausing or executing an emergency withdrawal acceptable? If not, Watsons will submit issues related to these situations that can harm your protocol's functionality.
Besides the stable coin contracts, this contract interacts with the Symmio contract and calls one of its methods. If that method is paused in Symmio, the 'depositToSymmio' method will be reverted
___

### Q: Do you expect to use any of the following tokens with non-standard behaviour with the smart contracts?
No
___

### Q: Add links to relevant protocol resources

___



# Audit scope


[solver-vaults @ 4bdebbecb66e29ac18e5a5c9eda42e4cb44cdd65](https://github.com/SYMM-IO/solver-vaults/tree/4bdebbecb66e29ac18e5a5c9eda42e4cb44cdd65)
- [solver-vaults/contracts/SolverVaultToken.sol](solver-vaults/contracts/SolverVaultToken.sol)
- [solver-vaults/contracts/SolverVaults.sol](solver-vaults/contracts/SolverVaults.sol)

