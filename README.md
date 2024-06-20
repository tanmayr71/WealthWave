# WealthWave

WealthWave is a personal finance management tool designed to help users manage their finances efficiently. This project leverages cloud computing and advanced AI capabilities to provide robust and scalable financial management solutions.

## Demo

Watch the demo video on [YouTube](https://www.youtube.com/watch?v=4ZwqtT1zWqM).

<img width="1470" alt="image" src="https://github.com/tanmayr71/WealthWave/assets/55703966/e10e5060-428c-4ebd-9ca6-4cb814e17679">

## Features

- **Expense Tracking**: Monitor daily expenses and categorize them for better insights.
- **Budget Management**: Set and manage budgets to achieve financial goals.
- **Reports and Analytics**: Generate detailed financial reports and analytics.
- **Prediction and Insights**: Provides predictive visualizations and insights using machine learning models.
- **Cloud Integration**: Utilizes AWS services for secure data storage and processing.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/tanmayr71/WealthWave.git

2.	Navigate to the project directory:
   ```bash
   cd WealthWave
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

Run the application:
```bash
python app.py
```
Access the application in your web browser at `http://localhost:5000`.

## Project Structure

- **app.py**: Main application file.
- **templates/**: HTML templates for the web interface.
- **static/**: Static files (CSS, JavaScript).
- **requirements.txt**: List of dependencies.
- **AWS/**: AWS configuration and deployment scripts.
- **Documentation/**: Project documentation files.

## Application Architecture

- **Frontend**: Utilizes Flask, hosted on AWS Elastic Beanstalk with Elastic Load Balancing and Auto Scaling.
- **Authentication**: Amazon Cognito for secure user signup/login and session management.
- **Routing**: Amazon Route 53 for domain management and request routing.
- **Data Management**: DynamoDB for storing structured bill data, managed through CRUD operations with Lambda functions.
- **Analytics**: Lambda functions analyze bill and transaction data, with reports and pie charts displayed on the "Analytics" page.
- **Reports**: Automated email reports via Lambda and Amazon SES.
- **Prediction and Insights**: Predictive visualizations using machine learning models for expense forecasting.
- **Storage**: Amazon S3 for storing bill images and user profile pictures.
- **Text Extraction**: Amazon Textract for extracting text from bill images.
- **API Gateway**: Configured resources within an API gateway for dedicated endpoints.
- **GPT Integration**: AI-driven insights and categorization of financial data.

## Technologies Used

- **Python**: Backend logic.
- **Flask**: Web framework.
- **HTML/CSS/JavaScript**: Frontend.
- **AWS**: Cloud services (Elastic Beanstalk, Route 53, Cognito, DynamoDB, S3, Textract, Lambda, SES, API Gateway).
- **GPT**: AI-driven insights.

## Abstract

WealthWave leverages cloud computing and advanced natural language processing to revolutionize personal finance management. Integrating AWS services with GPT's AI capabilities, it offers a cutting-edge approach to automate bill digitization and enhance financial analysis. This project addresses challenges like manual bill entry and inadequate expense insights, providing a seamless, intelligent solution.

## Problem Statement

Personal finance management faces a critical challenge in tracking and effectively categorizing expenses for insightful analysis. Traditional financial tools often lack sophistication, making it difficult for individuals to analyze their expenses meaningfully, thereby hindering effective financial planning and budgeting. WealthWave addresses this need by offering an advanced solution for automated expense tracking and intelligent categorization, providing users with valuable insights into their financial behavior.

## Motivation

WealthWave aims to enhance personal finance management through technological innovation. As financial transactions become increasingly digital and diverse, traditional tools fall short in providing comprehensive and insightful analysis. WealthWave leverages cloud computing and AI, including GPT's language processing capabilities, to bridge this gap. It offers an intelligent, automated system for digitizing bills, categorizing expenses, and delivering actionable financial insights.

## Design and Architecture

WealthWave's architecture showcases a comprehensive use of AWS services, aligning with modern cloud computing practices for robust and scalable personal finance management.

### Key Components and Their Roles:

![image](https://github.com/tanmayr71/WealthWave/assets/55703966/87a2e8c2-4a39-40d3-b33f-41158b4eb562)


- **AWS Lambda**: Processes data and interfaces with DynamoDB, chosen for scalability and serverless management.
- **Amazon S3**: Stores bill images and user profile pictures for secure and accessible data storage.
- **Amazon Textract**: Extracts text from bill images, integrated with GPT for detailed insights.
- **Amazon API Gateway**: Manages API calls and throttles requests to control usage.
- **Amazon DynamoDB**: Stores user data, user preferences, and transaction records, integrated with DAX for faster data retrieval.
- **Elastic Load Balancing and Auto Scaling**: Manages user traffic and scales resources as needed.
- **Flask Web Framework**: Serves as the backbone for the WealthWave web application.
- **GPT Integration**: Provides AI-driven insights and categorization of financial data.
- **Amazon ElastiCache (Redis)**: Enhances data retrieval speed, particularly for user profile pictures.
- **Amazon Cognito**: Manages user authentication and authorization.
- **Amazon Route 53 and AWS Certificate Manager**: Handles domain management and SSL/TLS certification.
- **Amazon EventBridge Scheduler**: Automates the sending of email reports based on user preferences.
- **Amazon SQS**: Handles data export requests, processed and sent via Amazon SES.
- **Amazon Simple Email Service (SES)**: Sends emails within WealthWave, delivering exported data and scheduled reports.
- **AWS Secrets Manager**: Securely stores and manages sensitive information, such as API keys.

## Implementation

WealthWave's development involved setting up and configuring a suite of AWS services, establishing a secure and scalable cloud environment, and integrating services like Lambda, DynamoDB, S3, and Textract. The Flask web application serves as the user-facing component, developed for a responsive and intuitive user interface. The application was deployed using Elastic Beanstalk for efficient management and scaling.

### Workflows:

- **Landing Page**: User-friendly and informative gateway for user interaction.
- **Sign In/Up**: Secure authentication using AWS Cognito.
- **Upload Bill**: Bill image upload and processing using Amazon Textract and GPT.
- **Analytics**: Data aggregation, analysis, and visualization.
- **Predictions**: Forecasting future expenses based on historical data.
- **Export Data**: Data export and email delivery.
- **Settings**: User profile and preference customization.
- **Logout**: Secure session termination.

## Challenges Encountered and Resolutions

The team faced and overcame several challenges, such as structuring bill data, integrating AWS Cognito, handling DNS and hosting adjustments, processing bill images under varying conditions, managing LLM API costs, and integrating predictive analytics.

## Future Enhancements

WealthWave aims to incorporate more advanced AI algorithms, improve the user interface, introduce a broader range of financial tools, enhance real-time data processing, add community features, and implement stronger security measures.

## Contributing

We welcome contributions! Please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## References

1. [AWS Documentation](https://docs.aws.amazon.com/)
2. [Amazon Cognito](https://aws.amazon.com/cognito/)
3. [Amazon Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/)
4. [AWS Certificate Manager](https://aws.amazon.com/certificate-manager/)
5. [Amazon ElastiCache](https://aws.amazon.com/elasticache/)
