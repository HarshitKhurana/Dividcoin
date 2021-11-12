# Dividcoin
##### This is a pet project for getting hands on with SmartContracts development. And may never see the light of day.


### UseCase

- The intent of the coin is to payout dividends to it's board of directors (A hypothetical set of people).
  - This can be further generalised to all the shareholders in an organisation.
- The Profit made by an organisation can be transferred to this Contract account & will further be paid out as dividends to board members.


### Functionalities

- `addProfits(uint64 profit) public`
  - The profits made by an organisation can be depositted in this account by using this method, which will further be paid out as dividends.

- `addMember(uint16 member_id) onlyOwner`
  - Only the contract owner can add a member to the table, contingent upon the `BoardTable` not being full already.

- `registerMember(uint16 member_id, unit64 deposit)`
  - Once the contract owner has added a member, the member needs to register themeselves by paying in a deposit amount. (no min/max limit on deposit)
  - The dividends received by the member will be proportionate to this deposit amount.
  - Dividends can only be paid out to registered members.

- `KickoutMember(uint16 member_id) onlyOwner`
  - Only the owner of the contract can kickout a member from the table.

- `resignFromBoard(uint16 member_id)`
   - Allows a member to resign from the board and make room for new member.



Note: 
- Ir-respective of whether the member was kicked out or they themselves resigned, their initial deposit will be refunded to their address.
- Currency of token is Ethereum.

