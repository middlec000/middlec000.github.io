<div align="center">
  <img src="World_Time_Zones_Map.png" alt="Time Zones of the World">
  <div align="center">
    World Time Zones Map. <a href="https://en.wikipedia.org/wiki/File:World_Time_Zones_Map.png">Source</a>
  </div>
</div>

---

# Why Everyone Should Use UTC with Region-Specific Business Hours

## What is UTC?

Coordinated Universal Time (UTC) is the current global standard clock that all timezone-specific clocks are based on. Digital devices already use UTC under the hood by tracking time in UTC, then calculating the local time by adding or subtracting a certain number of hours determined by your time zone. Almost all people use the timezone-specific clock time, not UTC.

If you want more history, [here](https://en.wikipedia.org/wiki/Coordinated_Universal_Time) is the Wikipedia page.

## Motivation

I work remotely for a company headquartered in a timezone with a 3 hour difference from my own. My fellow coworkers are spread across the globe, some with a 13 hour time difference. Every time I want to schedule a meeting with someone outside of our digital calendar, we have to specify which timezone we are using as the reference and do mental math each time we go back and forth proposing different times. Admittedly this is not much effort, but it adds up over everyone communicating with anyone else in a different time zone. There is also a high risk of miscommunication if someone forgets to reference the timezone - did you mean your time or mine?

## Proposed New System

I, along with many others, think everyone should use UTC. I add a few additional details here that I have not seen others discuss in an attempt to ease the transition from current state to future state and to fill a few gaps in a UTC-only system.

The system I propose is this:

1. In situations where a specific time is needed, use UTC.
1. In situations where a convenient time for someone must be assumed, use a business hours or daylight hours lookup table (stored in UTC).
1. In situations where time is used as a cultural or contextual que, use the cultural or contextual que directly.

## Argument

To convince you to use this new system, I will compare the currently widespread timezone method of tracking and communicating about time to this new system within each type of situation outlined above. In each case, the new method is at least as good as the current method. By "good" I mean easier and clearer. I will present the general points and then give some examples.

### Specific Time Needed

This category includes all situations where a specific time is being communicated and no assumptions about what is convenient for others need to be made.

#### Point 1: UTC is more Efficient

UTC requires less effort/information when specifying a time across timezones and requires the same amount within a timezone.

| Example | Situation         | Conventional                                         | Proposed                     | Explanation                                                                                |
| ------- | ----------------- | ---------------------------------------------------- | ---------------------------- | ------------------------------------------------------------------------------------------ |
| 1       | Across Timezones  | Let's meet at 17:00, <timezone-specifier>, on day X. | Let's meet at 8:00 on Day X. | You must specify a timezone to be precise when communicating with the conventional system. |
| 2       | Within a Timezone | Let's meet at 17:00.                                 | Let's meet at 8:00.          | Same amount of information required.                                                       |

#### Point 2: UTC is less Risky

UTC is more difficult to get wrong, meaning it's lower risk. Using the conventional system can easily result in miscommunication when communicating across timezones or around daylight savings clock changes.

| Example | Situation                                             | Conventional                  | Proposed                     | Explanation                                                                                                          |
| ------- | ----------------------------------------------------- | ----------------------------- | ---------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| 1       | Across Timezones                                      | Let's meet at 17:00.          | Let's meet at 8:00.          | If a timezone is not specified using the conventional system, the time could be any of the participants' local time. |
| 2       | A Daylight Savings Time Change will Occur at Midnight | Let's meet at 17:00 tomorrow. | Let's meet at 8:00 tomorrow. | UTC does not change with daylight savings - it is standard for everyone.                                             |

### Assume Convenient Time

This category includes all situations where one party must assume a reasonable or convenient time for another party.

## Additional Notes

While poking around Google Scholar on this topic, I found several papers describing the economic benefits of effectively building a round-the-clock production cycle by coordinating production across the globe. Companies that produce digital products have organized teams that hand off their project at the end of their work day to another team in a different location that is just starting their work day. See [this](https://mpra.ub.uni-muenchen.de/78779/1/MPRA_paper_78779.pdf) review of literature for more. Note that this does not diminish my argument for UTC; coordination between these teams would be easier if they both used UTC.
