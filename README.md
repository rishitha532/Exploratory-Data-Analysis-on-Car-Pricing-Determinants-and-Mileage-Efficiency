# Exploratory-Data-Analysis-on-Car-Pricing-Determinants-and-Mileage-Efficiency

# Dataset Description
The dataset comes from Kaggle's "CarDekho Used Car Data" dataset, containing 15,411 observations. It includes various attributes about used cars, such as the brand, model, vehicle age, and the selling price. The dataset provides a rich set of variables that can be analyzed for insights related to used car pricing trends.

# Source: 
- Kaggle - CarDekho Used Car Data

# Data Variables (Features):

1. brand: The manufacturer of the car (categorical).
2. model: The model of the car (categorical).
3. vehicle_age: The age of the car in years (integer).
4. km_driven: The number of kilometers driven (integer).
5. fuel_type: Type of fuel used by the car (categorical: Petrol/Diesel).
6. transmission_type: Transmission type (categorical: Manual/Automatic).
7. mileage: Mileage in kilometers per liter (float).
8. engine: Engine capacity in cc (integer).
9. seats: Number of seats in the car (integer).
10. selling_price: The selling price of the used car (integer).

# Interest in the Dataset
- I am interested in this dataset because it provides a comprehensive look at the used car market. By exploring the factors that influence the price of used cars, such as vehicle age, mileage, and fuel type, we can gain insights into market dynamics and the key variables that affect pricing decisions.

# Research Objectives:
- Analyze how vehicle age and kilometers driven affect mileage in used cars.
- Investigate how engine size and vehicle age impact price for automatic vs. manual cars.
- Explore how fuel type affects car mileage and price differences.

# Goals:
- Identify factors contributing to high mileage in used cars.
- Understand key drivers of price differences between transmission types.
- Provide insights on efficiency and value differences between Petrol and Diesel cars.


### EDA Hypotheses 

## 1. What factors contribute to high mileage in used cars?
- Reason for Interest: Mileage is a critical factor for buyers as it often reflects the car's usage and condition. Understanding what factors contribute to higher mileage (e.g., vehicle age, kilometers driven) can help identify which types of cars may be more likely to have higher mileage, providing valuable insights for buyers and sellers.

Univariate Analysis Insights:

- Age of Vehicle: The distribution shows that the majority of cars are clustered between 5 to 10 years old. Older cars tend to have slightly more variance in mileage performance, but age alone doesn't show significant insights into high mileage.

- Kilometers Driven: Cars with lower kilometers driven are more frequent, but the distribution is right-skewed, showing that cars with more kilometers driven are less common. Mileage might start to decrease with more kilometers driven.

- Fuel Type: Diesel cars appear less frequent but are known for providing higher mileage compared to petrol cars, which dominate the distribution.

- Engine Capacity: The distribution shows that most cars have engine capacities ranging from 1000cc to 1500cc. Larger engines may correlate with lower mileage.

- Mileage: The histogram shows a distribution of mileage with a central tendency between 15 to 20 kmpl, suggesting that most cars achieve moderate mileage.

- Transmission Type: Manual transmission cars are more frequent, and manual transmissions generally provide better mileage compared to automatic transmissions.

Bivariate Analysis Insights:

- Age of Vehicle vs Car Mileage: The scatterplot shows a weak negative correlation between age and mileage. Older cars generally have lower mileage, but the relationship isn't overly strong.

- Kilometers Driven vs Car Mileage: As expected, cars with more kilometers driven tend to have slightly lower mileage, though this is not a strong correlation. The mileage distribution remains fairly consistent for lower kilometers driven.

- Mileage by Fuel Type: Diesel cars, on average, offer higher mileage compared to petrol cars. This is a clear and strong differentiation between the two fuel types.

- Engine Capacity vs Car Mileage: There is a strong negative correlation between engine capacity and mileage. Cars with smaller engines have higher mileage, while larger engines (above 1500cc) are associated with lower mileage.

Multivariate Analysis Insights:

- Correlation Matrix: The heatmap shows moderate negative correlations between engine_capacity and car_mileage, as well as age_of_vehicle and car_mileage. Kilometers_driven has a weaker negative correlation with mileage, suggesting that engine size and age are more critical factors in determining fuel efficiency.

- FacetGrid: Mileage vs Age of Vehicle by Fuel Type: Across both fuel types, mileage decreases as cars age, but diesel cars maintain a higher average mileage compared to petrol cars over time.

- FacetGrid: Mileage vs Kilometers Driven by Fuel Type: The pattern is consistent across both fuel types—mileage decreases as kilometers driven increase, but diesel cars generally maintain higher mileage.

- FacetGrid: Mileage vs Engine Capacity by Fuel Type: The inverse relationship between engine capacity and mileage is evident across both fuel types. Diesel cars still outperform petrol cars in mileage even with larger engine sizes, but petrol cars with smaller engines have more variance.

Transmission Type vs Car Mileage by Fuel Type: Manual transmission cars generally provide higher mileage than automatic ones. This is true for both fuel types, but more pronounced for petrol cars.

From the analyses, it's clear that several factors contribute to high mileage in used cars:
- Fuel Type: Diesel cars consistently offer higher mileage compared to petrol cars across all analyses.
- Engine Capacity: Cars with smaller engine capacities (below 1500cc) are associated with higher mileage, especially petrol cars.
- Age of Vehicle: As cars get older, their mileage tends to decrease, although the relationship is not strong.
- Transmission Type: Manual transmissions tend to provide better mileage than automatic transmissions.

## 2. How does the combination of vehicle characteristics affect the selling price of automatic vs. manual transmission cars?
- Reason for Interest: Transmission type (automatic vs. manual) can significantly impact the selling price of a car. By analyzing the interactions between vehicle characteristics (e.g., engine size, vehicle age) for different transmission types, this question can reveal which features drive the value of each type, allowing for a deeper understanding of price differences and consumer preferences.

Univariate Analysis Insights:

- Transmission Type Distribution: The pie chart reveals that manual transmission vehicles dominate the dataset, making up a larger percentage than automatic transmission vehicles. This could influence the distribution of selling prices.

- Fuel Type Distribution: Petrol vehicles are more common than diesel and other fuel types. This could suggest that petrol cars are more readily available, and hence the pricing differences could be influenced by fuel types.

- Engine Capacity Distribution: Most vehicles have smaller engines, generally ranging between 1000cc and 1500cc, with fewer vehicles having larger engine capacities.

- Selling Price Distribution: The price distribution shows a wide range with a right-skewed pattern, indicating more affordable cars are common, but high-priced cars also exist, likely with better features or higher specifications.

- Car Mileage Distribution: The distribution of car mileage shows that many cars have mileage between 15 to 20 kmpl, typical for average-performance vehicles in this dataset.


Bivariate Analysis Insights:

- Selling Price by Transmission Type: Manual transmission cars generally have a lower price range compared to automatic transmission cars. This might reflect the higher cost and demand for automatic cars, especially for more recent models.

- Engine Capacity by Transmission Type: Vehicles with automatic transmissions tend to have slightly larger engine capacities compared to manual transmission vehicles, which could be one reason for the higher price of automatic cars.

- Car Mileage vs Price: There’s no strong relationship between car mileage and selling price, but cars with lower mileage tend to have slightly higher prices, likely because they are in better condition or newer.

- Fuel Type vs Price: Diesel vehicles tend to command a higher price compared to petrol vehicles. This could be due to their superior fuel efficiency and longer lifespan.
Engine Capacity vs Price:

- Vehicles with larger engines tend to have higher prices, which is consistent with the idea that larger engine vehicles offer more power or features that justify the cost.

Multivariate Analysis Insights:

- Pair Plot of Car Mileage, Engine Capacity, and Price: The pair plot reveals that price tends to increase with engine capacity, while car mileage has a moderate negative relationship with price. Gearbox type doesn't strongly impact car mileage but does affect pricing—automatic vehicles generally have higher prices.

- Box Plot: Fuel Type vs. Price by Gearbox Type: Diesel cars, whether manual or automatic, generally have higher prices than petrol cars. Among both petrol and diesel cars, automatic transmission vehicles have higher prices.

- FacetGrid: Car Mileage vs. Price by Fuel Type and Gearbox Type: For both petrol and diesel cars, automatic transmission vehicles tend to have a wider range of prices. Diesel automatic cars appear to have the highest price, likely due to a combination of superior mileage and higher demand for diesel-powered automatics.

- Heatmap of Correlation Matrix: The heatmap shows that engine capacity has a strong positive correlation with price, meaning larger engines result in higher prices. Car mileage, on the other hand, has a weaker, slightly negative correlation with price.

From the analyses, we can conclude that the combination of vehicle characteristics significantly influences the selling price of both automatic and manual transmission cars. Key insights include:

- Transmission Type: Automatic transmission vehicles generally command higher prices compared to manual transmission vehicles.
- Fuel Type: Diesel cars are priced higher than petrol cars, especially in combination with automatic transmission.
- Engine Capacity: Larger engines significantly increase the price of a vehicle, particularly for automatic transmission cars.
- Car Mileage: Although mileage plays a role, it is less critical than engine capacity and transmission type in determining price.

## 3. How does fuel type (Petrol vs. Diesel) influence car performance in terms of mileage and price?
- Reason for Interest: Fuel type is a major consideration for car buyers, especially when it comes to performance and cost. Investigating how petrol and diesel cars differ in terms of mileage and price can provide insights into which fuel types offer better efficiency and value, helping buyers make informed decisions based on their priorities.

Univariate Analysis Insights:

- Fuel Type Distribution: The pie chart shows that petrol cars dominate the dataset, making up a larger portion compared to diesel cars. This difference in representation could impact the average mileage and price trends observed in the data.

- Car Mileage Distribution: The histogram shows a spread of car mileage, with a higher frequency of cars achieving mileage between 15 to 20 kmpl. There’s a fairly normal distribution of mileage, indicating that most cars perform in a similar range.

- Price Distribution: The price distribution has a right skew, suggesting that more cars fall into the lower price range, with fewer cars in the higher price brackets. This could reflect the larger number of petrol cars, which tend to be more affordable compared to diesel cars.

Bivariate Analysis Insights:

- Car Mileage by Fuel Type: The box plot reveals a clear difference between fuel types. Diesel cars generally offer higher mileage compared to petrol cars, with less variance. Petrol cars have a wider range in mileage, but their median mileage is lower compared to diesel.

- Price by Fuel Type: The violin plot shows that diesel cars tend to have higher prices, while petrol cars exhibit a wider price range. Diesel cars appear to have fewer outliers and a more concentrated distribution of higher prices. This likely reflects the increased fuel efficiency and durability of diesel engines.


Multivariate Analysis Insights:
- Pairplot: Fuel Type, Car Mileage, and Price: The pairplot shows clear separation between petrol and diesel cars when examining mileage and price together. Diesel cars tend to cluster at higher mileage and price points, while petrol cars are spread more evenly across lower price ranges with variable mileage performance.

- FacetGrid: Price vs. Car Mileage by Fuel Type: The FacetGrid highlights that while diesel cars achieve higher mileage, they are also priced higher than petrol cars. Petrol cars show more variance in mileage, but generally cluster around lower prices and lower mileage performance. Diesel cars demonstrate a more linear relationship between higher mileage and higher price.

Insights from PCA Analysis:
- Explained Variance: Principal Component 1 explains 81.63% of the variance, while Principal Component 2 explains 18.37%, meaning these two components capture almost all the information related to mileage and price.
- Diesel Cars: Diesel cars (green) are closely clustered, indicating consistent mileage and pricing. They tend to offer better fuel efficiency and are priced higher with less variability compared to petrol cars.
- Petrol Cars: Petrol cars (blue) are more widely spread, showing greater variability in both mileage and price. Petrol cars cater to a broader market, with a mix of lower-priced, lower-mileage vehicles and some higher-end models.
- Other Fuel Types: LPG (purple) and CNG (red) are few in number and scattered, indicating less consistency and less influence on the overall market compared to petrol and diesel vehicles.

The analysis highlights the following key insights regarding the influence of fuel type on car performance:

- Diesel cars consistently outperform petrol cars in terms of mileage. Diesel cars offer better fuel efficiency, leading to higher mileage values, with a more concentrated distribution of performance.
- Diesel cars are priced higher than petrol cars. This is likely due to their better mileage, fuel efficiency, and durability, which makes them more desirable and justifies the higher price.
- Petrol cars show a wider variance in both mileage and price, suggesting that there are more affordable petrol cars on the market, but their performance is not as consistent as diesel vehic
  
PCA Analysis insights:
- Diesel cars provide better and more consistent mileage and are generally priced higher, making them more efficient and valuable in the used car market.
- Petrol cars display greater variation in both mileage and price, serving a wider market with more affordable options but lower overall performance in fuel efficiency.
- The PCA confirms that mileage and price are key differentiators between these fuel types, with diesel cars standing out for their superior performance and pricing stability.les.





