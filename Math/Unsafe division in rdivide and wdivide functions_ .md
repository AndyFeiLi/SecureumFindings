Unsafe division in rdivide and wdivide functions: The function rdivide on line 227 and the function wdivide on line 230 of the GlobalSettlement contract, accept the divisor y as an input parameter. However, these functions do not check if the value of y is 0. If that is the case, the call will revert due to the division by zero error.

    Recommendation: consider adding a require statement in the functions to ensure y > 0, or consider using the div functions provided in OpenZeppelin’s SafeMath libraries

    Medium Risk severity finding from OpenZeppelin’s Audit of GEB Protocol