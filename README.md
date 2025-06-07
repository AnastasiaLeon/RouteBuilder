# RouteBuilder
Console application for finding routes between cities using Yandex API

## Description

A console application for finding routes from Saint Petersburg to Nizhny Novgorod and back, using Yandex API and third-party libraries.

The application searches for possible routes between Saint Petersburg and Nizhny Novgorod (round trip) with no more than 1 transfer using any available transport for a specified date. Intermediate results are cached in memory and on the filesystem to reduce the number of requests to the external API (data expires after 24 hours)

## Источник данных

The application uses [Yandex Schedule API](https://yandex.ru/dev/rasp/doc/ru/). The free tier is limited to 500 requests per day.

## Implementation Details

- HTTP requests are handled using the [С++ Requests (CPR) library](https://github.com/libcpr/cpr). 
- JSON responses are processed using [nlohmann/json](https://github.com/nlohmann/json).

## Example Usage

./bin/RouteBuilder "to Nizhniy Novgorod" 2025-03-01

./bin/RouteBuilder "to Saint Petersburg" 2025-03-01

## Key-Features

- Round-trip route search (SPb ↔ Nizhny Novgorod).
- Max 1 transfer allowed.
- In-memory & filesystem caching (24-hour TTL).
- Rate-limited API usage (500 requests/day).