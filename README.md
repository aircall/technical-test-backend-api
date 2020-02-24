# Aircall Technical Test / Backend API
The goal of this test is to evaluate your ability:
- to architecture a simple but reliable backend application,
- to process data and compute metrics,
- and to build a JSON API delivering these metrics.

## Instructions

For an organisation of your choice on GitHub (that has public repositories), you need to build an app that computes the number of monthly new contributors for each of those repositories, from the month of their creation until now.

A new contributor is someone who did a commit for the first time in a repository.

### 1. Homework
Build a **straightforward** application able to fetch data from GitHub API in a reliable and efficient way. You'll need to handle GitHub API errors and rate limit so that calls are retried properly.

Store the fetched data in a storage system of your choice (in-memory, filesystem, database, ...) and expose a HTTP JSON API delivering the results. The format of the API is the following (example with Facebook):

```json
//GET `/facebook/react/2019`
{
    "org": "Facebook",
    "repository": "react", 
    "year": "2019",
    "newContributors": ...,
}

//GET `/facebook/jest/2018`
{
    "org": "Facebook",
    "repository": "jest", 
    "year": "2018",
    "newContributors": ...,
}
```

```json
//GET `/facebook/react/2019/06`
{
    "org": "Facebook",
    "repository": "react",
    "year": "2019",
    "month": "06",
    "newContributors": ...,
}

//GET `/facebook/jest/2018/03`
{
    "org": "Facebook",
    "repository": "jest",
    "year": "2018",
    "month": "03",
    "newContributors": ...,
}
```

You can use any programming language and/or framework for this application as long as it's reliable, fault tolerant and efficient.
Make sure that you put the instructions on how to preview your application and run it, so that we can easily see the result.

You can access the GitHub API using your personal GitHub account. There are many ways to retrieve the needed data, choose the most simple one, you do not need to handle more than what is required for the app.

:warning: Do not fork this repository and do not submit any Pull Requests. :warning:

When you're done, please create your public or private repo on GitHub and give access to:
- [aherve](https://github.com/aherve)
- [kimious](https://github.com/kimious)

### 2. Technical Presentation (~1.5 hour)
Presentation of the whole project in English to 2 engineers.

## Questions
You can ask any questions at any time. Any feedback on the test itself is welcome.

Good luck!
