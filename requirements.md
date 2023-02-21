# Software Requirements

## Vision
### What is the vision of this product?
- Removes banks and loan officials from the equation when trying to see if you would be a good candidate to receive a mortgage based on user input criteria 
### What pain point does this project solve?
- Allows the normal Joe/Jane access to a wealth of data which will allow them to know when they are competitive/qualified for a loan given the pre-stated criteria
### Why should we care about your product?
- If you don't want your credit score to go up because of all the hard inquiries, this is the website for you.
- Are you interested in removing yourself from the grind/hassle of paying rent and ready to join the class of landed gentry, then this website will push info to the user which will facilitate the homebuying process.

## Scope (In/Out)
### IN - What will your product do?
- Source the data, scrub the data, and prepare it for training
- We will train our model on different combinations of data so it can make the best decisions based upon the user supplied information 
- Will take in user supplied data (INPUT) which will be compared against a trained model containing data across all 50 states and return to the user the likelihood of them receiving a loan
- We will store this INPUT for our own non-nefarious deeds like internal marketing and company direction

### OUT - What will your product not do?
- Be able to predict things outside its data, so it can't help you with car loans
- It will be limited by the information we have trained it on so it doesn't self update, that is to say when new models come out they will have to manually "folded" into the current programs
- It will not provide information based upon user credit score
 
## Minimum Viable Product vs
 
### What will your MVP functionality be?
- A machine learning model trained on public mortgage records
- A display of where the user is relative to the records
- A fully connected front end, back end, and database

### What are your stretch goals?
- Us storing and capitalizing upon user inputted data
- Providing information based upon location and user salary for Down Payment Assistance (DPA)

## Functional Requirements
- An admin can create and delete user accounts to access info
- An admin/database user can access web site user INPUT info to process it for interpretation
- A user can enter various data points (INPUT) to our ML model
- Our ML model then calculates the likelihood of approval of a home loan
- Have the info our ML model cranked out returned to final user via the website

## Data Flow
[USER ENTERS INPUT] →	[Input to DB] → [Info accessible to website owner] → [Input to ML Model] → [ML Prediction] → [Prediction Returned]

		
## Non-Functional Requirements

- Security: User account creation via django app and saving of previous searches saved and privacy of data
- Maintainability: Each year as new data is produced in CSV format by the federal government will need to have its data scrubbed and validated. This data will then be added to the current ML model resulting in a new version. This new version once confirmed to be working will be uploaded to the live site
- Testability: Our code 80%+ covered with PyTest. Confirmation via testing of Creation, Read, Update, Deletion again using PyTest. Utilized VSCode's ThunderClient feature to review and confirm results
