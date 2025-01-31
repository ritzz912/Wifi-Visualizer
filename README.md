# Wifi-Visualizer
Overview
Wi-Fi Visualizer is a web application designed to measure Wi-Fi signal strength at various locations in a given area and generate a heat map that visualizes signal distribution. Users can upload a floor plan image, and Wi-Fi strength data collected at specific coordinates is overlaid on this image, creating a clear visualization of Wi-Fi coverage.

Features
•	Wi-Fi Signal Strength Collection: Automatically collects Wi-Fi signal strength at specified coordinates within the area.
•	Data Storage: Stores location-based signal strength data in a CSV file.
•	Heat Map Generation: Uses Radial Basis Function (RBF) interpolation to generate a heat map overlay on the uploaded floor plan.
•	User Interface: Provides a user-friendly interface to display the heat map and allow users to input location coordinates.

Requirements
•	Python 3.x
•	Django
•	NumPy
•	Pandas
•	SciPy
•	Matplotlib
•	Seaborn

Installation
1.	Make sure Python 3.x is installed on your machine.
2.	Install the necessary libraries by running:
Copy this in bash:
pip install django numpy pandas scipy matplotlib seaborn
3.	Set up the Django application by navigating to the project directory and starting the server:
Copy this in bash:
python manage.py runserver
4.	Access the application in your browser at http://127.0.0.1:8000.

Usage
1.	Collecting Wi-Fi Data: Open the application interface and log Wi-Fi signal strength at different coordinates within the area.
2.	Generating a Heat Map: Use the heat map generation feature to produce a visual representation of signal strength over the specified floor plan.
Project Structure
•	views.py: Contains the main logic for handling Wi-Fi data collection, CSV storage, and heat map generation.
•	static/: Stores the generated heat map image.
•	templates/: HTML templates for the application interface.

Example Code Snippets
Example of Wi-Fi data saving to CSV:
python
Copy code
with open(CSV_FILE, mode='a', newline='') as file:
    writer = csv.writer(file)
    writer.writerow([x, y, wifi_strength])

Future Scope
•	Signal Strength Visualization on Custom Floor Plans: Add support for uploading custom floor plans and overlaying signal strength data directly on the uploaded images.
•	Real-Time Data Updates: Implement a feature to display real-time changes in Wi-Fi signal distribution on the heat map.
