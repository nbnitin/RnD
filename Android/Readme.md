
# Major step for this is to create Service Account, once this service account gets ready only after you are able to consume apis for Android

API Details link
https://developers.google.com/android-publisher/api-ref/rest/v3/edits.bundles/upload

A. Create Service Account(You have to login from owner's email into google play console)
1. Open the Google Play Console
2. Click Account Details, and note the Developer Account ID listed there
3. Click Setup → API access
4. Click the Create new service account button
5. Follow the Google Cloud Platform link in the dialog, which opens a new tab/window:
6. Click the CREATE SERVICE ACCOUNT button at the top of the Google Cloud Platform Console
7. Verify that you are on the correct Google Cloud Platform Project by looking for the Developer Account ID from earlier within the light gray text in the second input, preceding .iam.gserviceaccount.com. If not, open the picker in the top navigation bar, and find the one with the ID that contains it.
8. Provide a Service account name and click Create
9. Click Select a role, then find and select Service Account User, and proceed
10. Click the Done button
11. Click on the Actions vertical three-dot icon of the service account you just created
12. Select Manage keys on the menu
13. Click ADD KEY -> Create New Key
14. Make sure JSON is selected as the Key type, and click CREATE
15. Save the file on your computer when prompted and remember where it was saved to
16. Return to the Google Play Console tab, and click DONE to close the dialog
17. Click on Grant Access for the newly added service account at the bottom of the screen (you may need to click Refresh service accounts before it shows up)
18. Choose the permissions you'd like this account to have. We recommend Admin (all permissions), but you may want to manually select all checkboxes and leave out some of the Releases permissions such as Release to production
19. Click Invite user to finish

# You will get JSON file store it that JSON

# Note:- As per google policy you have to upload first build manually just to enroll/ register package name to play store

now go to where your json is stored, and download sh files from this repo and put all files (JSON, 2 sh files) at same location

and run this command to generate JWT token(JSON Web Token) sh accesstoken.sh ./service_account.json https://www.googleapis.com/auth/androidpublisher

exaplaination for above shell command
./ -> current directory
service_account.json -> json file name which you get from service account creation steps
https://www.googleapis.com/auth/androidpublisher -> Scope this is mentioned on google developer api page 

<img width="500" alt="Screenshot 2023-09-06 at 2 26 49 PM" src="https://github.com/nbnitin/RnD/assets/5785670/0e246cc9-ff5d-41b4-8de9-03297fa5dba7">



