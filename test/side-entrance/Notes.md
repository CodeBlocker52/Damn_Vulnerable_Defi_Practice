# Challenge-4

# SIDE ENTRANCE

## Desc

The challenge starts with a flash loan pool that has 1000 ETH in balance.
It allows users to deposit and withdraw ETH
We need to drain the pool

## Plan of Action

Similar to the previous challenge, we are going to leave a backdoor and claim our ETH later. We will exploit the 3 functions flashLoan, deposit and withdraw

We request a flashLoan
During the flashloan we deposit the borrowed assets back to the pool. The flashLoan will succeed since the balance of the pool didn't change, but the contract will credit our mapping balance.
After the flashLoan is completed and the contract credited us, we call the withdraw function to drain all the ETH that we "deposited" earlier (even though it wasn't our ETH but we borrowed ETH)
The challenge is completed and we were able to drain all the ETH from the pool!! :)
