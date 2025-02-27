
# Goal: Configure the `Club Membership Records` Zap to automatically: (1) create a new record OR, (2) update an existing record when the Zap triggers ( form submission ). 
- [ ] The first and second ( household ) member tables need both a creation step AND an update step. 

# Update the `Custom Membership Records` Zap

## Task: Initialize Storage by Zapier in the Club Membership Records Zap

- [ ] Share my Storage by Zapier account with Peter Moe's team to they can use the feature. 
- [ ] Zap: Club Membership Records: Add a step immediately after the trigger to add Storage by Zapier >> Increment Value.
- [ ] Configuration of Increment Value Zap step: Assign the value of 'Member ID' to the storage key, and set the increment value to 1.

## Task: Change the Ninja Forms date / time submission in trigger to only a data formatted as MM-DD-YYYY 

- [ ] Add Zapier Formatter step at the start of the Zap to change the data / time form subission to a date only format 
      
## Task: Add a Path step immediately following the Increment Value step

- [ ] There will be a minumum of 3 path steps; ( 1 ) Filter by Individual & Honorary Members, ( 2 ) Filter by Household Members - 1st member; and ( 3 ) Filter by Household Members - 2nd member

## Task: Configure the path conditions for each path - Preparation to build the `Joint Membership Membership` table

- [ ] Rules for Filter by Individual & Honorary Members: Membership Level exactly matches 'Honorary' OR 'Individual'.
- [ ] Rules for Filter by Household Members - 1st member: Membership Level exactly matches 'Household'.
- [ ] Rules for Filter by Household Members - 2nd member: Membership Level exactly matches 'Household'.

## Task: Update the `1) Garden Member Info` table

- [ ] Columns ( L to R ): Member ID ( Num ), Last Name ( T ), First Name ( T ), Membership Level ( DD ), Spouse / Partner ( T ), Email Address ( email ), Address, City ( T ), State ( DD ), Zip Code ( Num ), County ( T ), Phone Number ( phone_number ). Options to add: Year Joined, Latest Table Submission ( MM-YY-DDDD ).

## Task: Add a 'Year Joined' field to the 'Garden Member Info' table

- [ ] Should this field be left empty, or filled with a static value (e.g. 1900, 1942, or some other value )?
- [ ] Note: Any static value will be overwritten when the current club data is imported into Zapier Tables.

## Task: Delete the `2) Member Contact Info` table. 

- [ ] All that data is going to get captured in the `1) Garden Member Info` table. 

## Task: Update the `3) Household ( HH ) Memberships` table

- [ ] Change the column `Fporm Submission ID` to `Member ID`.
- [ ] Map the `Member ID` column to the the Increment Value key `MemberID`.
- [ ] Delete columns: `Last Name - Member` & `First Name - Member`. [ Those values will be captured when this table is joined to `Garden Member Info`.
- [ ] Add column: `Year Joined`.

## Task: Join Committees to Honorary and Individual Member data
- [ ] Create a separate table to join information from `1) Garden Member Info` and `Committees` tables. Link the tables by `Member ID`.

---

# Update the Membership application form

## Task: Remove section asking for renewing members to update their information
- [ ] On the Join / Renew form, remove the section titled `Did you member directory information change in the last year?`

## Task: The 2nd Household Member will require their own set of committee selections on the triggering form
- [ ] Add selections and conditions to the membership application form to show committee options for a 2nd household member when ML == `Household`.

# Build Custom Views
- [ ] Member Info table ( Individual & Honorary members only )
- [ ] Joined Household Record table ( Household members only )
- [ ] Committee Selections, Individual and Honorary members only
- [ ] Committee Selections, Household members only
- [ ] Member Attributes, Individual and Honorary members only
- [ ] Member Attributes, Household members only

## Custom View - Members Attributes, Individual and Honorary members only
- [ ] Decide which fields to keep and which to remove from the `4) Member Attributes` table.

## Custom View - Member Attributes, Household members only
- [ ] The membership application form does not currently distinguish between input for the first and second household member. Fix this on the form so the input can be automated. 

