# General Philosophy

Smart contract programming requires a different engineering mindset than what you may be used to.

The cost of failure is high and changes can be difficult, making it in some ways similar to hardware programming or financial services programming rather than web or mobile app development.

It is therefore not enough to defend against known vulnerabilities. Instead you will need to learn a new philosophy of development.

## Prepare for Failure

+ Place circuit breakers
+ Manage money at risk (rate limiting, maximum usage,etc)
+ Effective mechanism for proxy upgrades

## Stay up to Date

+ Check your contracts for any new bug as soon as it is discovered
+ Keep on upgrading all tools and libraries
+ Adopt new security techniques that emerge (and seem useful)

## Keep it simple

+ Keep contract logic simple. Modularize code. Use already written code, use as many lego blocks as you can, before writing custom logic
+ Clarity over performance (Debatable)
    > For example one could argue that the OpenSea Seaport contract is so damned performant that it affects the auditability of the contracts. But realise the fact that the Seaport contract will be deployed on the Ethereum mainnet and will be used to mint hundereds of thousands of NFTs, saving the users **millions of dollars** over the course of time.

    > So, based on the nature of your contract, do have healthy, sane discussions on whether you will place 
    more impetus on performance or clarity.

+ Roll out in phases. Have a bug bounty in place, test your code-base thoroughly and immediately add relevant tests to your codebase as soon as a new attack is discovered.

## Blockchain Properties

+ Randomness can be gamified.
+ Timestamps are imprecise. Miners can influence the time of execution of a txn within a margin of several seconds
+ Beware of external calls. Private data is not actually private and public functions can be called by anyone in any order.
+ Prefer reusing contract code only when you have proven previously-deployed contracts which you own. Otherwise go for duplication of code.
    > Efforts such as OpenZeppelin's Solidity Library seek to provide patterns such that secure code can be re-used without duplication

# Development best practices:

+ External calls are very risky. 
    + Try and avoid doing that, prefer duplicating code over using a call to an external contract. 
    + And when you absolutely have to do that, make sure that the contract is owned/maintained/managed by a trusted party. 
    + Always mark your function making external calls as unsafe via comments and naming convention
    + Avoid making state changes after the external call. The usual *re-entrancy attack* and following the *check-effects-interactions* pattern circus.

+ 