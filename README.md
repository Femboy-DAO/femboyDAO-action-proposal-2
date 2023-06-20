# femboyDAO-action-proposal-2

---
```
FAP: FAP 2
title: <FAP title> FAP2 UniV2 & UniV3 LP FEM/WETH Liquidity Provision from Multisig
network: <Ethereum | Polygon | Ethereum & Polygon>
status: <Draft> Official
type: <Meta-Governance | Governance> treasury governance
author: <a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s), e.g. (use with the parentheses or triangular brackets): rachelg.eth (@bruleeshark), FirstName LastName <foo@bar.com>, FirstName (@GitHubUsername) and GitHubUsername (@GitHubUsername)> rachelg.eth (@bruleeshark)
implementor: <a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s), e.g. (use with the parentheses or triangular brackets): FirstName LastName (@GitHubUsername), FirstName LastName <foo@bar.com>, FirstName (@GitHubUsername) and GitHubUsername (@GitHubUsername)> Council Multisig
release: (Release Name) FAP2
implementation-date: to be determined
proposal: <snapshot.org proposal link> https://github.com/Femboy-DAO/femboyDAO-action-proposal-2/blob/main/README.md
created: <date created on, in ISO 8601 (yyyy-mm-dd) format> 2023-06-20
requires: <FAP number(s)>  n/a
```
---

<!--You can leave these HTML comments in your merged FAP and delete the visible duplicate text guides, they will not appear and may be helpful to refer to if you edit it again. This is the suggested template for new FAPs. Note that an FAP number will be assigned by an editor. When opening a pull request to submit your FAP, please use an abbreviated title in the filename, `sip-draft_title_abbrev.md`. The title should be 44 characters or less.-->

## Simple Summary

<!--"If you can't explain it simply, you don't understand it well enough." Simply describe the outcome the proposed changes intends to achieve. This should be non-technical and accessible to a casual community member.-->

We propose to add liquidity on uniV2 & uniV3 from our multisig funds. Amounts will be approximately equal to the market rate of FEM/WETH in the univ2 pool and slightly above that in the univ3 pool.

## Abstract

<!--A short (~200 word) description of the proposed change, the abstract should clearly describe the proposed change. This is what *will* be done if the FAP is implemented, not *why* it should be done or *how* it will be done. If the FAP proposes deploying a new contract, write, "we propose to deploy a new contract that will do x".-->

TLDR:
* 2 liquidity additions, +3 FEM per pool + ETH necessary, total liquidity of 6 FEM + ETH necessary.
* This represents around 7.84% of FEM total token supply, and about 7.08% of the ETH in the DAO treasury,* deposited as Uniswap liquidity.

## Motivation

<!--This is the problem statement. This is the *why* of the FAP. It should clearly explain *why* the current state of the protocol is inadequate.  It is critical that you explain *why* the change is needed, if the FAP proposes changing how something is calculated, you must address *why* the current calculation is innaccurate or wrong. This is not the place to describe how the FAP will address the issue!-->

There is very little FEM token liquidity and this makes it difficult for users to acquire the necessary 0.01 for membership and also any users wishing to have voting power in the protocol over a single membership find high slippage and fees, as well as a lack of available FEM on the market, as their barrier. We seek to meet the demands of the community and provide a base liquidity provision to Uniswap v2 and Uniswap v3.

## Specification

<!--The specification should describe the syntax and semantics of any new feature, there are five sections
1. Overview
2. Rationale
3. Technical Specification
4. Test Cases
5. Configurable Values
-->

### Overview

<!--This is a high level overview of *how* the FAP will solve the problem. The overview should clearly describe how the new feature will be implemented.-->

The amount of liquidity provision in the proposal is projected to allow increased user activity in the foreseeable months.

### Rationale

<!--This is where you explain the reasoning behind how you propose to solve the problem. Why did you propose to implement the change in this way, what were the considerations and trade-offs. The rationale fleshes out what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.-->

Proposal for FEM token protocol owned liquidity provision:
Proposal to add liquidity on uniV2 from multisig funds.
3 FEM + equivalent market rate WETH
Proposal to add liquidity on uniV3 from multisig funds.
Sell 3 FEM @ slightly above mkt rate (& therefore deposit no ETH).
How does that work?
Concentrated liquidity in uniswap v3 divides a position based on currentPrice vs priceRange, so we can avoid depositing ETH by setting priceRange slightly above currentPrice.
Why do we want 2 liquidity pools on Uniswap?
Primarily; reduced slippage.
How?
Partial routing to either pool through the uniswap smart router allows the uniswap protocol to utilize more of the total underlying liquidity for each trade, if necessary or if such conditions provide a more favourable trade.
TLDR:
2 liquidity additions, +3 FEM per pool + ETH necessary, total liquidity of 6 FEM + ETH necessary.
This represents around 7.84% of FEM total token supply, and about 7.08% of the ETH in the DAO treasury,* deposited as Uniswap liquidity.

Note*: Math and $ amounts subject to changes per market movements.

### Technical Specification

<!--The technical specification should outline the public Action Plan of the changes proposed.
Include technical documentation if necessary. -->

n.a

### Test Cases

<!--Test cases for an implementation are mandatory for FAPs but can be included with the implementation..-->

univ2 pool: https://www.geckoterminal.com/eth/pools/0xa326324ef5c44789017232a28cc13af61edb9d5e

univ3 pool: https://info.uniswap.org/#/pools/0x7fc309033216f5af765d74b81941d1239efa93fd

### Configurable Values (Via SCCP)

<!--Please list all values configurable via SCCP under this implementation.-->

uni pool parameters already set at deployment, see above links.

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

shoutout to @synthetix team for the original Improvement Proposal Template
