# Uber DataViz: An Interactive Tkinter Explorer

*A user-friendly desktop application for swift, visual exploration of Uber ride-sharing data.*

## Table of Contents

* [Introduction](#introduction)
* [Features](#features)
* [Problem Statement / Motivation](#problem-statement--motivation)
* [Technologies Used](#technologies-used)
* [Installation & Setup](#installation--setup)
* [Usage](#usage)
* [Project Structure](#project-structure)
* [Screenshots / Demo](#screenshots--demo)
* [Challenges & Learnings](#challenges--learnings)
* [Future Enhancements](#future-enhancements)
* [Team Members](#team-members)
* [License](#license)
* [Contact](#contact)

## Introduction

This project is a straightforward yet powerful desktop application built with Python's **Tkinter** for the graphical user interface, integrated with **Pandas** for data handling and **Matplotlib** for visualization. It allows users to intuitively load and explore large ride-sharing datasets, specifically designed for **Uber trip data**. The tool simplifies the process of generating common statistical plots, enabling quick insights into patterns, distributions, and relationships within the data.

## Features

* **CSV Data Loading:** Effortlessly import your Uber trip datasets from a standard CSV file.
* **Dynamic Variable Selection:** Select any two columns (variables, e.g., `Pickup_longitude`, `Fare_amount`, `Trip_duration`) from your loaded Uber data using user-friendly dropdown menus for targeted analysis and plotting.
* **Multiple Visualization Types:** Generate key statistical plots:
    * **Scatter Plots:** Ideal for visualizing relationships between two numerical variables (e.g., `fare_amount` vs. `trip_distance`).
    * **Histograms:** Show the distribution of a single numerical variable (e.g., frequency of `trip_duration` values).
    * **Box Plots:** Compare the distribution and central tendency of a numerical variable across different categories or for two different variables (e.g., `fare_amount` across `hour_of_day`).
* **Integrated Plotting:** Matplotlib plots are seamlessly embedded directly within the application's GUI, providing an all-in-one experience.
* **Intuitive User Interface:** Designed with Tkinter for a clean, accessible, and user-friendly experience, making data exploration accessible to non-programmers as well.

## Problem Statement / Motivation

The explosion of data from ride-sharing services like Uber presents immense opportunities for understanding urban dynamics, transportation trends, and operational efficiency. However, extracting actionable insights from these large datasets often requires specialized tools or coding expertise. This application was developed to bridge that gap, providing a quick, visual, and user-friendly platform for preliminary **Exploratory Data Analysis (EDA)**. It empowers data analysts, researchers, urban planners, or anyone interested in ride-sharing data to rapidly visualize key trends, identify anomalies, and formulate hypotheses without the overhead of writing extensive scripts.

## Technologies Used

* **Python:** The core programming language.
* **Tkinter:** For building the graphical user interface (GUI).
* **Pandas:** For efficient data loading, manipulation, and analysis of tabular data.
* **Numpy:** For high-performance numerical operations.
* **Matplotlib:** For creating static, interactive, and animated visualizations in Python.

## Installation & Setup

To get a copy of the project up and running on your local machine, follow these steps:

1.  **Prerequisites:**
    * Python 3.x installed on your system.

2.  **Clone the repository:**
    ```bash
    git clone https://github.com/shreud/dataScienceInUber.git
    cd dataScienceInUber
    ```

3.  **Create a virtual environment (recommended for dependency management):**
    ```bash
    python -m venv venv
    # On Windows:
    .\venv\Scripts\activate
    # On macOS/Linux:
    source venv/bin/activate
    ```

4.  **Install the required dependencies:**
    *(Create a `requirements.txt` file in your project's root directory with the following content:)*
    ```
    pandas
    numpy
    matplotlib
    ```
    Then, run:
    ```bash
    pip install -r requirements.txt
    ```

5.  **Obtain the Uber Dataset:**
    * This application is designed to work with standard Uber trip CSV datasets.
    * You can typically find public Uber datasets (e.g., "Uber Pickups in NYC") on platforms like Kaggle.
    * Download your desired `.csv` file and place it in the root directory of this project (or create a `data/` folder and place it there, then update your code to reflect the path).

## Usage

1.  **Run the application:**
    ```bash
    python main.py
    ```
2.  **Load Data:** In the application window, click the "Load CSV" button and navigate to select your Uber dataset CSV file.
3.  **Select Variables:** Once the data is loaded, dropdown menus will populate with column names. Choose one or two variables (depending on the plot type) that you wish to analyze.
4.  **Choose Graph Type:** Select your desired visualization type (Scatter Plot, Histogram, or Box Plot) using the provided radio buttons.
5.  **Analyze Data:** Click the "Analyze Data" button. The application will process your selection and display the generated plot, providing immediate visual insights into the Uber data.

## Project Structure

A typical layout for this project would be:

.
├── main.py <br>
├── data/ <br>
│   └── uber_trips.csv <br>
├── screenshots/ <br>
│   └── app_screenshot_1.png <br>
│   └── plot_demo.gif <br>
├── README.md <br>
└── requirements.txt <br>
└── LICENSE <br>


## Challenges & Learnings
* **GUI-Backend Integration:** Integrating data processing (Pandas, Matplotlib) seamlessly with a responsive Tkinter GUI required careful state management and threading considerations to prevent the UI from freezing.
* **Handling Diverse Data Types:** Ensuring the application could correctly handle different data types (numerical, categorical, datetime) from various CSV columns for appropriate plotting was a learning curve.
* **Error Handling:** Implementing robust `try-except` blocks to gracefully handle file loading errors, missing columns, or invalid data selections, providing user-friendly feedback rather than crashing.
* **Performance Optimization:** Strategies for optimizing the application's performance when dealing with larger Uber datasets, such as efficient Pandas operations or plot rendering.
* **User Experience (UX) Design in Tkinter:** Balancing functionality with simplicity in the GUI to ensure an intuitive and efficient user workflow.

## Future Enhancements
* **Advanced Plotting Options:** Implement additional visualization types such as line plots (for time-series data like trips over hours/days), bar charts (for categorical data), or heatmaps (for geographical density of pickups/drop-offs).
* **Basic Statistical Summaries:** Add a panel to display descriptive statistics (mean, median, standard deviation, quartiles) for selected variables.
* **Data Filtering & Grouping:** Allow users to filter the dataset based on specific criteria or group data for comparative analysis (e.g., by `driver_id` or `trip_status`).
* **Interactive Features:** Incorporate more interactive elements like zoom, pan, and hover-tooltips on plots.
* **Export Options:** Enable users to export generated plots as image files (PNG, JPEG).
* **Mapping Integration:** Integrate a mapping library (e.g., Folium) to visualize geographical pick-up and drop-off points directly on a map.

## License
This project is open-sourced under the MIT License. See the `LICENSE` file for more details.

## Contact
Feel free to reach out for questions, collaborations, or just to connect!

* [Email](shruti41wadekar@gmail.com)
* [GitHub Profile](https://github.com/shreud)
* [LinkedIn Profile](https://www.linkedin.com/in/shruti-w/)
