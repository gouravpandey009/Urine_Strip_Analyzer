# Urine Stripes Analyzer

## Project Overview

The Urine Strip Analyzer project is designed to analyze images of urine strips and extract associated colors for medical diagnostics. The project operates under the following assumptions:
1. The input image is in `.jpg` format.
2. These image has making the colors distinguishable to the human eye.

### Screenshots

![Screenshot 0](assets/0.PNG)
![Screenshot 1](assets/1.PNG)
![Screenshot 2](assets/2.PNG)
![Screenshot 3](assets/3.PNG)
![Screenshot 4](assets/4.PNG)
![Screenshot 5](assets/5.PNG)
![Screenshot 6](assets/6.PNG)
![Screenshot 7](assets/7.PNG)
![Screenshot 8](assets/8.PNG)
![Screenshot 9](assets/9.PNG)
![Screenshot 10](assets/10.PNG)
![Screenshot 11](assets/11.PNG)
![Screenshot 12](assets/12.PNG)
![Screenshot 13](assets/13.PNG)
![Screenshot 14](assets/14.PNG)
![Screenshot 15](assets/15.PNG)
![Screenshot 16](assets/16.PNG)
## Technology Stack

### Frontend

- **Framework**: ReactJS
- **Build Tool**: Vite
- **Component Library**: Chakra UI
- **HTTP Client**: Axios

### Backend

- **Framework**: Django + FastAPI (Python)
- **ASGI Server**: uvicorn

## Methodology

### Color Extraction Process

The color extraction logic is encapsulated in the `extractColors.py` file and involves three main steps:

1. **Cropping**: The background is removed to prevent interference with color detection.
2. **Preprocessing**: A bilinear extrapolator is used to replace each pixel's value with the average value of the row, eliminating granular noise and dark patches.
3. **Segmentation**: Small segments (2x2 pixels) are extracted from the image using a vertical offset to capture the color from each square. The average value of these segments determines the final RGB value of each square.

## Deployment

### Using Docker and Docker Compose

Follow these steps to deploy the application:

1. Ensure Docker and Docker Compose are installed on your system.
2. Navigate to the root directory of the project.
3. Run the following command to build and start the application:

   ```sh
   docker-compose up
   ```

4. Open your browser and navigate to [http://localhost:5173](http://localhost:5173).


#Extended Description

Sure! Here is an extended description you can add to your `README.md` file:

---

## Extended Description

### Motivation

Urine strip tests are a common diagnostic tool used in medical practice to detect a variety of conditions based on the chemical composition of urine. Automating the analysis of these strips can enhance accuracy, efficiency, and accessibility in medical diagnostics.

### Features

- **User-Friendly Interface**: The frontend, built with ReactJS and styled using Chakra UI, provides a clean and intuitive interface for uploading and analyzing urine strip images.
- **Efficient Backend Processing**: The FastAPI backend ensures fast and reliable processing of images, utilizing Python's robust image processing libraries.
- **Color Extraction**: Advanced algorithms preprocess and segment the image to accurately extract color data from urine strips.
- **Dockerized Deployment**: Easy deployment with Docker and Docker Compose, enabling consistent and reproducible environments.

### Installation

To set up the development environment, follow these steps:

1. Clone the repository:

   ```sh
   git clone https://github.com/yourusername/urine-strip-analyzer.git
   cd urine-strip-analyzer
   ```

2. Install frontend dependencies:

   ```sh
   cd frontend
   npm install
   ```

3. Install backend dependencies:

   ```sh
   cd backend
   pip install -r requirements.txt
   ```

### Usage

1. Start the backend server:

   ```sh
   uvicorn main:app --reload
   ```

2. Start the frontend development server:

   ```sh
   npm run dev
   ```

3. Open your browser and navigate to `http://localhost:5173` to use the application.

