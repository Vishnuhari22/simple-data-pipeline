# Simple ETL Data Pipeline with Python and Docker

This project is a simple, containerized ETL (Extract, Transform, Load) data pipeline. It extracts data from a raw CSV file (`MedicalDataset.csv`), cleans and transforms the data using Python's Pandas library, and saves the processed data to a new CSV file (`CleanedMedicalData.csv`).

The entire process is managed and orchestrated using Docker and Docker Compose, making it portable and easy to run.

## 🏛️ Architecture

The pipeline follows a simple architecture where the script, containerized by Docker, reads from a data source, processes it, and writes to a destination.

![ETL Architecture Diagram](ETL-1.png)

*Note: Make sure you've added your `ETL-1.png` diagram to the root of your repository so it appears here.*

---

## 🛠️ Tech Stack

* **Python**: The core language for the ETL script.
* **Pandas**: Used for data manipulation and transformation.
* **Docker**: Used for containerizing the application and its dependencies.
* **Docker Compose**: Used to define and run the multi-container Docker application.

---

## 🚀 Getting Started

Follow these instructions to get a copy of the project up and running on your local machine.

### Prerequisites

* You must have **Docker** and **Docker Compose** installed on your machine. You can download them from the [official Docker website](https://www.docker.com/products/docker-desktop).

### Installation & Usage

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    ```

2.  **Navigate to the project directory:**
    ```sh
    cd your-repo-name
    ```

3.  **Run the pipeline:**
    Use Docker Compose to build the image and run the container.
    ```sh
    docker-compose up
    ```

This command will start the service defined in `docker-compose.yml`, which runs the `pipeline.py` script. You will see the output logs in your terminal, indicating the completion of each ETL step.

After the process completes successfully, you can find the processed file, `CleanedMedicalData.csv`, in the `data/` directory.

---

## 📂 Project Structure

```
.
├── data/
│   ├── MedicalDataset.csv      # Raw input data
│   └── CleanedMedicalData.csv  # Processed output data (after running)
├── pipeline.py                 # The main ETL script
├── Dockerfile                  # Instructions to build the Docker image
├── docker-compose.yml          # Docker Compose configuration
├── requirements.txt            # Python dependencies
└── README.md                   # This file
```

---

## 📜 License

This project is licensed under the MIT License.
