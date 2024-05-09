# Solidity_Joint_Savings_Account

Objective:  To create a Solidity smart contract for a joint Ethereum-compatible savings account where 2 users may deposit and withdraw funds.

The File containing the Solidity code for the Ethereum-compatible savings account is named joint_savings.sol and the Execution_Results folder with the screenshot for the Deposit and Withdraw functionality testing.
The code starts by defining the contract JointSavings, creating its variables for address payable (accountOne and accountTwo), address public (lastToWithdraw) and uint public types (lastToWithdrawAmount, contractBalance). The code then defines the withdraw function with 2 arguments for amount and recipient.

Next, the Solidity code defines a require statement to prevent unauthorized access to the account if you are not either the owner of accountOne or accountTwo. If the user is not the owner of the accounts, a text message will display. To prevent overdraws, the code then creates a require statement to check the balance and prevent that a withdraw amount is higher than the account balance.

The next series of functions in the code update the account balances as both deposits and withdraws are transacted. Finally, the code adds a fallback function so the contract can store Ether that’s sent from outside the deposit function.

The contract was then compiled and deployed in REMIX IDE and the interaction with the deployed contract performed to test its functionality. 

## Deposit Functionality Test Screenshots: ##

The following screenshots show the following transactions: Initial Balance, Transaction 1: Send 1 ether as wei, Transaction 2: Send 10 ether as wei, Transaction 3: Send 5 ether, and the use of the dummy accounts.

<img src="/Execution_Results/startbal2.png">
###Transaction Send 1 ether as wei
<img src="/Execution_Results/Oneethwei3.png">
<img src="/Execution_Results/OneethBAL4.png">
###Transaction Send 10 ether as wei###
<img src="/Execution_Results/TenethBAL5.png">
###Transaction Send 5 ether###
<img src="/Execution_Results/FiveethBAL6.png">
<img src="/Execution_Results/Fivebal7.png">
###Dummy Accounts Set Up###
<img src="/Execution_Results/dummyacct8.png">

##Withdraw Functionality Screenshots: ##

The following screenshots show withdrawing 5 ether into accountOne and 10 ether into accountTwo. After each transaction I used the contractBalance function to verify that the funds were withdrawn from the contract. Finally, I also use the lastToWithdraw and lastWithdrawAmount functions to verify that the address and amount were correct.

<img src="/Execution_Results/5ethTR9.png">
<img src="/Execution_Results/11.png">
<img src="/Execution_Results/12.png">

### Resources ###

UC Berkely Fintech Bootcamp Class Material
UC Berkely Fintech Bootcamp  Tutoring Session 5/8/2024


