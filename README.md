# used-car-price-analysis
This is my first project in data cleaning and manipulation, also visualization. So, please, expect no miracles.

1. Torque column was a real challenge to clean. Some of the rows had kgm's which I had to convert them to Nm's and then replace them with. You can see it in my code.
2. All missing values are excluded from data analysis. (221 values in "mileage", 221 values in "engine", 215 values in "max_power", 222 values in "torque", 221 values in "seats", Although "seats" column has been altered to fill it's NaN values with the column's mode so that it can be of integer type. After all, cars can't have 5.3 seats.)
3. Provided values for torque column are not associated with the raw torque of the related car. For example provided value for Maruti Swift Dzire VDI is actually it's torque at 2000rpm, not it's default. 
