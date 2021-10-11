# holy-hour

A site to compare the amount of bars and the amout of churches a town or city has, within a 5 mile radius.
See review count as well as location rating, and get currently updated weather for that locatoin.



## Built With

* [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
* [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
* [Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

* [Jquery](https://jquery.com/)
* [JqueryUI](https://jqueryui.com/)

* [VEX](https://github.com/HubSpot/vex)

* [MaterializeCSS](https://materializecss.com/badges.html)
* [FontAwesome](https://fontawesome.com/)

* [ipify](https://www.ipify.org/)
* [ip-api](https://ip-api.com/)
* [YelpFusionAPI](https://www.yelp.com/fusion)
* [Open_Weather_Map_One_Call_API](https://openweathermap.org/api/one-call-api)





## Deployed Link



* [See Live Site](https://divinemayura.github.io/holy-hour/)

![landing](images/landing.jpg)
![main](images/main.jpg)

## Authors


* **Erik Gustuson**

- [Link to Portfolio Site](https://erikgustuson.github.io/basic-portfolio/)
- [Link to Github](https://github.com/ErikGustuson)
- [Link to LinkedIn](https://www.linkedin.com/in/erik-gustuson/)

* **May Faucher** 

- [Link to Portfolio Site](https://divinemayura.github.io/)
- [Link to Github](https://github.com/DivineMayura)
- [Link to LinkedIn](https://www.linkedin.com/in/mayfaucher)

* **Mehdi Safari**

- [Link to Portfolio Site](https://mehdisafari77.github.io/Basic-Bio/)
- [Link to Github](https://github.com/mehdisafari77)
- [Link to LinkedIn](https://www.linkedin.com/in/mehdi-safari-992799142/)


## License

This project is licensed under the MIT License 

## Code:
```
$(".dropdown-trigger").dropdown();

var allCities = JSON.parse(localStorage.getItem("saved-city")) || [];

function saveCity() {
  allCities.unshift(searchValue);
  showCity(searchValue);
  localStorage.setItem("saved-city", JSON.stringify(allCities));
}

function showCity() {
  if (allCities.length > 5) {
    allCities.pop();
  }
  console.log(allCities);
  document.getElementById("first-city").innerHTML = allCities[0];
  document.getElementById("second-city").innerHTML = allCities[1];
  document.getElementById("third-city").innerHTML = allCities[2];
  document.getElementById("fourth-city").innerHTML = allCities[3];
  document.getElementById("fifth-city").innerHTML = allCities[4];
}

var firstCityClick = document.getElementById("first-city");
var secondCityClick = document.getElementById("second-city");
var thirdCityClick = document.getElementById("third-city");
var fourthCityClick = document.getElementById("fourth-city");
var fifthCityClick = document.getElementById("fifth-city");

firstCityClick.addEventListener("click", function (event) {
  searchValue = allCities[0];
  console.log(searchValue);
  getYelpChurches(searchValue);
  getYelpBars(searchValue);
});
```
![alt text](images/code2.jpg)


