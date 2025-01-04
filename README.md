## By Belgis Anggita 

## Training Parameter Tuning
- epoch = 3
- batch size = 16
- learning rate = 5e-5
- Tokenizer/NLP Model = BERT-SMALL

## Training Loss and Accuracy

| **Categories**             | **Training Loss**  | **Training Accuracy**  |
|----------------------------|--------------------|------------------------|
| **Attack Vector**          |0.06153090472359961 |0.9803575447282548      |
| **Attack Complexity**      |0.039294798068496416|0.9876969242310578      |
| **Privileges Required**    |0.24270883338943902 |0.9058989298907041      |
| **User Interaction**       |0.09731902825969928 |0.9656017369727047      |
| **Scope**                  |0.051076244030279334|0.983862208084413       |
| **Confidentiality Impact** |0.1733723337674384  |0.9379836323341876      |
| **Integrity Impact**       |0.1933152508040746  |0.9314789886456748      |
| **Availability Impact**    |0.13116088520879207 |0.9534929477010858      |

## Metrics Summary

| **Categories**             | **Accuracy** | **Balanced Accuracy**  | **Precision** | **Recall** | **F1 Score** |
|----------------------------|--------------|------------------------|---------------|------------|--------------|
| **Attack Vector**          | 0.9791       | 0.9791                 | 0.9792        | 0.9791     | 0.9791       |
| **Attack Complexity**      | 0.9890       | 0.9891                 | 0.9891        | 0.9890     | 0.9890       |
| **Privileges Required**    | 0.8991       | 0.8993                 | 0.9002        | 0.8991     | 0.8986       |
| **User Interaction**       | 0.9637       | 0.9637                 | 0.9637        | 0.9637     | 0.9637       |
| **Scope**                  | 0.9837       | 0.9837                 | 0.9837        | 0.9837     | 0.9837       |
| **Confidentiality Impact** | 0.9252       | 0.9251                 | 0.9256        | 0.9252     | 0.9246       |
| **Integrity Impact**       | 0.9137       | 0.9136                 | 0.9135        | 0.9137     | 0.9135       |
| **Availability Impact**    | 0.9408       | 0.9412                 | 0.9406        | 0.9408     | 0.9404       |


## Steps to Deploy
1. Clone repositories
    ```bash
    git clone https://github.com/belgisanggita/bert-cvss-prediction.git
    cd bert-cvss-prediction
    ```
2. Download the model without training
    - Download on **Releases** Section
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

    
    
