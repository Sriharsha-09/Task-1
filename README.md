import matplotlib.pyplot as plt
import numpy as np

# 1. Pie Chart: 2015 U.S. GDP
def plot_pie_chart():
    labels = ['Manufacturing', 'Finance, Insurance, Real Estate, Rental, and Leasing',
              'Arts, Entertainment, Recreation, Accommodation, and Food Services', 'Other']
    sizes = [19, 18, 4, 59]  # Percent contributions
    colors = ['gold', 'lightblue', 'lightcoral', 'lightgreen']
    explode = (0.1, 0, 0, 0)  # Explode the first slice

    plt.figure(figsize=(8, 6))
    plt.pie(sizes, explode=explode, labels=labels, colors=colors, autopct='%1.1f%%', startangle=90)
    plt.title('2015 U.S. GDP (in millions of dollars)')
    plt.axis('equal')  # Equal aspect ratio ensures that pie is drawn as a circle
    plt.show()

# 2. Bar Graph: 2015 GDP by Industry
def plot_bar_graph():
    industries = ['All Industries', 'Manufacturing', 'Finance, Insurance, Real Estate', 
                  'Arts, Entertainment, Recreation', 'Other']
    values = [31.397023, 5.829554, 5.597018, 1.283813, 18.686638]  # GDP in trillions

    plt.figure(figsize=(10, 6))
    plt.bar(industries, values, color='skyblue')
    plt.xlabel('Industry')
    plt.ylabel('GDP (in trillions of dollars)')
    plt.title('2015 GDP by Industry')
    plt.xticks(rotation=45, ha='right')
    plt.tight_layout()
    plt.show()

# 3. Line Graph: Yearly GDP Over Time
def plot_line_graph():
    years = [1947, 1950, 1953, 1956, 1959, 1962, 1965, 1968, 1971, 1974, 1977, 1980, 
             1983, 1986, 1989, 1992, 1995, 1998, 2001, 2004, 2007, 2010, 2013]
    gdp = [0, 5, 10, 15, 20, 25, 30, 35, 30, 25, 20, 15, 10, 5, 0, 0, 5, 10, 15, 20, 25, 30, 35]

    plt.figure(figsize=(10, 6))
    plt.plot(years, gdp, marker='o', linestyle='-', color='green')
    plt.xlabel('Year')
    plt.ylabel('GDP (in trillions of dollars)')
    plt.title('Yearly Total GDP Over Time')
    plt.grid(True)
    plt.show()

# 4. Scatter Plot: Plotting x and y from a Table
def plot_scatter():
    x = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8])
    y = np.array([0, 3, 6, 9, 12, 15, 18, 21, 24])

    plt.figure(figsize=(8, 6))
    plt.scatter(x, y, color='blue', label='Data Points')
    plt.plot(x, y, linestyle='-', color='orange', label='Linear Fit')
    plt.xlabel('x-axis')
    plt.ylabel('y-axis')
    plt.title('Scatter Plot with Linear Fit')
    plt.legend()
    plt.grid(True)
    plt.show()

# 5. Example Computation: Family Budget
def compute_family_transportation_expense():
    total_income = 31000
    transportation_percent = 15 / 100
    transportation_expense = total_income * transportation_percent
    print(f"Yearly transportation expense: ${transportation_expense:.2f}")

# 6. Custom Bar Graph Example (Urban Affairs Life Expectancy)
def plot_custom_bar_graph():
    categories = ['Men (1925)', 'Men (2025)', 'Women (1925)', 'Women (2025)']
    life_expectancy = [55, 75, 60, 85]  # Hypothetical data

    plt.figure(figsize=(8, 6))
    plt.bar(categories, life_expectancy, color=['blue', 'blue', 'pink', 'pink'])
    plt.xlabel('Category')
    plt.ylabel('Life Expectancy (years)')
    plt.title('Life Expectancy Changes Over Time')
    plt.show()

# Example Usage
if __name__ == "__main__":
    print("1. Pie Chart: 2015 U.S. GDP")
    plot_pie_chart()

    print("2. Bar Graph: 2015 GDP by Industry")
    plot_bar_graph()

    print("3. Line Graph: Yearly GDP Over Time")
    plot_line_graph()

    print("4. Scatter Plot: x vs. y")
    plot_scatter()

    print("5. Family Budget Computation")
    compute_family_transportation_expense()

    print("6. Custom Bar Graph: Urban Affairs Life Expectancy")
    plot_custom_bar_graph()
