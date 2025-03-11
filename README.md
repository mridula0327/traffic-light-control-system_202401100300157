# traffic-light-control-system_202401100300157
Traffic Light Control System
Project Overview
The Traffic Light Control System simulates the behavior of traffic lights (Red, Yellow, and Green) at an intersection. This system provides a simple interface for controlling traffic lights manually, allowing users to simulate real-time traffic light cycles. The project is implemented in Python, with an interactive console-based interface for user input.

Features
Simulates the operation of a traffic light with Red, Yellow, and Green lights.
Allows user-based manual control for switching between lights.
Timed cycles for each light:
Red Light: 5 seconds
Yellow Light: 2 seconds
Green Light: 5 seconds
Validates user input and prompts for re-entry if an invalid choice is made.
Simple, text-based user interface.
Technologies Used
Python: The system is implemented using Python 3.x.
Libraries:
time: Used to simulate delays for each light's duration.
Getting Started
Prerequisites
Python 3.x or higher installed on your machine.
A terminal or command-line interface to run the Python script.
Installation
Clone the repository:

bash
Copy
git clone https://github.com/yourusername/traffic-light-control-system.git
Navigate to the project directory:

bash
Copy
cd traffic-light-control-system
No additional libraries or packages are needed to run the system, as it uses built-in Python libraries.

Running the System
Open a terminal or command prompt.
Navigate to the project directory where the script is located.
Run the script using the following command:
bash
Copy
python traffic_light_control.py
Usage
Once the system starts, the user will be presented with a simple menu displaying the following options:

1: Turn on Red Light (Stop)
2: Turn on Yellow Light (Prepare to Stop)
3: Turn on Green Light (Go)
4: Exit the system
To control the traffic lights:

Enter the number corresponding to the desired light (1 for Red, 2 for Yellow, 3 for Green).
The system will simulate the light turning on and then wait for the corresponding duration (as defined in the script).
If you want to exit the system, select option 4.
Example of menu output:

bash
Copy
Traffic Light Control System
1. Red Light
2. Yellow Light
3. Green Light
4. Exit
Enter your choice (1-4):
Sample Output
When selecting Red Light:
bash
Copy
Red Light: STOP
When selecting Yellow Light:
bash
Copy
Yellow Light: GET READY
When selecting Green Light:
bash
Copy
Green Light: GO
Code Explanation
The system is implemented in Python using the time.sleep() function to simulate the duration each light stays on. The input() function is used for user interaction, where the user is prompted to select the light they wish to activate.

Main Components of the Code:
display_menu(): Displays the options for the user to select the light.
traffic_light_control(): The main loop that handles user input and controls the lights.
time.sleep(): Used to control the duration for each light (5 seconds for Red and Green, 2 seconds for Yellow).
Code Snippet:
python
Copy
import time

def display_menu():
    print("\nTraffic Light Control System")
    print("1. Red Light")
    print("2. Yellow Light")
    print("3. Green Light")
    print("4. Exit")

def traffic_light_control():
    while True:
        # Display menu
        display_menu()

        # Get user input
        try:
            choice = int(input("Enter your choice (1-4): "))

            if choice == 1:
                print("Red Light: STOP")
                time.sleep(5)  # Red light for 5 seconds
            elif choice == 2:
                print("Yellow Light: GET READY")
                time.sleep(2)  # Yellow light for 2 seconds
            elif choice == 3:
                print("Green Light: GO")
                time.sleep(5)  # Green light for 5 seconds
            elif choice == 4:
                print("Exiting Traffic Light Control System.")
                break
            else:
                print("Invalid choice. Please enter a number between 1 and 4.")
        except ValueError:
            print("Invalid input! Please enter a valid number.")
Contributing
Contributions to improve this project are welcome! If you'd like to contribute, please fork the repository, make your changes, and create a pull request.

License
This project is open-source and available under the MIT License.

Acknowledgements
The system was built as part of a learning project to simulate traffic light control.
Python documentation for time.sleep() and basic I/O handling was referenced during the development.
