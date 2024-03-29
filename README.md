# Meetings

## Criteria

A good meeting should:

- Include no more than 3 people, __OR__

- Have _all of the following_:
  1. __A leader__. The leader is responsible for:
	    1. Formulating the agenda and homework.
	    2. Divining and enforcing invitations. _Not everyone gets invited to all meetings._
	    3. Scheduling, inviting, and tracking RSVPs.
	    4. Distributing the agenda and homework.
	    5. Facilitating the meeting.

  2. __Homework__. Background references and resources, shaping and informing perspective on core point(s) of the meeting. This should be clearly stated in an agenda.

  3. __An agenda.__<sup>[example](#agenda-example)</sup>

These three standards for a >=3-human meeting are __MANDATORY__. _Any meeting where any participant has failed to recieve an agenda or to complete the homework should be called off and rescheduled._ This is critical for skin-in-the-game buy in and accountable collaborative productivity. It will also naturally and beneficially restrict both meeting size and frequency.


## Meeting Types

__Consensus__ meetings hint toward all-hands meetings and/or project management meetings. Their purpose is essentially to decide to act decisively as a group. Cooperative decisions can be reached with (in order of efficacy):

- tried and true forms of gestures  and grunts, which are collectively undertaken whenever any speaker has finished the first half of any sentence,
  + gestures can include hand-waving, raised fists, pounding fists, clenched fists, touching lips with index finger, pinching nose, grabbing furniture...
  + grunts can include but are not limited to panting, whimpering, sighing, and holding your breath until the contrarians concede because the pathos has replaced the majority of oxygen in the air
- coercision and/or extortion before the meeting
- what they call voting, which is just a politically correct way of adding unnecessary and irrelevant rituals to some combination of the first two forms. 

Please seek to educate, garner early feedback, and document an engineering process or other provenance of a proposal. A consensus meeting is NOT a brainstorming or engineering session; the point is _Yea_ or _Nea_, not revision or invention. These types of meetings should be limited to high-impact and large-scale solutions that will impact life for everyone at the meeting and possibly minions or groupies. Final decisions and attached accountability should be documented in a consistent way.

__Engineering__ meetings are held with the purpose of investigating and building a problem and/or solution. Eventually, a solution will then either be brought to a consensus meeting, or will simply be implemented, depending on scope, impact, and audacity of the engineers. These are NOT open-invitation meetings, and participation should be tightly controlled and limited to the relevant problem designers and solution builders (engineers).

__Teaching__ meetings are held to emulate the role of the classroom. These may be lecture style or discussion based.

__Pep talk__ meetings are held with the shameless and advisable intention of showing the likenesses of human faces to one another for a few brief moments. Topics of discourse can involve bragging about how much awesome stuff you did last week, worrying about how you're going to get everything done this week, and blaming any problems or tardinesses you have on other people. These should be notably time-restricted to prevent participants from developing human-interaction dependencies or other forms of weakness.

__Hangout__ meetings are granted unstructured times to commiserate, rant, ass-pat, and speculate. No clever ideas, solutions, or bridging questions are allowed; just team-bonding and emotional comfort food. The only allowed topics of conversations are the weather, cats, the professional American Football league (NFL), and suggestive but not provocative mainstream criticisms that have been read or heard somewhere else around politics, religion, and/or sex.

## Meeting Nontypes

__Informational__ meetings are unnecessary. This is what email is for.

__Stakeholder__ meetings should involve a small number of delegated representatives appearing on behalf of the team. This is a _nontype_ because it's not really a meeting, it's a press conference -- probably on par with the public relations attitude at CERN: _I will try to be polite and patient despite the continuing reference to photons as 'fairy dust'._ 
  + These meetings should happen as infrequently as possible so that those short-straw representatives can try to get some actual work done. 
  + Delegated representatives may find it advisable to have an Engineering Meeting prior to the stakeholder assembly in order to devise believable and convincing stories and excuses, as well as to anticipate strategies to counter protestors who may ask questions.

### Agenda example

```markdown
---
type: Engineering
leader: Isaac
date: Thurs, 2019 May 16, 19:00Z
homework: 
  - Must-Read: https://github.com/multi-geth/multi-geth/issues/55
  - Must-Read: https://github.com/ethereumproject/go-ethereum/wiki/JSON-RPC#geth_getaddresstransactions
  - Should-Peruse: https://github.com/ethereum/go-ethereum/tree/master/cmd/clef (README)
  - Should-Peruse: https://github.com/etclabscore/jade-signer-rpc (README)
---

## What is the problem on the table?

Address/transaction indexing is useful for cases like wallets and other account-management roles, but
there are strong arguments for moving account management away from client purview.

Problem: Is this feature worth pursuing? (GO/NOGO)
Problem: If so, What approach should be taken?

## Why is this an important problem; what will the domain of impact be?

A frequent use case for balance-based account (ie ledgers) is to list transactions. With current client
data and API implementation, this view is discouragingly inconvenient, requiring impassably signficant expertise and invention to achieve
for an apparent majority of users.

The impact of the feature, especially a feature that can be extended more generally to other "advanced" account-management features,
would potentially impact third-party wallet applications, DAPP development, and institutional users.

## What are the criteria for a solution?

- [ ] Must design the problem (and potential solution approach) with awareness of existing account management tools.
- [ ] If-GO: Must provide a documented API for listing transactions by account.
- [ ] If-GO: Should be architecturally extensible; built in a way that makes extending logic thru other account/tx-relating calls approach trivial.
- [ ] If-GO: Should be human-accessible; built in a way that makes interaction with developers and end-users approach fun!

## What are outlines of possible solutions?  (at least two, no more than 5)

- [ ] A: GO: A standalone utility interoperating with a standard RPC-enabled ET_ client, either via library or 'wire' JSON RPC interfaces.
- [ ] B: GO: A Go plugin that utilizes a few simple interface methods and/or subscriptions to act as an 'add-on' to a go-ethereum or multi-geth client.
- [ ] C: NOGO: This feature is not worth pursuing at this time; instead we should look at...
```

