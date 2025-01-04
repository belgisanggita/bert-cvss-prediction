## By Belgis Anggita 

1. Clone repositories
    ```bash
    git clone https://github.com/omidiyanto/bert-small-cvss-prediction.git
    cd bert-small-cvss-prediction
    ```
2. Download the model without training
    ```bash
    pip install gdown
    mkdir -p ./models
    gdown https://drive.google.com/drive/folders/1eScuYo-_todE6o7fPCrMTZHcxokb-syU -O models --folder
    ```

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
    
