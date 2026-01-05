# Linear regression using direct values (no dataset)

x = [800, 1000, 1200, 1500, 1800]
y = [20, 25, 30, 38, 45]

n = len(x)

sum_x = sum(x)
sum_y = sum(y)
sum_xy = sum(x * y for x, y in zip(x, y))
sum_x2 = sum(x * x for x in x)

m = (n * sum_xy - sum_x * sum_y) / (n * sum_x2 - sum_x ** 2)
c = (sum_y - m * sum_x) / n

print("Slope (m):", m)
print("Intercept (c):", c)

new_house_size = 1600
predicted_value = m * new_house_size + c

print("Predicted value for house size", new_house_size, ":", predicted_value)
