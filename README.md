# meet-app

Del Manzueta Meet App TDD
Key Features:
•	Filter events by city.
•	Show/hide event details.
•	Specify number of events.
•	Use the app when offline.
•	Add an app shortcut to the home screen.
•	View a chart showing the number of upcoming events by city.


FEATURE 1: FILTER EVENTS BY CITY
User Story:
As a User
I should be able to “filter events by city”
So that I can see the list of events that take place in that city

Scenario 1: When user has not searched for a city, show upcoming events from all cities. 
Given: User has not searched for any city
When: User opens the app
Then: User should see a list of all upcoming events.
Scenario 2: User should see a list of suggestions when they search for a city.
Given: The main page is open
When: User starts typing in the city textbox
Then: User should see a list of cities (suggestions) that match what they have typed
Scenario 3: User can select a city from the suggested list.
Given: User was typing “Berlin” in the city textbox and the list of suggested cities is showing
When: User selects a city (e.g., “Berlin, Germany”) from the list
Then: User city should be changed to that city (i.e., “Berlin, Germany”) and the user should receive a list of upcoming events in that city.




FEATURE 2: SHOW/HIDE AN EVENTS DETAILS
User Story:
As a User
I should be able to “show and hide the details of the events”
So that I have an option to expand or collapse the detail information of an event

Scenario 1: An event element is collapsed by default.
Given: Main page loads events
When: User selects their city
Then: User will receive a list of events related to that city
Scenario 2: User can expand an event to see its’ details.
Given: User has list of events to choose from
When: User selects desired event from list
Then: User should see detailed information about the event
Scenario 3: User can collapse an event to hide its’ details.
Given: Event details are hidden
When: User clicks on collapse key/button
Then: Event elements will be collapsed, returning user to collapsed event list


FEATURE 3: SPECIFY NUMBER OF EVENTS
User Story:
As a User
I should be able to “specify number of events I want to view”
So that I can choose the number of events I want to on screen at one time

Scenario 1: When user hasn’t specified a number, 32 is the default number.
Given: The default max number of returned events will be 32
When: User opens event page
Then: User will receive a max-default of 32 events
Scenario 2: User can change the number of events they want to see.
Given: User has option to update number of events to see
When: User inputs the number of events they want to view
Then: User receives the number of events they chose

FEATURE 4: USE THE APP WHEN OFFLINE
User Story:
As a User
I should be able to “use the app while offline”
So that I access events and details without internet connection/cellular coverage

Scenario 1: Show cached data when there is no internet connection.
Given: Show saved/cached data without internet/service
When: User opens app
Then: User will have access to stored data and information
Scenario 2: Show error when user changes the settings (i.e., City, Time, Details, etc.)
Given: User encounters error if offline
When: User attempts to update/change stored information
Then: User receives error message if stored settings are altered

FEATURE 5: DATA VISUALIZATION
User Story:
As a User
I should be able to “visualize the events data of cities”
So that I choose between cities and events based on my preferences
Scenario 1: Show a chart with the number of upcoming events in each city.
Given: Show visualized data of event types and cities
When: User clears all search settings and preferences
Then: User will ability to see all events in each city



