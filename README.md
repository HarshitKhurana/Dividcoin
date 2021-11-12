# Dividtract (Divident Payout Contract)
##### This is a pet project for getting hands on with SmartContracts development. And may never see the light of day.


### UseCase

- The intent of this contract is to payout dividends to it's investors (A hypothetical set of people).
  - This can be further generalised to all the shareholders in an organisation.
- The Profit made by an organisation can be transferred to this Contract account & will further be paid out as dividends to all investors.


### Functionalities
- Dividend payout will be triggered as soon as Profits are added to the contract.
- Once a dividend is paid out, emit an event for the subscribers to make aware of the transaction.

- `addProfits(uint64 profit) public`
  - The profits made by an organisation can be depositted in this account by using this method, which will further be paid out as dividends.

- `addMember(uint16 member_id) onlyOwner`
  - Only the contract owner can add a member to the table, contingent upon the `BoardTable` not being full already.

- `registerMember(uint16 member_id, unit64 investment)`
  - Once the contract owner has added a member, the member needs to register themeselves by paying in a deposit amount called investment. (no min/max limit on investment)
  - The dividends received by the member will be proportionate to their investment.
  - Dividends can only be paid out to registered members.

- `KickoutMember(uint16 member_id) onlyOwner`
  - Only the owner of the contract can kickout a member from the `BoardTable`.

- `ResignFromBoard(uint16 member_id)`
   - Allows a member to resign from the board and make room for new member.


Note: 
- Ir-respective of whether the investor was kicked out or they themselves resigned, their initial investment will be refunded to their address.
- Currency for this contract is Ethereum.
