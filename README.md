# meet

A serverless, Progressive Web Application (PWA) built with React (using a test-driven development (TDD) technique) using the Google Calendar API to fetch upcoming events. Features have been broken down into 6 parts, each defined below and coupled with user scenarios of operation.

The project dependencies include JavaScript and AWS, with the key technologies including React.


**Feature 1: Filter Events by City**

As a user,
I should be able to filter events by city
So that I can see a list of events taking place in that city.

	SCENARIO 1: When user hasn’t searched for a specific city, show upcoming events from all cities.
	Given user hasn’t searched for any city;
	When the user opens the app;
	Then the user should see a list of upcoming events.
 
	SCENARIO 2: User should see a list of suggestions when they search for a city.
	Given the main page is open;
	When user starts typing in the city textbox;
	Then the user should receive a list of cities (suggestions) that match what they’ve typed.

 	SCENARIO 3: User can select a city from the suggested list.
	Given user was typing “Berlin” in the city textbox AND the list of suggested cities is showing;
	When the user selects a city (e.g., “Berlin, Germany”) from the list;
	Then their city should be changed to that city (i.e., “Berlin, Germany”) AND the user should receive a list of upcoming events in that city.


**Feature 2: Show/Hide an Event's Details**

As a user,
I would like to be able to show/hide event details
so that I can see more/less information about an event.

	Scenario 1: An event element is collapsed by default.
	Given the user has a list of events;
 	When the events first appear;
  	Then the event are displayed by title only.
 	
 
	Scenario 2: User can expand an event to see details.
 	Given the user a list of events;
  	When the user selects an event;
   	Then the expanded details of the event are displayed.
 
	Scenario 3: User can collapse an event to hide details.
 	Given the user is content with the viewing the details of an event;
  	When the user selects to close the details;
   	Then the details of the event will no longer be displayed.
    


**Feature 3: Specify Number of Events**

As a user,
I would like to be able to specify the number of events I want to view in the app
so that I can see more or fewer events in the events list at once.

	Scenario 1: When user hasn’t specified a number, 32 events are shown by default.
 	Given the user has not specified a number of events to view;
  	When events are listed to the user;
   	Then 32 events will be shown.
 
	Scenario 2: User can change the number of events displayed.
 	Given the user wishes to choose the amount of events that are displayed;
  	When the user selects their desired amount of events to be listed;
   	Then this amount will be displayed.


**Feature 4: Use the App When Offline**

As a user,
I would like to be able to use the app when offline
so that I can see the events I viewed the last time I was online.

	Scenario 1: Show cached data when there’s no internet connection.
 	Given the user is no longer online;
  	When the user wants to view events previously viewed;
 	Then display these events from cached data.
  
	Scenario 2: Show error when user changes search settings (city, number of events).
 	Given the user is off-line;
  	When the user attempts to amend their search settings;
	Then display an error message informing user they cannot amend settings when off-line.
 
 
**Feature 5: Add an App Shortcut to the Home Screen**

As a user,
I would like to be able to add the app shortcut to my home screen
so that I can open the app faster.

	Scenario 1: User can install the meet app as a shortcut on their device home screen.
	Given the user wants the app to open faster;
 	When the user selects the option install the app;
  	Then add a shortcut to their home screen.
 
**Feature 6: Display Charts Visualizing Event Details**

As a user,
I would like to be able to see a chart showing the upcoming events in each city
so that I know what events are organized in which city.

	Scenario 1: Show a chart with the number of upcoming events in each city
	Given the user wants a visual representation of the data;
 	When the user chooses a city;
  	Then display the information in chart form

	
