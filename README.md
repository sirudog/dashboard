# Healthchecks.io Status Dashboard

A standalone dashboard page showing the status of the checks in your [Healthchecks.io](https://healthchecks.io)
account.

[See a live example dashboard here](https://cuu508.github.io/).

* Single page, no external dependencies.
* Plain HTML, JS and CSS. Fork it and hack on it – no build tools or dev environment needed.
* Live-updates every 5 seconds.
* Can display checks from multiple projects.
* Uses Healthchecks.io read-only API keys, does not expose ping URLs.


## Dark Theme

![Dark THeme](/docs/theme-dark.png?raw=true "Dark Theme")

## Light Theme

![Light THeme](/docs/theme-light.png?raw=true "Light Theme")


## How To Use

* Fork the repository.
* Edit `index.html` and replace the API keys in `<h1>` tags. Be sure to use the
**read-only** API keys!
* Optionally, you can tweak the colors, font sizes and layout.
* Publish the `index.html` file to a web server (Github pages, S3 bucket.
Netlify, ...), or simply open it as a local file in your browser.

## Security

If you decide to make your dashboard public, your read-only API key will
become public as well. Using the read-only API key, anybody can fetch basic information
about checks in your project. This includes, for each check:

* name, **tags and description** (even though tags and descriptions are currently not
being shown on the dashboard)
* check's schedule (period, grace time, cron expression + timezone)
* current status (new / up / down / paused)
* precise time of the last ping
* precise time of when the next ping is expected
* total number of pings the check has received

Here are the things that the read-only API keys *cannot* do:

* the ping URLs are not exposed. You are not risking unexpected pings from random visitors
* no write access: cannot update or delete the existing checks, cannot create new checks
in your project
