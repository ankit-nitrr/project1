# Geology Data Preprocessing Tool

A Flask-based web application for preprocessing geological and geochemical data CSV files. This tool automatically fills missing or incomplete data values with appropriate default values for geophysical and geochemical parameters.

## Features

- Web-based CSV upload and processing interface
- Automated preprocessing of geochemical data including:
  - Oxide compositions (SiO2, TiO2, Al2O3, etc.)
  - Trace elements (Ba, Sc, Co, Cr, Ni, V, Zr, etc.)
  - Rare earth elements (La, Ce, Pr, Nd, etc.)
- Handles blank and missing data values
- Downloads preprocessed data as CSV


## Usage

1. Run the Flask application:
   ```bash
   python app.py
   ```

2. Open your web browser and navigate to `http://localhost:5000`

3. Upload your CSV file containing geological/geochemical data

4. Click "Preprocess" to process the file

5. Download the preprocessed CSV file

## Data Format

Your CSV file should contain columns for geochemical parameters. The tool will automatically replace empty strings and "<" symbols with NaN values and fill them with default values suitable for geochemical analysis.

## Technologies Used

- Python 3.x
- Flask
- Pandas
- NumPy

## Deployment

### Deploy to Render

1. Fork or create a repository on GitHub and push this code.

2. Create a Render account at [render.com](https://render.com).

3. Click "New" and select "Web Service".

4. Connect your GitHub repository.

5. Configure the service:
   - **Build Command**: Leave as default (`pip install -r requirements.txt`)
   - **Start Command**: `gunicorn app:app`
   - Select your desired plan

6. Click "Create Web Service" to deploy.

Your app will be live at the provided Render URL.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source. Please check the license file for more details.
