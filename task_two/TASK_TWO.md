# Task Two - What’s the weather like there?

Your team is getting ready for the holiday season to travel abroad and need a new tool to help them check the weather at cities around the world. You have been tasked with creating a simple API that lets the team check the weather in a city using a provided, open source, third party API to retrieve weather data.

This question is open ended so you may make any extensions you like, but please make sure that you first satisfy the initial brief and specification, and also make sure to clearly state any assumptions you make.

Please don't spend more than 3 hours on this task.

## Technical Specification

For this task, you should use the Open Weather Map API. The documentation for the free plan for the specific API you should use is accessible at [Open Weather Map](https://openweathermap.org/current).

This API lets you make a requests for current weather data for one location, by providing a city name. It also has data for approximately 200,000 cities. You can sign up for a free account to receive an API key to use and test the API. However, you may have to wait a few hours for them to activate your account so that the keys work. If you are having difficulty creating your own account, reach out to us and we can provide you with sign in details for an account registered to jobs@behaviourlab.com.

## Requirements

Short summary: Set up a Django API that queries the provided third party weather API, stores the data in a PostgreSQL table / Django model. There should be an endpoint to look up data from the table. If you’re looking for a city that’s not in the table, you have to get this information from the third party and return it. Otherwise, you have to return the data directly from the table.

In more detail this means:

1. The user must be able to enter the name of a city on your API and receive information about the temperature in degrees Celsius for that city.
2. Each time a user makes a request to your API, it should check if that data is stored in your PostgreSQL table or Django Model.
3. If a request is made to your API for a city where the weather data was _not requested before_, OR previously requested _more than 4 hours in the past_, you should fetch the weather data from the third party OpenWeatherMap API and store the data in your PostgreSQL table or Django model. Once the data is stored in your database, you should return this data to the user.
4. If a request is made to your API for a city where the weather data was previously _requested 4 hours or less in the past_, you should return the response directly from the PostgreSQL table or Django Model.

Submit a README alongside your submission, with instructions on how to run the project and a brief overview of the technical decisions made. Please provide as much detail as possible in your answer - technical and otherwise.

You have full freedom to design the API and the database so long as it satisfies these requirements.

## Sample API Request:

The following is a sample API request to retrieve weather data from the API, where the `{CITY}` can be replaced with the name of a city, and the `{API_KEY}` can be replaced with your API key.

```
https://api.openweathermap.org/data/2.5/weather?q={CITY}&appid={API_KEY}
```
