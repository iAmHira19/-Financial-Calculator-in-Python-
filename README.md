```markdown
# Financial Calculator

This project provides a comprehensive financial calculator implemented in Python using Google Colaboratory. The calculator can perform various financial calculations based on user input, including:

- **Annuity Calculation**: With monthly or continuous growth
- **Monthly Mortgage Payment**: Calculation based on principal, annual interest rate, and number of months
- **Retirement Investment Balance**: Estimate based on initial investment, annual rate of return, and years
- **Time to Double Investment**: Given the annual rate
- **Logarithmic Equation Solver**: Solve equations of the form \( \log_{base}(result) \)
- **Scientific Notation Converter**: Convert to and from scientific notation

## Getting Started

To use the financial calculator, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/financial-calculator-python.git
   cd financial-calculator-python
   ```

2. **Open the Project in Google Colaboratory**:
   - Go to [Google Colaboratory](https://colab.research.google.com/)
   - Open the `.ipynb` file from your cloned repository or upload the notebook if you're starting from scratch.

3. **Run the Code**:
   - Execute the code cells in Google Colaboratory.
   - Follow the prompts in the interactive console to perform calculations.

## Features

### 1. Annuity Calculation
Calculate the annuity with monthly or continuous growth. 
- **Formula**:
  - Monthly: `principal * (monthly_rate / (1 - (1 + monthly_rate) ** -periods))`
  - Continuous: `principal * np.exp(rate * periods)`

### 2. Monthly Mortgage Payment
Calculate the monthly mortgage payment based on the loan principal, annual interest rate, and number of months.
- **Formula**:
  - ` (principal * monthly_rate) / (1 - (1 + monthly_rate) ** -months)`

### 3. Estimate Retirement Balance
Estimate the retirement investment balance based on initial investment, annual rate of return, and years.
- **Formula**:
  - `principal * (1 + annual_rate) ** years`

### 4. Time to Double Investment
Determine how long it takes for an investment to double given the annual rate.
- **Formula**:
  - `np.log(2) / np.log(1 + rate)`

### 5. Solve Logarithmic Equations
Solve equations of the form \( \log_{base}(result) \).
- **Formula**:
  - `sp.log(result, base)`

### 6. Scientific Notation Converter
Convert numbers to and from scientific notation.
- **Conversion to Scientific Notation**:
  - `"{:.2e}".format(value)`
- **Conversion from Scientific Notation**:
  - `float(sci_notation)`

## Example Code

Below is a snippet of how the calculator operates:

```python
def main():
    while True:
        display_menu()
        choice = input("Enter the number of your choice: ")
        
        if choice == '1':
            principal = float(input("Enter the principal amount: "))
            rate = float(input("Enter the annual rate (as a decimal): "))
            periods = int(input("Enter the number of periods (months for monthly growth): "))
            growth_type = input("Enter growth type ('monthly' or 'continuous'): ")
            print(f"Result: {calculate_annuity(principal, rate, periods, growth_type)}")
        
        # Additional options...
        
        elif choice == '7':
            print("Exiting the calculator.")
            break
        
        else:
            print("Invalid choice. Please try again.")
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [NumPy](https://numpy.org/)
- [SymPy](https://www.sympy.org/)

## Contact

For questions or suggestions, please reach out to [Hira Amanat email](mailto:hiraamanat99@gmail.com.com).
