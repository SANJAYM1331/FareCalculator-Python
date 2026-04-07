# FareCalc — CityCab Travel Optimizer

A simple Python script that calculates ride fares based on distance, vehicle type, and time of day.

---

## What It Does

- Takes user input: distance (km), vehicle type, and hour of day
- Calculates a base fare using per-km rates
- Applies a **1.5x surge multiplier** during peak hours (5 PM – 8 PM)
- Prints a formatted price receipt
- Handles invalid vehicle type input gracefully

---

## Vehicle Rates

| Vehicle Type | Rate per KM |
|--------------|-------------|
| Economy      | ₹10         |
| Premium      | ₹18         |
| SUV          | ₹25         |

---

## Surge Pricing

| Hour of Day     | Multiplier |
|-----------------|------------|
| 0 – 16, 21 – 23 | 1.0x (No Surge) |
| 17 – 20         | 1.5x (Peak Hours) |

---

## How to Run

Make sure Python 3 is installed.

```bash
python farecalc.py
```

You will be prompted to enter:
1. Distance in KM
2. Vehicle type (`Economy`, `Premium`, or `SUV`)
3. Vehicle type (`Economy`, `Premium`, or `SUV`)
4. Hour of day (0–23)

---

## Sample Output

```
       Welcome to CityCab FareCalc      
Enter distance in KM        : 12
Available vehicle types: Economy, Premium, SUV
Enter vehicle type          : Premium
Enter hour of day (0-23)    : 18

           Price Receipt             
 Vehicle Type     : Premium
 Distance         : 12.0 km
 Rate per KM      : ₹18
 Base Fare        : ₹216.00
 Surge Pricing    : 1.5x (Peak Hours!)
 Total Fare       : ₹324.00
```

---

## Error Handling

If an unsupported vehicle type is entered, the script displays:

```
Error: Service Not Available for vehicle type: <input>
Please choose from: Economy, Premium, SUV
```

---

## Project Structure

```
farecalc.py     # Main script
README.md       # Project documentation
```

---

## Requirements

- Python 3.x
- No external libraries needed
