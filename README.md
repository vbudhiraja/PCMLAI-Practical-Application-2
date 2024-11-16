# PCMLAI-Practical-Application-2



 # Analysis based on the specified rubric

### Data cleaning steps included
- **Removing irrelevant columns** (`id`, `VIN`, `region`, `state`).
- **Handling missing values**: Imputed values for essential categorical columns like `condition` and `manufacturer`, and removed rows missing critical values like `price`, `year`, or `odometer`.
- **Encoding** categorical features via one-hot encoding for modeling.

### Removed outliers
- **z-score method**: value >3
- **IQR Treatment**: (`price`, `odometer`, `year`).

### Used Correlation Matrix
- **Price vs. Year**: There’s a positive correlation between `price` and `year`, as newer vehicles generally retain higher value.
- **Price vs. Odometer**: Higher odometer readings are associated with lower prices, as higher mileage indicates more wear.
- **Manufacturer and Condition**: Brands and vehicle condition (e.g., “like new”) can significantly impact value, with well-known brands and good condition generally attracting higher prices.

### Used Regression Techniques to see features influence on the price
- **Applied Linear Regression along with Ride and Lasso**  
- **Both Ridge and Lasso models** performed similarly in terms of RMSE, making them comparable in predictive power.

The top factors affecting price, based on the regression coefficients, are as follows:

1. **fuel_electric**: Electric fuel type negatively impacts price significantly.
2. **manufacturer_tesla**: Tesla as a manufacturer has a strong positive influence on price.
3. **fuel_gas**: Gasoline-powered vehicles have a noticeable negative impact on price.
4. **cylinders_12**: Vehicles with 12 cylinders strongly increase the price, likely reflecting high performance.
5. **manufacturer_porsche**: Porsche vehicles contribute significantly to a higher price.
6. **manufacturer_fiat**: Fiat as a manufacturer lowers the price.
7. cylinders_3**: Vehicles with 3 cylinders strongly decrease the price, likely reflecting low performance.
8. **Condition (like new)**: Vehicles in "like new" condition add the most to price, suggesting that excellent condition is highly valued.
9. **Condition (good)**: Vehicles in "good" condition also positively impact price, though less than "like new."
10. **Odometer**: Higher mileage slightly decreases price, though its effect here is relatively small compared to other features.



