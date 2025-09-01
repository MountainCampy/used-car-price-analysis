# used-car-price-analysis
This is my first project in data cleaning and manipulation, also visualization. So, please, expect no miracles.
This project has been done to see which features have the most effect on selling prices of cars.

a.Key notes that you should know:
1. Torque column was a real challenge to clean. Some of the rows had kgm's which I had to convert them to Nm's and then replace them with. You can see it in my code.
2. All missing values are excluded from data analysis. (221 values in "mileage", 221 values in "engine", 215 values in "max_power", 222 values in "torque", 221 values in "seats", Although "seats" column has been altered to fill it's NaN values with the column's mode so that it can be of integer type. After all, cars can't have 5.3 seats.)
3. Provided values for torque column are not associated with the raw torque of the related car. For example provided value for Maruti Swift Dzire VDI is actually it's torque at 2000rpm, not it's default.
4. Only the two primary columns, which are "km_driven" and "max_power", were taken into consideration.
5. Outliers from the "km_driven" and "max_power" columns have been excluded, since they were convincing enough to be an error value. For example a car had 1.5 million kilometers driven. That value was treated as typo and excluded.

b.To simply put, how did the process go?
1. A messy data set was cleaned ("Car details v3.csv") and then renamed ("cleaned_used_cars.csv"). Jupyter notebook for this, is named: "used_car_price_analysis.ipynb"
2. After cleaning, a second Jupyter notebook was made to visualize what factors affect the price. It is named: "what_affects_price.ipynb"

c.What can we infer from this project?
Correlation matrix says it all but let's dissect further.
1. "max_power" column, with 0.74 correlation, has the highest impact on the "selling_price" column. Which means higher the horse power of a car, higher the selling price of it.
2. "km_driven" column, with -0.22 correlation, has the lowest negative correlation. Which means lower the kilometers driven of a car, higher the selling price of it.
3. Graphs produced in the code are supporting these assesments.
4. Of course, other columns like, "engine", "mileage", etc. have impact on the selling price as well. But not as strong as max_power.
5. The "seats" column, with the lowest absolute correlation of 0.047, has almost no impact on the selling price, similar to the mileage column, which has an absolute correlation of 0.12. Therefore, neither is taken into consideration.
