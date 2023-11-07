# Home Assistant automations
## NodeRed Flows for Sunsynk 
### Adjust SOC for rainy days
I run this once a day to adjust the timer for the morning shift so that it increases the grid charge when it is going to be rainy in the morning. 

-Edit the "average cloud cover" function node to change the hours to sample 
-change the values in the "Increase SOC" and "Decrease SOC" nodes to adjust the SOC setting as well as specify which timer slot to adjust
-change the "CloudForecast" node to adjust the thresholds, currently set to 50% average. 
![Adjust SOC for rainy days](https://github.com/jimilutz/HA/assets/89185715/0e5ae76d-e67e-4a0f-9834-893498bba773)

### Geyser control
I have a 4kW and a 2kW geyser that I run mostly off solar power when available.
A flow to:
- Run the geyser once in the morning and once at night if Loadshedding is not in effect
- Run the geysers (2) during sunshine hours when the battery is agbove 50%. I toggle to the secondary geyser which is a smaller volume for a brief stint in the middle of the day.
![Geyser control](https://github.com/jimilutz/HA/assets/89185715/5adead01-923c-4406-a6dd-e5aed9a77255)

## Dependencies
I use the Big Timer from https://tech.scargill.net/big-timer/ 
