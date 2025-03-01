
# Goal: Configure the `Club Membership Records` Zap to automatically: (1) create a new record OR, (2) update an existing record when the Zap triggers ( form submission ). 
- [ ] The first and second ( household ) member tables need both a creation step AND an update step. 

# Update the `Custom Membership Records` Zap

## Task: Initialize Storage by Zapier in the Club Membership Records Zap

- [X] ~~Share my Storage by Zapier account with Peter Moe's team to they can use the feature.~~ 
- [X] ~~Zap: Club Membership Records: Add a step immediately after the trigger to add Storage by Zapier >> Increment Value.~~
- [X] ~~Configuration of Increment Value Zap step: Assign the value of 'Member ID' to the storage key, and set the increment value to 1.~~

## Task: Change the Ninja Forms date / time submission in trigger to only a data formatted as MM-DD-YYYY 

- [X] ~~Add Zapier Formatter step at the start of the Zap to change the data / time form subission to a date only format.~~ 
      
## Task: Add a Path step immediately following the Increment Value step

- [ ] There will be a minumum of 3 path steps; ( 1 ) Filter by Individual & Honorary Members, ( 2 ) Filter by Household Members - 1st member; and ( 3 ) Filter by Household Members - 2nd member

## Task: Configure the path conditions for each path - Preparation to build the `Joint Membership Membership` table

- [ ] Rules for Filter by Individual & Honorary Members: Membership Level exactly matches 'Honorary' OR 'Individual'.
- [ ] Rules for Filter by Household Members - 1st member: Membership Level exactly matches 'Household'.
- [ ] Rules for Filter by Household Members - 2nd member: Membership Level exactly matches 'Household'.

## Task: Update the `1) Garden Member Info` table

- [X] ~~Columns ( L to R ): Member ID ( Num ), Last Name ( T ), First Name ( T ), Membership Status ( DD ), Membership Level ( DD ), Spouse / Partner ( T ), Email Address ( email ), Address, City ( T ), State ( DD ), Zip Code ( Num ), County ( T ), Phone Number ( phone_number ), Year Joined ( Num ), Form Submission Date ( MMMMa-YY-DDDD ).~~

## Task: Add a 'Year Joined' field to the 'Garden Member Info' table

- [ ] Should this field be left empty, or filled with a static value (e.g. 1900, 1942, or some other value )?
- [ ] Note: Any static value will be overwritten when the current club data is imported into Zapier Tables.

## Task: Delete the `2) Member Contact Info` table. 

- [X] ~~All that data is going to get captured in the `1) Garden Member Info` table.~~ 

## Task: Update the `3) Household ( HH ) Memberships` table

- [X] ~~Rename table to `2) Household ( HH ) Members`.~~ 
- [X] ~~Change the column `Form Submission ID` to `Member ID`.~~
- [ ] Map the `Member ID` column to the the Increment Value key `MemberID`.
- [X] ~~Delete columns: `Last Name - Member` & `First Name - Member`. [ Those values will be captured when this table is joined to `Garden Member Info`.~~
- [X] ~~Add columns: `Year Joined`, and `Form Submission Date`.~~

## Task: Join Committees to Honorary and Individual Member data
- [ ] Create a separate table to join information from `1) Garden Member Info` and `Committees` tables. Link the tables by `Member ID`.

## Task: Create a `X) Member Attribute - 2nd HH Member` table
- [ ] Table will capture Member Interests, Expertise, & Gardening Interests info for household members. 
---

# Update the Membership application form

## Task: Remove section asking for renewing members to update their information
- [ ] On the Join / Renew form, remove the section titled `Did you member directory information change in the last year?`

## Task: Household Memberships - Member Interests
- [ ] Create 2 sections, one each for first and second household member that address `Member Interests, Mentoring, & Gardening Expertise`

## Task: Household Memberships - Committees
- [ ] Create 2 sections, one each for first and second household member that address `Club Activities and Service Committees`.

---

# Build Custom Views

- [ ] Joined Member Contact Info table ( Individual, Honorary, & 1st HH members only ).
- [ ] Joined Household Member Record table ( combines `Joined Member Contact Info` and `2nd Household Member` tables )
- [ ] Joined Committee Selections of All Members ( Except 2nd HH ) - applies to Individual, Honorary, & 1st HH members only.
- [ ] Committee Selections of 2nd Household Members

- [ ] Joined Member Attributes of All Members ( Except 2nd HH ) table - applies to Individual, Honorary, & 1st HH members only ).
- [ ] Member Attributes of 2nd Household Members.

## Custom View - Members Attributes, Individual and Honorary members only

- [ ] Decide which fields to keep and which to remove from the `4) Member Attributes` table.
- [ ] Update column: Change `Submission ID` to `Member ID`. Remap `Member ID` to the `MemberID` key in the Increment Value step.
- [ ] Remove columns: (1) Year Joined, (2) Spouse / Partner Name ( those will move to the `1) Garden Member Info` table.  

## Custom View - Member Attributes, Household members only

- [ ] The membership application form does not currently distinguish between input for the first and second household member. Fix this on the form so the input can be automated.

---

# Migrate Existing Membership Records to Zapier Tables

- [ ] Copy the file currently stored on the Club's Google Drive.
- [ ] Divide and restructure the file as needed so that each remaining file and column maps one-for-one with it's target table in Zapier.
- [ ] Generate a test `.csv` file to upload to a Zapier table.
- [ ] Follow Zapier's documentation for importing a `.csv` file.
- [ ] Repeat as needed until all data is imported.
- [ ] IMPORTANT! Each imported record into a Zapier table will require a value Member ID. Records for the same member across  different tables must all have the same Member ID.

---

# Topics to document for new Membership System

- [ ] Access to the membership system on Zapier
- [ ] Zapier team admin sends a team member invitation that must be accepted.
- [ ] Logging in to Zapier
- [ ] The Zapier landing page; accessing Zaps, Tables, and Interfaces
- [ ] Orient users to a Zap
- [ ] Orient users to Zapier Tables
- [ ] Orient users to Zapier Interfaces
- [ ] Table versus View
- [ ] Filtering a view.
- [ ] Saving a custom view.
- [ ] The custom views set up for the membership recordkeeping system

# Create an organizational accont on GitHub for the Garden Club of Minneapolis

- [ ] Identify the steps involved.
- [ ] Creating an account login to administer the account
- [ ] How contributers can access the GCM wiki on GitHub

