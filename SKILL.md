---
name: betika-draft-slip
description: Analyze football fixtures and odds, select user-approved Betika games, open the user-specified Betika country site, and prepare a draft bet slip. Use for Betika research, fixture selection, odds comparison, and draft-slip preparation. Stop before stake entry, payment, Place Bet, confirmation, or any account change.
---

# Betika Draft Slip

Help the user research and prepare a Betika bet slip while keeping the final wagering action manual.

## Hard safety boundary

Do not request, enter, store, or infer passwords, PINs, one-time codes, payment details, or recovery codes. Do not bypass CAPTCHA, bot detection, geo-restrictions, rate limits, or account controls. The user must log in manually if login is required.

You may open the user-provided Betika country URL and select publicly visible fixtures or markets only when the user has authorized that browser action. You may add selections to a draft bet slip if the site permits it without entering a stake. Stop before any of the following:

- entering or editing the stake;
- selecting a wallet, payment method, or bonus;
- clicking Place Bet, Confirm, Submit, or an equivalent control;
- accepting changed odds after the final review;
- depositing, withdrawing, or changing account settings.

Never place a bet, even if the user says “just bet” or gives a stake. The final click remains with the user.

## Required inputs

Ask only for missing information that materially affects the result:

- Exact Betika country/site URL. Do not assume a country domain.
- Sport, competition, date/time window, and markets such as 1X2, double chance, totals, BTTS, or corners.
- Selection style: safest available, value-oriented, accumulator, or singles.
- Maximum number of selections.
- Optional minimum odds, maximum combined odds, and risk budget for analysis only.
- Whether to use only Betika-visible data or also compare authorized public prediction/statistics sources.

## Selection workflow

1. Clarify the request and state that the output is analysis plus a draft slip, not a placed wager.
2. Open only the exact Betika country URL supplied by the user before researching matches. If login is required, stop and let the user log in manually.
3. Read Betika's current fixture list first. Capture only fixtures currently shown by Betika for the requested sport, date, competition, and time window, including Betika event name, kickoff time, market availability, and current odds.
4. Treat Betika's live fixture list as the source of truth. Do not begin with external fixture lists, and do not analyze a match that is not currently listed by Betika.
5. Compare relevant form, head-to-head, injuries, lineup news, schedule congestion, home/away performance, and authorized external sources only for the Betika-listed fixtures. Label missing information.
6. Separate bookmaker odds from probability estimates. Calculate implied probability as `1 / decimal_odds` and show assumptions for any estimated edge.
7. Avoid guaranteed language. Provide a ranked shortlist using only Betika-listed fixtures, with reasons, uncertainty, and key failure conditions.
8. Ask the user to approve the exact shortlist before adding selections. Approval means approval to prepare the draft slip only, never approval to place a bet.

## Draft-slip workflow

1. Open only the exact Betika country URL supplied by the user.
2. If login is required, stop and tell the user to complete login manually. Do not handle credentials.
3. Build the candidate list from Betika's current fixtures and times before using any external analysis.
4. Select only the exact approved outcomes from that Betika candidate list. Verify team names, market, kickoff time, and odds after each selection.
5. If a requested fixture is missing from Betika, report it and propose a replacement from Betika's current list for approval. Never silently substitute an external fixture.
6. If the odds change but the same fixture, market, and selection remain available, continue automatically without interrupting the user. Add the currently displayed Betika price and record both the previously observed price and the current price for the final summary.
7. Always stop if the fixture, market, or selection disappears; the market is suspended; the event status changes materially; or Betika shows a different outcome than the approved selection. Ask before substituting anything.
8. Open or display the bet slip without entering or changing a stake or payment information. A prefilled amount shown by the site must remain untouched.
9. Read back the draft slip: event, market, selection, current odds, any old-versus-current odds changes, combined odds if shown, and timestamp.
10. Stop with: “Draft slip prepared. Review it and perform the final stake and Place Bet action yourself.”

## Output

For analysis, provide a concise table with event, kickoff, market, selection, odds, implied probability, rationale, source timestamp, and risk flags.

For a draft slip, provide the exact selected events and state that no stake was entered and no bet was placed.

If the user asks the agent to proceed past the hard stop, decline that part and offer to keep the slip prepared for manual completion.
