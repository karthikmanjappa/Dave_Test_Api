In this assignment, I tested both an API and a website. For the API part, I used the public Reqres API to check if it returns the right responses, handles errors properly, and creates new users. I also set up a small load test to see how it works with multiple users.
For the website part, I used Selenium to test the DaveAI website. I checked if the site loads correctly, the logo and buttons are visible, and navigation works as expected. The tests include setup and cleanup steps so the browser opens and closes properly.

API and Website Testing Assignment :
Project Overview :
This project contains automated tests for:
1. Reqres API  – validating responses, error handling, and user creation.
2. DaveAI Website – verifying title, logo, navigation, and button presence.
3. Optional Load Test – using Locust to simulate 5–10 users.

## Run API tests:
pytest tests/api_tests.py -v
## Run UI tests:
python -m unittest tests/ui_tests.py
## Brief Explanation of Test Design Choices
For the API tests, I chose to cover the most important cases: checking if the API gives a successful response, making sure the data in the response is correct, handling errors properly (like when a user is not found), and testing user creation with valid data. These cover both normal usage and error scenarios.
For the website tests, I focused on basic but critical checks: whether the site loads with the right title, if the logo and key buttons are visible, if navigation works correctly, and if important elements are present on the page. These tests ensure that the website is working as expected from a user’s point of view.
For the load test, I kept it simple by simulating 2–4 users making requests at the same time, while limiting total calls to avoid overloading the public API. This helps see how the system performs under small user loads.
Test Design Choices

## API Tests check:
#### Successful response (200 OK).
#### Correct data in response.
#### Error handling (404).
#### User creation with POST.

## UI Tests validate:
#### Page load with correct title.
#### Logo visibility.
#### Navigation links work.
#### Important buttons exist.
#### Locust used to simulate small load (5–10 concurrent users, ≤100 requests/day).
