# 🏀 MEDALLION COURT — Sports Betting Intelligence System

## Quick Start

Upload these files into your OpenClaw bot's brain/knowledge base:

```
BRAIN.md              ← Master orchestrator (load FIRST)
STRATEGY.md           ← Playbook and decision rules
BANKROLL.md           ← Purse management and risk protocol
SUB_LINES.md          ← Line movement tracking agent
SUB_MONEY.md          ← Betting/money percentage analysis
SUB_NEWS.md           ← News, injuries, rest, travel intel
SUB_QUANT.md          ← Quantitative models & Monte Carlo
SUB_CONTRARIAN.md     ← Contrarian value scoring
SUB_PSYCHOLOGY.md     ← Vegas trap detection
SUB_SITUATIONAL.md    ← Schedule spots and situational edges
SUB_HISTORY.md        ← Historical validation and backtesting
```

## Architecture

```
                    ┌─────────────────┐
                    │   MEDALLION     │
                    │   COURT BRAIN   │ ◄── Reports to Doug
                    │   (BRAIN.md)    │
                    └────────┬────────┘
                             │
              ┌──────────────┼──────────────┐
              │              │              │
     ┌────────┴──┐  ┌───────┴───┐  ┌───────┴──────┐
     │ STRATEGY  │  │ BANKROLL  │  │ SUB-AGENTS   │
     │ Playbook  │  │ Risk Mgmt │  │ (7 agents)   │
     └───────────┘  └───────────┘  └───────┬──────┘
                                           │
                    ┌──────────────────────┬┴┬─────────────────────┐
                    │          │          │  │         │           │
               ┌────┴───┐ ┌───┴──┐ ┌────┴┐ │  ┌──────┴──┐ ┌─────┴────┐
               │ LINES  │ │MONEY │ │NEWS │ │  │CONTRARY │ │PSYCHOLOGY│
               └────────┘ └──────┘ └─────┘ │  └─────────┘ └──────────┘
                                    ┌──────┴──────┐  ┌──────────┐
                                    │ SITUATIONAL │  │ HISTORY  │
                                    └─────────────┘  └──────────┘
                                           │
                                      ┌────┴────┐
                                      │  QUANT  │
                                      │ (10M MC)│
                                      └─────────┘
```

## Daily Workflow

1. **Morning**: All agents scan today's slate
2. **Midday**: Hypothesis board built for promising games
3. **T-2 hours**: All agents refresh with latest data
4. **T-30 min**: FINAL DECISION — all agents vote, Brain tallies conviction
5. **Execute or Stand Down**: Threshold is 9/14. No exceptions.

## Conviction Voting System

Each of the 7 sub-agents votes on the proposed bet:
- **STRONG YES**: +2 points
- **YES**: +1 point
- **NEUTRAL**: 0 points
- **NO**: -1 point
- **STRONG NO**: -2 points (also triggers automatic veto)

**Maximum**: +14 | **Minimum to bet**: +9

## Configuration

Set these values in BRAIN.md before first use:
- `STARTING PURSE`: Your initial bet amount
- `CURRENT STREAK`: 0/6
- `ATTEMPT`: 1

## Important Disclaimer

This is a decision-support system, not financial advice. Sports betting involves
significant risk of loss. Past patterns do not guarantee future results. Only
wager what you can afford to lose entirely. Gambling can be addictive — if you
or someone you know has a gambling problem, call 1-800-522-4700.
