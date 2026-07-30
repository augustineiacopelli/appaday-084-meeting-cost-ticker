# AppADay 084 &middot; Meeting Cost Ticker

Watch the running dollar cost of a meeting climb in real time. Set the head count and an average hourly rate, or switch to **By Person** and enter each attendee's actual salary. Hit start and the ticker tallies the burn second by second.

**Live:** https://augustineiacopelli.github.io/appaday-084-meeting-cost-ticker/

## What it does

The ticker prorates cost to the second from whichever inputs you give it. In **Average rate** mode you enter how many people are in the room and a single average hourly rate. In **By Person** mode you add a row per attendee with their salary, marked either per year or per hour; annual figures are converted to an hourly rate at 2,080 work hours per year. Either way the big counter ticks up live while the panel below shows the per-minute and per-hour burn rate and the current head count, plus a light running tally of what the spend could have bought instead, from a coffee up through a weekend getaway.

Start turns into Pause and then Resume, so you can stop the clock without losing the total, and Reset zeroes everything and unlocks the inputs. The spacebar toggles start and pause when you are not typing in a field. Your last-used values are remembered on the device between visits.

## How it is built

A single self-contained `index.html` of vanilla HTML, CSS, and JavaScript. No frameworks, no build step, and no dependencies beyond Google Fonts. The counter is driven by `requestAnimationFrame` off a wall-clock timestamp rather than a drifting interval, so the total stays accurate across pause and resume. Inputs and last-used values persist in `localStorage`. Nothing is sent anywhere; all figures stay in the browser.

## Notes

Cost is an estimate. Hourly conversion of annual salaries assumes a 2,080-hour work year and does not account for benefits, overhead, or fully loaded labor cost, so treat the number as a rough, motivating signal rather than an accounting figure.

---

Part of [AppADay](https://augustineiacopelli.github.io/appaday/), one complete web app designed, built, and shipped every day.
