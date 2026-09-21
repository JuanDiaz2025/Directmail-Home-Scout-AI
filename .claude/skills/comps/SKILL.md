---
name: comps
description: Pull real sold comparables for a property address — 5 or more recent sales within about a mile — and turn them into a median $/sf and an indicated ARV. Use whenever someone gives an address and wants comps, an ARV, a value estimate, or "what's this worth". Output pastes straight into the Flip Underwriter calculator. Never invents a sale.
---

# Comps

Given a property address, find **real, sourced** recent sales near it and turn them
into an ARV.

The one rule that matters: **every comp must come from a page you actually
retrieved.** If you did not read it, it does not go in the table. Never fill a gap
with a plausible-looking address, price, size or date. A short table of real sales
is worth more than a long table with invented rows in it — the numbers here get
used to price cash offers to real sellers.

## What you need first

The subject address, and ideally its square footage. If the address is ambiguous
(no city, or a street name that exists in several cities), ask before searching —
comps for the wrong town are worse than none.

## Where the data actually is

Work down this list until you have five or more verified sales. Different metros
have different best sources, so try several.

1. **Local newspaper home-sales columns.** The most reliable structured source,
   because they publish per-sale articles with address, price, date, square
   footage, $/sf, beds, baths and year built — and each article usually lists
   three or four *more* nearby recent sales. In Sonoma County this is the
   Press Democrat (`pressdemocrat.com`, articles titled "Single-family home sells
   in <city> for $X"). Most metros have an equivalent; search
   `"<city>" home sales <month> <year> sold price square foot`.
2. **Listing aggregators' sold pages.** `homes.com/<city>-<state>/<zip>/sold/`,
   Zillow, Redfin, Realtor.com, Estately, Trulia sold/recently-sold pages. Search
   results often surface the individual sale details even when the page itself
   resists fetching. Try `site:homes.com <zip> sold` style queries.
3. **County assessor and recorder records.** Authoritative for sale price and
   date, usually thin on square footage and condition. Good for confirming a sale
   you found elsewhere.
4. **The subject property itself** — search it directly to pick up its square
   footage, beds, baths and year built for the calculator.

Fetch the promising pages rather than trusting a search snippet alone. Snippets
mix properties together and drop the address off the number more often than you
would expect.

## Choosing the comps

Rank by, in order: distance (inside a mile is the target), recency (last six
months is ideal, stretch to twelve if you must), then similarity in square
footage, beds and baths.

Say what you could not confirm rather than papering over it:

- If you cannot establish distance, put the neighborhood or ZIP in the distance
  column instead of a number — never guess a mileage.
- If a comp is outside a mile or older than a year, keep it if it is the best
  available but mark it.
- If you find fewer than five verifiable sales, hand over what you have and say
  so plainly. Do not pad the table.
- Flag any comp that looks like a flip, a teardown, or a non-arm's-length
  transfer — those distort a median badly.

## What to hand back

**1. The comps table.**

| Address | Bd | Ba | Sq ft | Sold | $/sf | Date | Distance | Source |
|---|---|---|---|---|---|---|---|---|

**2. The read.** Median $/sf across the comps you would actually count, the range,
and the indicated ARV (median $/sf × subject square footage). Note which comps you
would throw out and why — a 4,900 sq ft estate does not belong in the median for a
1,000 sq ft bungalow. Give the ARV as a range, not a single number.

**3. A paste block** for the Flip Underwriter calculator, one comp per line:

```
123 Example St, 3 bd, 2 ba, 1,450 sqft, sold $712,000, Aug 14 2026, 0.4 mi
```

That page's paste box reads this shape directly, and the calculator takes the
median $/sf from there.

**4. Sources.** Every URL you pulled a number from, as markdown links. Anyone
should be able to click through and check any row.

## Condition

Comps come from sold listings that were, in general, in retail condition. The
subject usually is not — that is the whole point of the deal. Say so: the ARV is
what the property is worth *after* the rehab, which is exactly what the
calculator's "Estimated sale price (ARV)" field wants. Do not discount it for
current condition; the rehab budget handles that.
