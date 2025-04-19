# On-Chain Expense Tracker

A decentralized expense tracking application built using Solidity and React. This DApp allows users to register, log shared expenses, and track balances on the Ethereum blockchain.

---

## New Features Added

### 1️. Get Total Number of Registered People (Solidity)

#### Description:
A new view function was added to the smart contract to allow external applications (like the frontend) to retrieve the **total number of registered users** on the platform.

#### Code Added in `blockbase.sol`:

```solidity
// NEW FUNCTION
function getTotalRegisteredUsers() public view returns (uint256) {
    return registeredPeople.length;
}
```

### 2. Display Total Registered Users (React Frontend)

#### Description:
The JS was updated to fetch the total number of registered users from the smart contract and display it in the user interface.

``` JS
const totalUsers = await contract.methods.getTotalRegisteredUsers().call();
setTotalUsers(totalUsers);
<p>Total Registered Users: {totalUsers}</p>
```
## Screenshot:

![image](https://github.com/user-attachments/assets/2dea51b4-728f-42e0-b450-1978a8ded940)
