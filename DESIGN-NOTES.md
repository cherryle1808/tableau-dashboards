# Design Notes

Who the dashboard is for, why the layout stays simple, and why each chart
type was chosen.

## Target Audience

**Persona:** Sarah Flower, 36, newly appointed Marketing Manager at GoodNews
National Bookstore.

Not a data analyst — a time-pressed business stakeholder who needs to:
- Gauge how severe the sales decline is, quickly
- Identify which segments to prioritize for recovery
- Bring evidence, not raw numbers, into a CEO/Board conversation

The dashboard is built for someone skimming it before a meeting, not
someone digging through 29 columns of transaction data.

## Why the Design Stays Simple

- **One decision flow, not a data dump** — sections follow Sarah's actual
  questions in order: overall health → which segments → when/how to act
- **Sales and the 4Ps stay the focus** — anything that doesn't inform that
  decision (e.g. payment method, gift wrap fees) was left out
- **Minimal color** — reserved for signaling decline (red), not decoration
- **Interactivity over more charts** — segment/year filters give a headline
  view and a drill-down view without cluttering the screen

## Chart Selection Rationale

| Section | Chart Type | Why |
|---|---|---|
| Health Check | KPI cards (big number + YoY %) | Instant "good vs. bad" recognition — no time needed to interpret |
| Segment Performance | Comparison table (2024 vs. 2025) | Precise multi-metric comparison a bar chart would compress — lets Sarah quote exact figures |
| Monthly Performance | Line chart, single color, filters | Standard for trend/seasonality; one color avoids "color = category" confusion, segment comparison handled by the filter |
| 4Ps inputs (category, price, location, promotion) | Horizontal bar charts, % labels | Ranked data reads faster as bar length than pie angles |

## Data Ethics Considerations

- Synthetic dataset — no real customers, stores, or purchases
- No personally identifiable information, only segment-level classifications
- Axes aren't truncated; % labels shown alongside raw counts to avoid misleading scale
- Segment labels are broad classifications, not individual profiles
