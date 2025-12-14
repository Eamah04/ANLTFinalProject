# ANLTFinalProject
This project demonstrated the successful design and implementation of an AI-powered operational decision support system for a transportation and logistics context. 

 ## How to Run Experiments Locally
 **Clone the repository**
   ```bash
   git clone https://github.com/Eamah04/ANLTFinalProject.git
   cd ANLTFinalProject
 ```
**Install dependencies**
```pip install -r requirements.txt
```
**Ensure models are available**
Place tuned_rf.pkl (classification model) and tuned_gbr.pkl (regression model) in the project root.
These files must match the scikit-learn version used during training.

**Run the Flask app**
```python app.py
```
The app will start at http://127.0.0.1:5000.
Ngrok will generate a public URL : Public URL: NgrokTunnel: "https://unfiltered-karly-uncaptivating.ngrok-free.dev"
Share this link to allow external users to access the app.

## How to Reproduce Results
**Match scikit-learn version**
Models were trained with scikit-learn==1.3.2.
Ensure the same version is installed: pip install scikit-learn==1.3.2
**Upload or place models**
In Colab: use 
```files.upload() to upload .pkl files.
```
Locally: ensure they are in the project folder.
**Run the app**
Start Flask (python app.py) and open the browser at http://127.0.0.1:5000.
Or use the ngrok public URL (e.g., https://unfiltered-karly-uncaptivating.ngrok-free.dev) for external access.
**Input test values**
Distance (km), Preparation Time (min), Courier Experience (yrs), Weather, Traffic Level, Time of Day, Vehicle Type.
**Observe predictions**
Regression model outputs delivery time (minutes).
Classification model outputs status: Delayed or On Time.
**Compare results**
Expected metrics: MAE ≈ 6, R² ≈ 0.82, classification accuracy ≈ 93%
## Dependencies
Listed in requirements.txt
