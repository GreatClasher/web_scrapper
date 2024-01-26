# Flipkart Web Scraper

This is a simple web scraper built with Flask for extracting product reviews from Flipkart. It allows users to enter a search term, retrieves the product details from Flipkart, and then scrapes and displays customer reviews.
![Web Scraper](https://i.ibb.co/5rMKt7D/your-image-file.jpg)


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

## Deployment on AWS Elastic Beanstalk with CodePipeline

### Prerequisites

- [AWS CLI](https://aws.amazon.com/cli/)
- [AWS Elastic Beanstalk CLI (EB CLI)](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html)
- [AWS CodePipeline](https://aws.amazon.com/codepipeline/)

### Steps

1. **Configure AWS Elastic Beanstalk:**

    - Create an Elastic Beanstalk environment with the appropriate settings.
    - Ensure that the environment has the necessary environment variables (e.g., MongoDB connection string) configured.

2. **Configure AWS CodePipeline:**

    - Create a CodePipeline in the AWS Management Console.
    - Configure the source stage to connect to your GitHub repository.
    - Configure the build stage to use AWS CodeBuild or a custom build environment.
    - Configure the deploy stage to deploy the application to Elastic Beanstalk.

3. **Update AWS Elastic Beanstalk Configuration:**

    - Ensure that your Elastic Beanstalk environment uses a Python runtime.
    - Update the `requirements.txt` file with the necessary dependencies.
    - Configure environment variables in the Elastic Beanstalk console or using configuration files.

4. **Push Changes to GitHub:**

    - Push any changes to your GitHub repository. This should trigger the CodePipeline to automatically deploy the updated application.


This application is designed to be deployed on AWS Elastic Beanstalk using AWS CodePipeline. The source code is automatically deployed when changes are pushed to the main branch.

## Contributing

Feel free to contribute to the project by opening issues or submitting pull requests. Follow standard Git flow:

1. Fork the repository.
2. Create a new branch for your feature/bug fix.
3. Make changes and commit.
4. Submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
