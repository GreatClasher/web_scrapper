# Flipkart Web Scraper

This is a simple web scraper built with Flask for extracting product reviews from Flipkart. It allows users to enter a search term, retrieves the product details from Flipkart, and then scrapes and displays customer reviews.

## Features

- Search for a product on Flipkart
- Extract customer reviews, including name, rating, comment heading, and comment
- Store reviews in MongoDB

## Technologies Used

- Flask
- Flask-CORS
- Requests
- BeautifulSoup (bs4)
- pymongo
- HTML, CSS (for frontend)

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/web_scrapper.git
    cd flipkart-web-scraper
    ```

2. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Set up MongoDB:

    - Create a MongoDB database and collection.
    - Update the MongoDB connection string in `application.py`.

## Usage

1. Run the application:

    ```bash
    python application.py
    ```

2. Open your browser and visit [http://127.0.0.1:8000/](http://127.0.0.1:8000/) to access the web scraper.

3. Enter a product name in the search bar, and the application will display the extracted reviews.

## Deployment

This application is designed to be deployed on AWS Elastic Beanstalk using AWS CodePipeline. The source code is automatically deployed when changes are pushed to the main branch.

## Contributing

Feel free to contribute to the project by opening issues or submitting pull requests. Follow standard Git flow:

1. Fork the repository.
2. Create a new branch for your feature/bug fix.
3. Make changes and commit.
4. Submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
