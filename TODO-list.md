# Task: Initialize Storage by Zapier in the Club Membership Records Zap

- [ ] Share my Storage by Zapier account with Peter Moe's team to they can use the feature. 
- [ ] Zap: Club Membership Records: Add a step immediately after the trigger to add Storage by Zapier >> Increment Value.
- [ ] Configuration of Increment Value Zap step: Assign the value of 'Member ID' to the storage key, and set the increment value to 1.
      
# Task: Club Membership Records Zap: Add a Path step immediately following the Increment Value step

- [ ] There will be a minumum of 3 path steps; ( 1 ) Filter by Individual & Honorary Members, ( 2 ) Filter by Household Members - 1st member; and ( 3 ) Filter by Household Members - 2nd member

# Task: Configure the path conditions for each path

- [ ] Rules for Filter by Individual & Honorary Members: Membership Level exactly matches 'Honorary' OR 'Individual'.
- [ ] Rules for Filter by Household Members - 1st member: Membership Level exactly matches 'Household'.
- [ ] Rules for Filter by Household Members - 2nd member: Membership Level exactly matches 'Household'.

# Task: Update the `1) Garden Member Info` table

- [ ] Columns ( L to R ): Member ID ( Num ), Last Name ( T ), First Name ( T ), Membership Level ( DD ), Spouse / Partner ( T ), Email Address ( email ), Address, City ( T ), State ( DD ), Zip Code ( Num ), County ( T ), Phone Number ( phone_number ). Options to add: Year Joined, Latest Table Submission ( MM-YY-DDDD ).

# Task: Change the Ninja Forms date / time submission in trigger to only a data formatted as MM-DD-YYYY 

- [ ] Add Zapier Formatter step at the start of the Zap to change the data / time form subission to a date only format 

# Task: Add a 'Year Joined' field to the 'Garden Member Info' table

- [ ] Should this field be left empty, or filled with a static value (e.g. 1900, 1942, or some other value )?
- [ ] Note: Any static value will be overwritten when the current club data is imported into Zapier Tables. 

# Task: Update the `3) Household ( HH ) Memberships` table

- [ ] Change the column `Fporm Submission ID` to `Member ID`.
- [ ] Map the `Member ID` column to the the Increment Value key `MemberID`.
- [ ] Delete columns: `Last Name - Member` & `First Name - Member`. [ Those values will be captured when this table is joined to `Garden Member Info`.
- [ ] Add column: `Year Joined`.

# Task: Delete the `2) Member Contact Info` table. 

- [ ] All that data is going to get captured in the `1) Garden Member Info` table. 

# Task 9

# Task 10
