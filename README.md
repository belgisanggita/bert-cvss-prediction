## By Belgis Anggita 

1. Clone repositories
    ```bash
    git clone https://github.com/belgisanggita/bert-cvss-prediction.git
    cd bert-cvss-prediction
    ```
2. Download the model without training
    - Download on **Release** Section
    ![{38CAC19B-5B60-49D6-BCBE-15D61506DA48}](https://github.com/user-attachments/assets/28a5ec0d-a484-4bbc-bc45-758ffc090341)
    - Create "models" folder
        ```bash
        mkdir -p ./models
        ```
    - Extract all of the models from "models.zip" to "models/" folder 

3. Install Libraries
    ```bash
    python -m venv venv
    source venv/Scripts/activate
    pip install -r requirements.txt
    ```
4. Run the model and the app
    ```bash
    python app.py
    ```

5. Or Run using Docker
    ```bash
    docker build -t cvss-bert-image .
    ```
    ```bash
    docker run -d --name cvss-bert-container -p 5000:5000 cvss-bert-image
    ```

    
    
