# ticket-alerts

State store for a scheduled Claude Code cloud routine that watches
https://charities.ticketsforgood.co.uk for new events matching saved
filters (Premier League: Gillingham, Tottenham; a list of music artists)
and emails matches to nmarchant@ri.ac.uk.

`seen_events.json` — event IDs already notified on, keyed by event ID.
The routine reads this file, diffs the current listing against it, emails
any new matches, then commits the updated file back to this repo.
