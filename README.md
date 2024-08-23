# Google-AppSheet-Application

This project involves creating a simple Google AppSheet application based on data from Google Sheets. The app manages information about learners, classes, and teachers. The instructions below will guide through setting up the app.
Prerequisites

## Before you start, ensure you have the following:

    A Google account to access Google Sheets and Google AppSheet.
    A copy of the Google Sheet provided for this exercise.

## Steps to Create the App
1. Copy the Google Sheet

    Open the provided Google Sheets link.
    Navigate to File > Make a copy to save a copy to your Google Drive.

2. Create a New App on Google AppSheet

    Log in to Google AppSheet.
    Click on Create new app.
    Select Start with your own data.
    Choose the copied Google Sheet as the data source.

3. Add Tables to the App

    Ensure the app automatically includes all tables (Classes, Learners, Teachers) from your Google Sheet.
    If any table is missing, manually add it by navigating to the Data tab in AppSheet.

4. Set Column Types

Review and adjust the column types for each table as follows:

Learners Table:

    ID: Text
    First Name: Name
    Surname: Name
    Date Enrolled: Date
    Grade: Text
    Class: Ref (Linked to Classes table)
    Teacher Display Name: Ref (Linked to Teachers table)

Classes Table:

    ID: Text
    Class Name: Text
    Teacher: Ref (Linked to Teachers table)
    Related Learners: List (Linked to Learners table)
    Number of Learners: Number (Formula to count learners)
    Teacher Display Name: Ref (Linked to Teachers table)

Teachers Table:

    ID: Text
    First Name: Name
    Surname: Name
    Display Name: Name (Formula: "Surname, First Name")
    Position: Enum ("HOD", "Deputy Principal", "Principal")

For columns not present in the Google Sheet, create a virtual column with the correct formula.
5. Create App Views

Configure the following views for the app:

    Form View (New Learners):
        Create a form to add new learners.
        Include fields for First Name, Surname, Grade, and Class.

    Table View (All Learners):
        Create a table view showing all learners.
        Group the data by Grade and Class.

    Deck View (Classes):
        Create a deck view to display class information.
        Set Class Name as the primary field, Teacher Display Name as the secondary field, and Number of Learners as the summary.

    Table View (Grade 1 Learners):
        Create a slice of the Learners table for Grade 1 learners.
        Display this slice in a table view.

6. Name the App

    Go to the Info tab in AppSheet.
    Set the app's name to Yanga Zukelwa Task 1.

## Conclusion

After completing these steps, the app should be fully functional, allowing you to manage learners, classes, and teachers efficiently. The views created will enable easy data entry and visualization within the app.

For any issues or further instructions, please refer to the AppSheet documentation.
