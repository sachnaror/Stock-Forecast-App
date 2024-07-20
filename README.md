# Website Checker and Alert System

## Overview

This project is designed to monitor specific websites in open browser tabs and play an alert sound when any of these websites are detected. The script runs continuously and checks the open tabs every minute. If any of the specified websites are found, an alert sound will play until the tabs are closed.

The script is built using Python and leverages Streamlit for a user-friendly interface. It supports multiple operating systems, including Windows, macOS, and Linux, and is compatible with major web browsers.

## Features

- **Continuous Monitoring**: The script runs indefinitely, checking open browser tabs every 60 seconds.
- **Multi-Browser Support**: Works with Safari, Google Chrome, Brave on macOS; and general window titles on Windows and Linux.
- **Audio Alerts**: Plays an alert sound when specified websites are detected in open tabs.
- **Streamlit Interface**: Provides a web-based interface for monitoring the script's status and results.

## Requirements

- Python 3.7+
- Streamlit
- Pydub
- Simpleaudio
- Pygetwindow (Windows)
- wmctrl (Linux)

## Installation

1. **Clone the repository**:

    ```sh
    git clone <repository-url>
    cd <repository-directory>
    ```

2. **Create and activate a virtual environment**:

    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. **Install the required packages**:

    ```sh
    pip install -r requirements.txt
    ```

4. **Install additional system dependencies**:

    - **Linux**: Install `wmctrl`

        ```sh
        sudo apt-get install wmctrl
        ```

## Usage

1. **Place your alert sound file**: Ensure you have an alert sound file in `.wav` format. Place it in a convenient location and update the `sound_path` variable in the script with the path to this file.

2. **Run the Streamlit app**:

    ```sh
    streamlit run t80.py
    ```

3. **Interact with the app**: Open the provided URL in your web browser to view and interact with the app. The app will display the status of monitored websites and play an alert sound if any specified websites are detected.

## Code Explanation

### Main Script (`youTrade.py`)

The main script sets up the monitoring and alert system, using Streamlit for the interface.

#### Importing Modules

```python
import streamlit as st
import platform
import subprocess
import time
import simpleaudio as sa
from threading import Event, Thread



#Future Improvements

    •   Add support for more browsers and operating systems.
    •   Enhance the UI with more control options.
    •   Add logging functionality to track detected websites over time.
    •   Implement notification support for better alerts.
