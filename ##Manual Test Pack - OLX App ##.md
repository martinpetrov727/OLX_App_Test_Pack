##Manual Test Pack - OLX App ## 
App/Site - OLX App 
Date: <26.03.2026>
Tester: Martin Petrov

#Scope
//testing create a listing, messeging, search and filter functionalyty.

###Test Cases###

Test Case ID: TC-001
Title: Create a listing with valid data
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open the app
2. Click "Add a listing"
3. Enter a valid title
4. Enter a description
5. Upload photos
6. Select a category
7. Enter a price
8. Select condition
9. Fill in address and contact information
10. Click "View listing"
11. Click "Publish without promoting"

Expected Result:
- Listing is successfully created
- Listing is sent for review


Test Case ID: TC-002
Title: Create a listing without photos
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open the app
2. Click "Add a listing"
3. Enter a valid title
4. Enter a description
5. Do not upload photos
6. Select a category
7. Enter a price
8. Select condition
9. Fill in address and contact information
10. Click "View listing"
11. Click "Publish without promoting"

Expected Result:
- Listing is successfully created
- Listing is sent for review
- Listing has no photos


Test Case ID: TC-003
Title: Create a listing without title
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open the app
2. Click "Add a listing"
3. Leave title empty
4. Enter a description
5. Upload photos
6. Select a category
7. Enter a price
8. Select condition
9. Fill in address and contact information
10. Click "View listing"

Expected Result:
- User cannot proceed to "View listing"
- Error message is displayed: "Please enter a valid title"



Test Case ID: TC-004
Title: Create a listing without description
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open the app
2. Click "Add a listing"
3. Enter a valid title
4. Leave description empty
5. Upload photos
6. Select a category
7. Enter a price
8. Select condition
9. Fill in address and contact information
10. Click "View listing"

Expected Result:
- User cannot proceed to "View listing"
- Error message is displayed: "Please enter a valid description"



Test Case ID: TC-005
Title: Create a listing without selecting category
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open the app
2. Click "Add a listing"
3. Enter a valid title
4. Enter a description
5. Upload photos
6. Do not select a category
7. Enter a price
8. Select condition
9. Fill in address and contact information
10. Click "View listing"

Expected Result:
- User cannot proceed to "View listing"
- Error message is displayed: "Please choose a category"


Test Case ID: TC-006
Title: Create a listing without price
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open the app
2. Click "Add a listing"
3. Enter a valid title
4. Enter a description
5. Upload photos
6. Select a category
7. Leave price empty
8. Select condition
9. Fill in address and contact information
10. Click "View listing"

Expected Result:
- User cannot proceed to "View listing"
- Error message is displayed: "Please enter a price"



Test Case ID: TC-007
Title: Create a listing without address and contact information
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open the app
2. Click "Add a listing"
3. Enter a valid title
4. Enter a description
5. Upload photos
6. Select a category
7. Enter a price
8. Select condition
9. Leave address and contact information empty
10. Click "View listing"

Expected Result:
- User cannot proceed to "View listing"
- Error message is displayed: "Please enter valid address and contact information"



Test Case ID: TC-008
Title: Upload more than allowed number of photos
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open the app
2. Click "Add a listing"
3. Click "Add photos"
4. Select 9 photos

Expected Result:
- User cannot upload more than 8 photos
- System prevents selection or shows an error message




Test Case ID: TC-009
Title: Title maximum length validation
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open the app
2. Click "Add a listing"
3. Enter 71 characters in the title field

Expected Result:
- User cannot enter more than 70 characters



Test Case ID: TC-010
Title: Title minimum length validation
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open the app
2. Click "Add a listing"
3. Enter 15 characters in the title field
4. Click "View listing"

Expected Result:
- Error message is displayed: "Title must contain at least 16 characters"



Test Case ID: TC-011
Title: Description maximum length validation
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open the app
2. Click "Add a listing"
3. Paste text longer than 9000 characters

Expected Result:
- User cannot enter more than 9000 characters



Test Case ID: TC-012
Title: Description minimum length validation
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open the app
2. Click "Add a listing"
3. Enter 39 characters in description
4. Click "View listing"

Expected Result:
- Error message is displayed: "Description must contain at least 40 characters"


Test Case ID: TC-013
Title: Title with only numbers
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open the app
2. Click "Add a listing"
3. Enter only numbers in title
4. Complete the listing

Expected Result:
- Listing is successfully created



Test Case ID: TC-014
Title: Upload photos with invalid format
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open the app
2. Click "Add a listing"
3. Click "Add photos"
4. Select files with unsupported format (e.g., .pict)

Expected Result:
- Photos are not uploaded
- Error message is displayed



Test Case ID: TC-015
Title: Set price to zero
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open the app
2. Click "Add a listing"
3. Enter price as 0
4. Complete listing

Expected Result:
- System suggests category "Free"



Test Case ID: TC-016
Title: Search by keyword
Preconditions:
- App is installed
- User is on home page

Steps:
1. Navigate to search bar
2. Enter keyword "iPhone"
3. View results

Expected Result:
- Listings contain keyword "iPhone" in title or description


Test Case ID: TC-017
Title: Search by keyword with maximum price filter
Preconditions:
- App is installed
- User is on home page

Steps:
1. Enter keyword "iPhone"
2. Open filters
3. Set maximum price to 300€
4. Click "Show Results"

Expected Result:
- Listings match keyword "iPhone"
- Listings price is up to 300€


Test Case ID: TC-018
Title: Search by keyword with price range
Preconditions:
- App is installed
- User is on home page

Steps:
1. Enter keyword "iPhone"
2. Open filters
3. Set price from 100€ to 300€
4. Click "Show Results"

Expected Result:
- Listings match keyword "iPhone"
- Price range is between 100€ and 300€


Test Case ID: TC-019
Title: Search with minimum price only
Preconditions:
- App is installed
- User is on home page

Steps:
1. Enter keyword "iPhone"
2. Open filters
3. Set minimum price to 100€
4. Leave max empty
5. Click "Show Results"

Expected Result:
- Listings match keyword "iPhone"
- Price is above 100€


Test Case ID: TC-020
Title: Search with unrealistic high price
Preconditions:
- App is installed
- User is on home page

Steps:
1. Enter keyword "iPhone"
2. Set minimum price to 1000000€
3. Click "Show Results"

Expected Result:
- No results found message is displayed
- Suggestions are shown


Test Case ID: TC-021
Title: Search by keyword with city filter
Preconditions:
- App is installed
- User is on home page

Steps:
1. Enter keyword "iPhone"
2. Open filters
3. Set location to Sofia
4. Click "Show Results"

Expected Result:
- Listings match keyword
- Listings location is Sofia only


Test Case ID: TC-022
Title: Search by keyword with postal code
Preconditions:
- App is installed
- User is on home page

Steps:
1. Enter keyword "iPhone"
2. Enter postal code "1000"
3. Click "Show Results"

Expected Result:
- Listings are from Sofia


Test Case ID: TC-023
Title: Search by keyword in small town
Preconditions:
- App is installed
- User is on home page

Steps:
1. Enter keyword "iPhone"
2. Enter postal code "2030"
3. Click "Show Results"

Expected Result:
- Listings are from Kostenec


Test Case ID: TC-024
Title: Search with invalid postal code
Preconditions:
- App is installed
- User is on home page

Steps:
1. Enter keyword "iPhone"
2. Enter postal code "1234"

Expected Result:
- System shows error or no location found


Test Case ID: TC-025
Title: Search using current location
Preconditions:
- App is installed
- User is on home page

Steps:
1. Enter keyword "iPhone"
2. Open location filter
3. Click "Use current location"

Expected Result:
- System detects user location automatically


Test Case ID: TC-026
Title: Search by category
Preconditions:
- App is installed
- User is on home page

Steps:
1. Select category "Electronics"

Expected Result:
- Listings are only from Electronics category


Test Case ID: TC-027
Title: Search with wrong category
Preconditions:
- App is installed
- User is on home page

Steps:
1. Select category "Style"

Expected Result:
- Listings are only from Style category
- No Electronics listings appear


Test Case ID: TC-028
Title: Change category without keyword
Preconditions:
- App is installed
- User is on home page

Steps:
1. Select category "Style"
2. Go back
3. Select another category

Expected Result:
- Listings update to new category only


Test Case ID: TC-029
Title: Change category with keyword
Preconditions:
- App is installed
- User is on home page

Steps:
1. Select category "Electronics"
2. Enter keyword "iPhone"
3. Change category to "Style"
4. Search

Expected Result:
- No results found message is displayed


Test Case ID: TC-030
Title: Search by subcategory
Preconditions:
- App is installed
- User is on home page

Steps:
1. Select category "Electronics"
2. Open category filter
3. Select subcategory "Computers"

Expected Result:
- Listings are only from Computers subcategory


Test Case ID: TC-031
Title: Add item to favorites
Preconditions:
- App is installed
- User is logged in

Steps:
1. Search "iPhone"
2. Open listing
3. Click "Heart" icon

Expected Result:
- Item is added to favorites


Test Case ID: TC-032
Title: Remove item from favorites
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open favorites
2. Select item
3. Click "Heart" icon

Expected Result:
- Item is removed from favorites


Test Case ID: TC-033
Title: Favorites persist after logout
Preconditions:
- App is installed
- User is logged in

Steps:
1. Logout
2. Login again
3. Open favorites

Expected Result:
- Favorites list is saved


Test Case ID: TC-034
Title: Save search to favorites
Preconditions:
- App is installed
- User is logged in

Steps:
1. Search "iPhone"
2. Click save search (heart icon)

Expected Result:
- Search is saved in favorites


Test Case ID: TC-035
Title: Remove saved search
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open favorites
2. Go to searches
3. Click "X" on saved search

Expected Result:
- Search is removed


Test Case ID: TC-036
Title: Send message to seller
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open listing
2. Click "Message"
3. Type message
4. Click send

Expected Result:
- Message is sent successfully


Test Case ID: TC-037
Title: Send message when logged out
Preconditions:
- App is installed
- User is logged out

Steps:
1. Open listing
2. Click "Message"

Expected Result:
- User is prompted to log in


Test Case ID: TC-038
Title: Send message without internet
Preconditions:
- App is installed
- User is logged in

Steps:
1. Turn off internet
2. Try to send message

Expected Result:
- Message is not sent
- Retry option is shown


Test Case ID: TC-039
Title: Receive notification from seller
Preconditions:
- App is installed
- User has active chat

Steps:
1. Open messages
2. Check notifications

Expected Result:
- Notification is visible


Test Case ID: TC-040
Title: Send image in chat
Preconditions:
- App is installed
- User is logged in

Steps:
1. Open chat
2. Click attachment icon
3. Upload image
4. Send

Expected Result:
- Image is sent successfully
- Image appears in chat