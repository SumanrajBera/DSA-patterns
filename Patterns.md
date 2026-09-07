# DSA Patterns

## Palindrome
- Core property: symmetry
- Checking a known substring → compare ends inward
- Finding longest palindrome → expand around center
- Odd center → (i, i)
- Even center → (i, i+1)

## Binary Exponentiation / Exponentiation by Squaring
- Core idea: halve the exponent, square the base
- Instead of multiplying x by itself y times → break the power into pairs
- Even exponent → x^y = x^(y/2) * x^(y/2) = (x^(y/2))²
- Odd exponent → take one x separately, then handle the remaining even exponent
- num → keeps growing into x², x⁴, x⁸, ... by squaring
- pow → keeps shrinking by half
- result → accumulates the powers needed when pow is odd (which is 1 [base power for collection] and any other odd power that comes before )
- Each step halves the exponent → O(log y) instead of O(y)
- Often combined with % MOD to prevent huge intermediate values

## Fact about prime number
- A square of prime number will always have exactly 3 factors

### Distinct subsequences — counting instead of generating
- Recursive generation: extend every previously generated subsequence with the current character.
- If only the count is needed, we may be able to count these extensions instead of constructing them.
- Repeated characters can create duplicate resulting subsequences.
- For distinct subsequences, track/count results by their ending character to handle those duplicates.
