# Python_Day4

#Activity 1: Traffic Light Control System
def traffic_light(signal):  
    if signal == "red":  
        return "Stop"  
    elif signal == "yellow":  
        return "Get Ready"  
    elif signal == "green":  
        return "Go"  
    else:  
        return "Invalid signal"  
  
signal = input("Enter the traffic signal (red, yellow, green): ")  
action = traffic_light(signal.lower())  
print(f"Signal: {signal} - Action: {action}")  

#Project: Fault-Detection System for Resistors
def detect_faults(resistances, min_resistance, max_resistance):  
    faulty_resistors = []  
    for index, resistance in enumerate(resistances):  
        if resistance < min_resistance:  
            faulty_resistors.append(f"Resistor {index + 1}: Below minimum resistance")  
        elif resistance > max_resistance:  
            faulty_resistors.append(f"Resistor {index + 1}: Above maximum resistance")  
    if not faulty_resistors:  
        return "All resistors are within the specified range."  
    else:  
        return "\n".join(faulty_resistors)  
  
resistances = [4.5, 10.2, 5.0, 3.8, 8.9]  
min_resistance = 4.0  
max_resistance = 10.0  
result = detect_faults(resistances, min_resistance, max_resistance)  
print(result) 
