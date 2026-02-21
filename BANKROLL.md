# 💵 BANKROLL — Purse Management & Risk Protocol

## Structure

```
STARTING PURSE: $[USER_DEFINED]
BET STRUCTURE: Full purse, every bet
PROGRESSION: Double on win, reset on loss
TARGET: 6 consecutive wins (64x return)
```

## The Martingale Ladder

| Bet # | Wager | Return if Win | Cumulative Multiple |
|-------|-------|--------------|-------------------|
| 1 | $500 | $955 | 1.9x |
| 2 | $955 | $1,819 | 3.6x |
| 3 | $1,819 | $3,456 | 6.9x |
| 4 | $3,456 | $6,566 | 13.1x |
| 5 | $6,566 | $12,475 | 24.9x |
| 6 | $12,475 | $23,703 | 47.4x |

*At -110 standard vig. Adjust for actual odds obtained.*

**Better odds improve everything.** If we can get -105 or even money on any bet, the math improves significantly. Always shop for the best line across books.

---

## Risk Budget

### Per-Attempt Risk
One starting purse ($500 example). This is the MAXIMUM we lose on a failed attempt.

### Total Campaign Budget
```
CONSERVATIVE: 5 attempts = $2,500 total risk
MODERATE: 10 attempts = $5,000 total risk  
AGGRESSIVE: 15 attempts = $7,500 total risk

EXPECTED ATTEMPTS TO HIT (at 65% per bet):
  Mean: ~13 attempts
  Median: ~9 attempts
  25th percentile: 5 attempts (lucky)
  75th percentile: 18 attempts (unlucky but normal)
```

### Stop-Loss Rules
```
HARD STOP: After [USER_DEFINED] consecutive failed attempts (suggested: 10)
  → Full system review
  → Recalibrate all models
  → Consider if per-bet edge estimate was wrong
  → Only resume if clear fix is identified

SOFT STOP: After 5 consecutive failed attempts
  → Postmortem on all 5
  → Check if losses were process failures or variance
  → If process is clean: continue (variance is expected)
  → If process failures found: pause, fix, resume
```

---

## Line Shopping Protocol

Before placing any bet, check lines at:
1. Best available legal sportsbook (compare 3+ books)
2. Record the line we actually get
3. Note closing line for CLV tracking

```
PRIORITY: Getting the best number > speed of execution
  A half-point can mean the difference between a push and a loss.
  
  If our target is Team +5.5 and one book has +6:
  → Take +6. That half point has significant value.
  
  If our target is Team +5.5 and best available is +5:
  → Reassess. One full point worse than target.
  → If conviction is still ≥ 9/14: Proceed at +5
  → If conviction drops below 9/14 at the worse number: PASS
```

---

## Timing Protocol

```
IDEAL BET PLACEMENT: Between T-60min and T-30min

WHY NOT EARLIER:
  - Late news can change everything
  - We want maximum information before committing
  
WHY NOT LATER:
  - Lines can move against us in final minutes
  - Books may limit bet sizes close to tip
  - We need time to shop lines

EXCEPTION: If we identify a line that will move against us
  (steam move incoming, breaking news), place immediately
  to capture the better number.
```

---

## Record Keeping

### Per-Bet Log
```
DATE:
GAME:
PICK:
LINE OBTAINED:
CLOSING LINE:
CLV: [+/- points]
BET AMOUNT:
RESULT: [W/L/P]
PAYOUT: [Amount]
NEW PURSE:
STREAK: [X/6]
CONVICTION SCORE: [X/14]
NOTES:
```

### Season Dashboard
```
TOTAL BETS:
RECORD: [W-L]
WIN RATE:
ROI:
AVG CONVICTION SCORE:
AVG CLV:
STREAK ATTEMPTS:
BEST STREAK:
CURRENT STREAK:
TOTAL INVESTED:
TOTAL RETURNED:
NET P/L:
```

---

## Emotional Discipline Rules

```
1. AFTER A WIN: You are not a genius. The system worked. Stay humble.
2. AFTER A LOSS: You are not an idiot. Variance happened. Stay process-focused.
3. AFTER 3 LOSSES: Review process. If clean, continue. If not, fix.
4. WHEN TEMPTED TO BET WITHOUT FULL CONVICTION: Walk away from the screen.
5. WHEN SOMEONE SAYS "LOCK OF THE CENTURY": That's noise. Run your system.
6. WHEN THE PURSE IS LARGE (bets 4-6): Do not let the dollar amount change your process.
   $6,000 gets the same analysis as $500. The system is the system.
```
