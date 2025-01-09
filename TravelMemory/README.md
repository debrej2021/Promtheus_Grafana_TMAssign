# Travel Memory

`.env` file to work with the backend after creating a database in mongodb: 

```
MONGO_URI='ENTER_YOUR_URL'
PORT=3001
```

Data format to be added: 

```json
{
    "tripName": "Incredible India",
    "startDateOfJourney": "19-03-2022",
    "endDateOfJourney": "27-03-2022",
    "nameOfHotels":"Hotel Namaste, Backpackers Club",
    "placesVisited":"Delhi, Kolkata, Chennai, Mumbai",
    "totalCost": 800000,
    "tripType": "leisure",
    "experience": "Lorem Ipsum, Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum,Lorem Ipsum, ",
    "image": "https://t3.ftcdn.net/jpg/03/04/85/26/360_F_304852693_nSOn9KvUgafgvZ6wM0CNaULYUa7xXBkA.jpg",
    "shortDescription":"India is a wonderful country with rich culture and good people.",
    "featured": true
}
```

Setup Details :- 

Promtheus & application deploment - 

I used my Ubuntu (OS) laptop to download Travel Memory application , deployed both frontend and backend , 
challenges faced -
CORS issue faced and wasnt connecting unless I made few changes to the conn.js files 
MongoDb installation and running of mongo server . I had to repari and reinstall mongo multiple times as connection was failing . 

I was able to deploy frontend , backend , install MongoDB and run the application which did work ( screen shots included ) , I also made few changes to the .env file which I have not included in the git checkin , can do so if required . 
since its a new machine , I had to install git , docker , node latest version as well which took some time . 

While Scrapping as well the config scripts had to be adjusted which took time in .
-----------------------------------------------------------------------------------------
Grafana - 

I then was able to configure Promethus with the help of docker for both frontend and backend 
Challenges Faced - 
I was also able to get the metrices but with localhost:9000/metrics but when I checked on the targets the backend server always seemed down because IP was not hard coded 
Each time I shut down my machine after working , to begin working I had to restart all and sometimes used to take some time for application restart it self , consumed a considerable amount of time 
I had to use IP of the machine for the backend "- targets: ['172.16.1.18:5000']" as it was otherwise not getting configured , perhaps some dynamic variable may work but I didnt find at this point . Pronthus ran on port 9000( screen shots included )
---------------------------------------------------------------------------------------------
Loki - 
I also then Grafana to run on port 3001 ( screen shots included )
I added promthus IP of machine :9000 as datasource ( screen shots added )
Challenges faced - 
When it was trying to connect prometheus with a variable and port it was again not working i.e Grafana was not able to connect to promtheus .  
I have created the loki folder and the config file but some reason I am not able to mount the loki aggregator and since I AM ON A TRAVEL DUE TO JOB CHANGE , UNABLE TO COMPLETE END TO END 

I have also added screen shots of the errors and successes to convey the challenges . 