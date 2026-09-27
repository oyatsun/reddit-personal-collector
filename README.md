# Personal Reddit Technical Information Collector

This repository provides public documentation for a private,
non-commercial, self-hosted information collector.

The collector uses the Reddit Data API in read-only mode to retrieve
public technical information from a small, explicitly configured set
of communities.

Initial communities:

- r/StableDiffusion
- r/comfyui

## Purpose

The purpose of the application is to help me keep track of technical
developments related to generative image tools, including:

- model releases
- ComfyUI workflows
- bug fixes
- performance improvements
- benchmarks
- tutorials
- implementation notes
- other technically useful discussions

The system runs on my own private home server and is not offered as a
public or paid service.

## Reddit API Usage

The application is read-only.

It does not:

- post submissions
- post comments
- vote
- send private messages
- perform moderation actions
- interact with Reddit users

The collector may retrieve public fields such as:

- post ID
- title
- self-text
- creation time
- subreddit
- flair
- permalink
- outbound URL/domain
- score
- upvote ratio
- comment count

For selected posts that appear technically useful, the collector may
also retrieve a small number of top-level public comments, typically
3 to 5, to provide additional technical context.

## Processing

Retrieved posts are filtered locally to identify information relevant
to my personal technical interests.

For example, posts about:

- new models
- ComfyUI nodes and workflows
- technical releases
- bug fixes
- inference performance
- benchmarks
- implementation techniques

may be retained for personal reference.

Low-information content such as memes or generic showcases may be
filtered out.

Some selected content may be processed locally using an existing
language model for relevance classification and summarization.

Reddit data is NOT used to train, fine-tune, or create an AI/ML model
or training dataset.

## Data Handling

The application is intended to access only the minimum Reddit data
required for the described purpose.

The collector is designed to respect Reddit API rate limits and Reddit
content deletion requirements.

The production application source code, configuration, infrastructure
details, and API credentials are private because they are part of my
personal self-hosted environment.

No Reddit API credentials, access tokens, passwords, or other secrets
are stored in this public repository.
