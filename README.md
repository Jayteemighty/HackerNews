# HackerNews - Tech News Aggregator

HackersFeed is a web application designed to streamline navigation through tech-related news from Hacker News. It provides an intuitive interface for browsing, searching, and filtering news items, along with the ability to add new items via an API. The project utilizes a combination of Next.js for the frontend and Django for the backend.

![Alt text](/docs-assets/image.png)

## Stack

- **Frontend**: Built using Next.js, a popular React framework for building modern web applications. It offers server-rendered React applications and features like server-side rendering, static site generation, and routing.

- **Backend**: Developed using Django, a high-level Python web framework that promotes rapid development and clean, pragmatic design. It includes powerful features such as an Object-Relational Mapping (ORM) system and built-in administrative interface.

## Getting Started

To run the HackersFeed application, you'll need to set up both the frontend and backend components. Follow the steps below to get started:

### Frontend

Before you start, make sure you have [Node.js](https://nodejs.org/) installed on your machine.

## Installation

1. Clone the repository and navigate to the frontend directory:

   ```bash
   cd frontend
   ```

## Preview
Below is a preview of how the HackersFeed web app looks:

![Alt text](/docs-assets/image.png)

News Detail
![Alt text](/docs-assets/image-2.png)

Search page
![Alt text](/docs-assets/image-1.png)

### Backend

Before you start, make sure you have the following software installed:

- [Python 3.9.6](https://www.python.org/downloads/release/python-396/)
- [PostgreSQL](https://www.postgresql.org/download/)
- [Redis](https://redis.io/download)


1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/Jayteemighty/HackerNews.git
   cd hackernews
   ```

2. Make sure you have Python 3.9.6 installed on your machine.

3. Install PostgreSQL and Redis: Install these prerequisites using the provided `setup_dependencies.sh` script if you are on a Mac.



4. Run backend.sh :

```bash
cd scripts
chmod +x backend.sh
./backend.sh
```
5. Run Celery workers and beat:

   ```bash
   python -m celery -A hackersfeed_api worker & python -m celery -A hackersfeed_api beat
   ```

   This will start Celery workers and beat for background tasks.

6. To start the redis server manually:

   ```bash
   redis-server
   ```

To run the tests:
   ```bash
      python manage.py tests
   ```
## Features

- **Scheduled Sync**: The backend includes a scheduled job that syncs published news items from the Hacker News API every 5 minutes.

- **News Listing**: The frontend provides a view to list the latest news items, with options to filter by item type and search by text.

- **Post jobs and tech stories around you**: Showcase job opportunities or share your own tech-related stories within the community. Create posts to connect with like-minded individuals and explore new opportunities in the tech world.

- **Anonymous Commenting**: Engage in discussions freely with the ability to leave anonymous comments on news items. Share your thoughts without the need to reveal your identity.

- **API**: The application exposes an API with endpoints to list items, apply filters, and add new items.



## Get Involved

Contributions to HackerNews are welcome! Feel free to fork the repository, make improvements, and submit pull requests. If you have any questions or feedback, please don't hesitate to reach out.

