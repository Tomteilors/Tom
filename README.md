# Base Learn — Solidity exercise contracts

Contracts completed for [Base Learn](https://docs.base.org/learn/welcome), the onchain Solidity course by Base.
Each exercise is deployed to Base Sepolia and submitted to the course contract to earn the matching Base Learn NFT badge.

Deployed and submitted in June 2024 via [Remix](https://remix.ethereum.org).
The solutions follow the reference implementations by [NelsonRodMar](https://github.com/NelsonRodMar); author tags in the source files are kept as-is.

## Contracts

| Exercise | File | What it covers |
|---|---|---|
| Basic Math | `contracts/BasicMath.sol` | Overflow/underflow-safe `adder` and `subtractor` returning an error flag |
| Control Structures | `contracts/ControlStructures.sol` | `fizzBuzz` and `doNotDisturb` with custom errors and `revert` |
| Storage | `contracts/EmployeeStorage.sol` | Storage packing of `uint16`/`uint32`/`uint256`, custom `TooManyShares` error |
| Arrays | `contracts/ArraysExercise.sol` | Dynamic arrays, `calldata` appends, filtering timestamps after Y2K |
| Mappings | `contracts/FavoriteRecords.sol` | Approved-records mapping, per-user favorites, custom `NotApproved` error |
| Structs | `contracts/GarageManager.sol` | `Car` struct, per-address garage, update and reset |
| Inheritance | `contracts/Employee.sol`, `Salaried.sol`, `Hourly.sol`, `Manager.sol`, `Salesperson.sol`, `EngineeringManager.sol`, `InheritanceSubmission.sol` | Abstract base, `virtual`/`override`, multiple inheritance |
| Imports | `contracts/ImportsExercise.sol`, `SillyStringUtils.sol` | Library import, `Haiku` struct, string concatenation |
| Error Triage | `contracts/ErrorTriageExercise.sol` | Fixing arithmetic and array-handling bugs |
| New Keyword | `contracts/AddressBook.sol`, `AddressBookFactory.sol` | Factory deploying `AddressBook` instances with `new`, `Ownable` pattern |
| Minimal Token | `contracts/UnburnableToken.sol` | Claim-once token with `safeTransfer` guard |
| ERC-20 Voting | `contracts/WeightedVoting.sol` | OpenZeppelin ERC-20 with issue creation, weighted votes, quorum |
| ERC-721 | `contracts/HaikuNFT.sol` | OpenZeppelin ERC-721 minting unique haikus and sharing them |

## Notes

- Compiler: Solidity `^0.8.17` (`Hourly.sol` is `^0.8.13`).
- OpenZeppelin contracts are resolved by Remix at compile time; there is no package manifest in this repo.
- Compiled artifacts and Remix build-info were removed from the repository; only sources are kept.
