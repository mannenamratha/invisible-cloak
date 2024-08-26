# Invisible Cloak Project

## Overview

The Invisible Cloak project uses computer vision techniques to create an effect where a specific color in the video feed (e.g., pink) appears invisible, revealing the background behind it. This is achieved using OpenCV and Python. The application captures video from your webcam, identifies the designated color, and replaces it with a background image to simulate the "invisibility" effect.

## Features

- Real-time invisibility cloak effect.
- Captures and uses a background image for the effect.
- Applies color-based masking to achieve the invisibility effect.

## Technologies Used

- **Programming Language:** Python
- **Libraries:**
  - `opencv-python` for computer vision tasks.
  - `numpy` for numerical operations.
- **Hardware:** Webcam

## Installation

To set up and run the Invisible Cloak project, follow these instructions:

### Prerequisites

- Python 3.x installed on your machine.
- A webcam connected to your computer.

### Steps

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/invisible-cloak.git
   cd invisible-cloak
   ```

2. **Create a Virtual Environment:**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install Dependencies:**

   ```bash
   pip install opencv-python-headless numpy
   ```

4. **Run the Application:**

   ```bash
   python invisible_cloak.py
   ```

## Usage

1. **Start the Application:**

   - Run the application with the command `python invisible_cloak.py`.

2. **Capture Background:**

   - Once the application starts, it will capture a series of frames to create a background model. Make sure you are not in the frame while this happens.

3. **Apply the Cloak Effect:**

   - After capturing the background, the application will start processing the video feed to apply the invisibility effect based on the predefined color (pink in this case).

4. **Exit the Application:**

   - Press 'q' while the application window is focused to exit the program.

## Configuration

- **HSV Color Range for Pink:**
  - The current HSV range for detecting pink color is set to:
    - `lower_pink = np.array([160, 100, 100])`
    - `upper_pink = np.array([180, 255, 255])`
  - Adjust these values in the `invisible_cloak.py` script if you need to detect different colors.

- **Background Capture:**
  - The number of frames captured for the background can be adjusted by changing the `num_frames` parameter in the `create_background` function.

## Troubleshooting

- **Camera Not Opening:**
  - Ensure that your webcam is connected and properly configured. Check if other applications are using the webcam.

- **Frames Not Captured:**
  - If no frames are captured, try adjusting the `time.sleep` duration in the `create_background` function or check the camera's driver and permissions.

- **Mask Issues:**
  - If the color detection is not accurate, adjust the HSV color range values.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For questions or support, please contact:

- **Email:** manne.namrathasai@gmail.com
- **GitHub:** https://github.com/mannenamratha

