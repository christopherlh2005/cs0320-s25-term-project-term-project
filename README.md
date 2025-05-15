# CanGo Details

Sprint 5.1: Front-End Map 
Sprint 5.2: Mapping Data
Group Members: Chris Ho (clho) and Doren Hsiao-Wecksler (dxhw)
Estimated Time: 6 hours (5.1) and 10 hours (5.2)
Github Link: https://github.com/cs0320-s25/maps-chris-doren.git

# Design Choices

5.1: 
At the high-level, we mocked pre-exisiting pins that are green in color. New pins added in by the current user are in red. Hovering over the pins reveals the user, which is anonymized to prevent any type of retaliation by landlords.

The relationship between the classes is that Mapbox.tsx controls the logic of the front-end map while App.tsx controls authentication via clerk and some of the front end designs.

5.2: At a high level, you can drop pins from a variety of accounts, and it will sync across any account. Additionally, we set up an API endpoint (see GetRedliningHandler) that returns the JSON, limiting coordinates to the redlined areas. Lastly, we implemented a search functionality that highlights specific pins that match a certain descriptor. 

# Errors/Bugs

n/a

# Tests

5.1:
 vd pins work
* creating pins works
* pins persist on reload
* clearing pins succeeds
* different users can see each others' pins
* different users cannot delete each others' pins

5.2: 
* mocked data to test api call for user story 4 (GetRedliningHandler)
* pins persist across accounts
* search is handled correctly


# How to

To run the Playwright tests, you can type "cd client" in the terminal and run "npx run test". 
To run the APITest in the backend, you can run the test by clicking the play button on the file.


# Collaboration

* gwang71 - discussed codegen testing 
* avzeng - worked with in collab section (how to persist storage)
* https://www.baeldung.com/java-check-string-number checking strings to be numbers in AddPinHandler

* OpenAI. (2025). ChatGPT (GPT-4o) [Large language model]. https://chat.openai.com/chat
    * Help setting up interval for making database call (so we don't spam firebase) in MapBox

* OpenAI. (2025). ChatGPT (GPT-4o) [Large language model]. https://chat.openai.com/chat
    * Create a way to print out the number of coordinates that meet the criteria for a certain location range. 

_(state all of your sources of collaboration past your project partner. Please refer to the course's collaboration policy for any further questions.)_
