## Nadiia Ivanitska

### Trainee/ Junior FrontEnd Developer

---

## Contact Information::

**E-mail:** nadie.ivanitska@gmail.com
**Telegram:** @nadieivy
[**LinkedIn**](https://www.linkedin.com/in/nadieivanitska/)
[**GitHub**](https://github.com/NadieIvi)

---

## About Me

I am currently actively studying Front End (HTML, CSS, JavaScript), so I am looking for an internship. I am confident that the experience I gained while working at Ikea, De Longi, will be useful and effective in the new field of work.

---

## Skills and Proficiency:

- HTML5, CSS3
- JavaScript Basics
- React Basics
- Git, GitHub
- VS Code

---

## Code Example:

Weather Forecast component from the project **Weather App** [Project link](https://roaring-biscochitos-e8e105.netlify.app/) [Project Github link](https://github.com/NadieIvi/react-weather-final)

```javascript
//
import React, { useState, useEffect } from "react";
import "./WeatherForecast.css";
import axios from "axios";
import WeatherForecastDay from "./WeatherForecastDay";

export default function WeatherForecast(props) {
  let [loaded, setLoaded] = useState(false);
  let [forecast, setForecast] = useState(null);

  function handleResponse(response) {
    setForecast(response.data.daily);
    setLoaded(true);
  }

  useEffect(() => {
    setLoaded(false);
  }, [props.city]);

  if (loaded) {
    return (
      <div className="WeatherForecast">
        <div className="row">
          {forecast.map(function (dailyForecast, index) {
            if ((index < 6) & (index > 0)) {
              return (
                <div className="col" key={index}>
                  <WeatherForecastDay data={dailyForecast} />
                </div>
              );
            } else {
              return null;
            }
          })}
        </div>
      </div>
    );
  } else {
    const apiKey = "3adcf3ct4b5e5390baeb304756b2oad1";
    let apiUrl = `https://api.shecodes.io/weather/v1/forecast?query=${props.city}&key=${apiKey}&units=metric`;
    axios.get(apiUrl).then(handleResponse);

    return null;
  }
}
```

---

## Certifications

- [**SheCodes Basics:**] (https://www.shecodes.io/certificates/f2663c34db56b20f21e0ab5a706d847e) learned basics of HTML5, CSS, JavaScript
- [**SheCodes Plus:**] (https://www.shecodes.io/certificates/e9535ae74dda4b36971b84d6068e3cf7) learned basics of Bootstrap, Git, API
- [**SheCodes Responsive:**] (https://www.shecodes.io/certificates/ad9ed577de4108483c7c1bc4dcb38a97) learned Responsiveness
- [**SheCodes React:**](https://www.shecodes.io/certificates/d1e6f381381c6667c0f7afbefbb3342d) learned basics of React

---

## Languages

- English - UpperIntermediate
- Ukrainien - Native
