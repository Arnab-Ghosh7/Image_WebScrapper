# Image Web Scrapper

![Python](https://img.shields.io/badge/Python-3.7+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-2.0+-000000?style=for-the-badge&logo=flask&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-4.x-4B8BBE?style=for-the-badge&logo=pypi&logoColor=white)

A robust **Flask-based web application** designed to automate the process of scraping and displaying images from Google Images based on user search queries.

## 📝 Description

This project serves as a comprehensive tool for collecting bulk images from the web. It solves the problem of manual image saving by automating the search and download process.

**How it works:**
1.  **User Interface:** The user enters a keyword (e.g., "Golden Retriever") on the home page.
2.  **Request Handling:** The Flask backend intercepts the request and allows cross-origin requests.
3.  **Web Scraping:** The `ScrapperImage` class constructs a Google Images search URL and parses the HTML response using **BeautifulSoup**.
4.  **Extraction & Download:** It extracts the raw image URLs, iterates through them, and downloads the images to the server's `static` directory.
5.  **Visualization:** Finally, the application dynamically generates a gallery view to display the downloaded images to the user.

This tool is particularly useful for:
*   **Data Scientists/ML Engineers**: Quickly building image datasets for Computer Vision models.
*   **Designers**: Gathering visual references or mood boards.
*   **Developers**: Testing image processing pipelines or gallery components.

## ✨ Features

- **Dynamic Search**: Real-time keyword-based image search.
- **Automated Scraping**: Efficiently scrapes multiple images in a single run.
- **Local Storage**: Automatically manages and saves images to the `static` folder.
- **Clean UI**: Simple and intuitive interface for searching and viewing results.
- **Error Handling**: gracefully handles connection errors or missing images.
- **Cross-Origin Support**: Integrated `flask_cors` for seamless API interactions.

## 🛠️ Tech Stack

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Backend** | ![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white) | Lightweight WSGI web application framework. |
| **Language** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) | Core logic and scripting. |
| **Scraping** | ![BS4](https://img.shields.io/badge/BeautifulSoup-4B8BBE?style=flat&logo=pypi&logoColor=white) | Parsing HTML and XML documents. |
| **Frontend** | ![HTML/CSS](https://img.shields.io/badge/HTML5_&_CSS3-E34F26?style=flat&logo=html5&logoColor=white) | Structure and styling of the web interface. |
| **Requests** | `urllib` / `requests` | Handling HTTP requests to Google. |

## 🚀 Installation & Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Arnab-Ghosh7/Image_WebScrapper
   cd Image_WebScrapper
   ```

2. **Create a Virtual Environment**
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Application**
   ```bash
   python app.py
   ```

5. **Access the App**
   Open your browser and navigate to: [`http://127.0.0.1:8000`](http://127.0.0.1:8000)

## 📂 Project Structure

```text
Image_WebScrapper/
├── app.py                  # Main Flask application entry point. Routes requests.
├── businesslayer/          # Encapsulates business logic.
│   └── BusinessLayerUtil.py # Orchestrates the download process.
├── scrapperImage/          # Core scraping engine.
│   └── ScrapperImage.py    # Handles HTML parsing and file writing.
├── static/                 # Storage for downloaded images (CSS/JS if any).
├── templates/              # HTML templates.
│   ├── index.html          # Input form for search keywords.
│   └── showImage.html      # Grid display of scraped images.
├── requirements.txt        # List of python dependencies.
└── LICENSE                 # License terms.
```

## 📜 License

This project is licensed under the **GNU General Public License v2.0**. See the [LICENSE](LICENSE) file for details.

## ✍️ Author

- **Arnab Ghosh** - *Initial work*
