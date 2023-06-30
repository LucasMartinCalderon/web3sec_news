# Web3Sec Podcast Summarizer

Welcome to the Web3Sec Podcast Summarizer's repository. This tool is a part of web3sec.news, the premier web3 security news aggregator. Web3Sec Podcast Summarizer allows users to search for any YouTube video, extract the entire transcript, condense it into a 5-minute summary, and deliver it straight to their inbox, all in an automated way.

## Table of Contents
1. [Features](#features)
2. [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installing](#installing)
3. [Usage](#usage)
4. [Running the Tests](#running-the-tests)
5. [Deployment](#deployment)
6. [Contributing](#contributing)
7. [License](#license)
8. [Acknowledgments](#acknowledgments)

## Features
- Search functionality for any video on YouTube, especially long-form podcasts
- Transcript extraction from YouTube videos
- Automated summarization into an easy-to-read, 5-minute bullet-point format
- Direct delivery of the summary to the user's inbox

## Getting Started
To get a local copy up and running, follow these simple steps.

### Prerequisites
Before you start, make sure your local system has the following installed:
- Python 3.7 or higher
- pip for installing Python packages
- Docker (recommended for deployment)

### Installing
1. Clone the repository to your local machine.

```bash
git clone https://github.com/Web3Sec/Podcast-Summarizer.git
```

2. Navigate to the project directory.

```bash
cd Podcast-Summarizer
```

3. Install the required Python packages

```bash
pip install -r requirements.txt
```

## Usage

1. Update the config.json file with your email settings and the YouTube API key.

```json
{
    "youtube_api_key": "YOUR_YOUTUBE_API_KEY",
    "email_settings": {
        "smtp_server": "SMTP_SERVER",
        "smtp_port": "SMTP_PORT",
        "username": "YOUR_USERNAME",
        "password": "YOUR_PASSWORD",
        "sender": "SENDER_EMAIL_ADDRESS",
        "receiver": "RECEIVER_EMAIL_ADDRESS"
    }
}
```

2. To run the summarizer, use the following command (replace "YouTube_Video_ID" with the ID of the video you want to summarize):

```python
python main.py "YouTube_Video_ID"
```

## Running the Tests

1. We use pytest for our testing framework. To run the tests, use the following command:

```python
pytest
```

## Deployment

For deployment, we recommend using Docker. here are the steps to build and run the Docker image: 

1. Build the Docker image:

```bash
docker build -t podcast-summarizer .
```

2. Run the Docker image:

```bash
docker run -d --name podcast-summarizer podcast-summarizer
```

## Contributing 

We appreciate contributions. Please read CONTRIBUTING.md for details on our code of conduct, and the process for submitting pull requests.

## Acknowledgements

* We extend our heartfelt gratitude to the open-source community, whose collective efforts have made this project possible.
* A big shout-out to the Web3Sec team for their continuous efforts in providing valuable tools to the community.
