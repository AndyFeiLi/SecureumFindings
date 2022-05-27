Wrong Order of Operations Leads to Exponentiation of rewardPerTokenStored: rewardPerTokenStored is mistakenly used in the numerator of a fraction instead of being added to the fraction. The result is that rewardPerTokenStored will grow exponentially thereby severely overstating each individual's rewards earned. Individuals will therefore either be able to withdraw more funds than should be allocated to them or they will not be able to withdraw their funds at all as the contract has insufficient SNX balance. This vulnerability makes the Unipool contract unusable.

    Recommendation: Adjust the function rewardPerToken() to represent the original functionality.

    Critical Risk severity finding from Sigma Prime's Audit of Synthetix Unipool