# determination-of-sampling-point-of-a-chemical-sample
program in Python that determines the sampling point of a chemical sample using a structured algorithm
def determine_sampling_point(chemical_properties):

    """

    Determines the sampling point of a chemical sample based on its properties.

    

    Arguments:

    chemical_properties -- A dictionary containing the properties of the chemical sample.

                           Example: {'temperature': 25, 'pressure': 1.2, 'pH': 7.5}

    

    Returns:

    sampling_point -- The recommended sampling point for the chemical sample.

    """

    # Determine the sampling point based on chemical properties

    if chemical_properties['temperature'] > 50:

        sampling_point = 'High-temperature zone'

    elif chemical_properties['pressure'] > 1.5:

        sampling_point = 'High-pressure zone'

    elif chemical_properties['pH'] < 6 or chemical_properties['pH'] > 8:

        sampling_point = 'pH-sensitive zone'

    else:

        sampling_point = 'Standard sampling point'

    

    return sampling_point

def main():

    # Get user input for chemical properties

    temperature = float(input("Enter the temperature of the chemical sample: "))

    pressure = float(input("Enter the pressure of the chemical sample: "))

    pH = float(input("Enter the pH value of the chemical sample: "))

    

    # Create a dictionary of chemical properties

    chemical_properties = {

        'temperature': temperature,

        'pressure': pressure,

        'pH': pH

    }

    

    # Determine the sampling point

    sampling_point = determine_sampling_point(chemical_properties)

    

    # Print the result

    print("Recommended Sampling Point: ", sampling_point)

if __name__ == '__main__':

    main()
    
In this project, the determine_sampling_point() function takes a dictionary called chemical_properties as input. This dictionary contains the properties of the chemical sample, such as temperature, pressure, and pH.

Based on the values of these properties, the function uses a series of conditional statements to determine the recommended sampling point for the chemical sample. If the temperature is greater than 50, it suggests a "High-temperature zone" sampling point. If the pressure is greater than 1.5, it suggests a "High-pressure zone" sampling point. If the pH is less than 6 or greater than 8, it suggests a "pH-sensitive zone" sampling point. Otherwise, it suggests a "Standard sampling point".

In the main() function, the user is prompted to enter the values for temperature, pressure, and pH. A dictionary called chemical_properties is created using these values. The determine_sampling_point() function is then called with chemical_properties as an argument, and the recommended sampling point is printed.

You can customize the program by adding more chemical properties or modifying the conditional


