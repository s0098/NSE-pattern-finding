# Nifty 500 Pattern Detection with YOLOv8

This project uses a YOLOv8 model from Hugging Face to detect stock market patterns on candlestick charts for NSE indices and Nifty 500 stocks. It fetches historical data, generates candlestick charts, runs YOLOv8 inference, and compiles annotated images into a PDF report.

## Features

- Fetches historical stock data using Yahoo Finance (`yfinance`)
- Generates candlestick charts with `mplfinance`
- Runs pattern detection using a YOLOv8 model from Hugging Face
- Annotates detected patterns on chart images
- Compiles annotated images into a PDF report

## Requirements

- Python 3.8+
- [ultralytics](https://github.com/ultralytics/ultralytics) (YOLOv8)
- [yfinance](https://github.com/ranaroussi/yfinance)
- [mplfinance](https://github.com/matplotlib/mplfinance)
- [opencv-python](https://github.com/opencv/opencv-python)
- [numpy](https://numpy.org/)
- [openpyxl](https://openpyxl.readthedocs.io/)
- [matplotlib](https://matplotlib.org/)
- [reportlab](https://www.reportlab.com/)
- [Pillow](https://python-pillow.org/)

Install dependencies with:

```sh
pip install mss==10.0.0 opencv-python==4.11.0.86 numpy ultralytics==8.3.94 openpyxl==3.1.5 mplfinance matplotlib reportlab yfinance pyvirtualdisplay google-api-python-client google-auth-httplib2 google-auth-oauthlib ultralyticsplus
```

## Usage

1. Clone the YOLOv8 model from Hugging Face:

    ```sh
    git lfs install
    git clone https://huggingface.co/foduucom/stockmarket-pattern-detection-yolov8
    ```

2. Run the script:

    ```sh
    python nifty500_pattern_yolo_model.py
    ```

3. The script will:
    - Download stock data
    - Generate candlestick charts
    - Run YOLOv8 inference to detect patterns
    - Save annotated images in the `annotated_images` directory
    - Create a PDF report with all annotated images

## Output

- Annotated images: `annotated_images/`
- PDF report: `annotated_images_YYYY-MM-DD.pdf`

## Notes

- The script processes both NSE indices and all Nifty 500 stocks.
- Model weights are loaded from the Hugging Face repository.
- Make sure you have sufficient disk space and bandwidth for model and data downloads.

## License

This project is for educational and research purposes only.

