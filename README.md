# Jadlis-Advisor-MomTest

Customer discovery conversation advisor based on **The Mom Test** by Rob Fitzpatrick (2013).

## What it does

Teaches Claude to conduct customer conversations that produce reliable signal instead of false positives. Overrides Claude's default tendency to generate opinion-seeking and hypothetical questions ("Do you think it's a good idea?", "Would you buy X?") with Mom Test-passing procedures.

## 7 Modes

| Mode | Situation | What advisor does |
|------|-----------|-------------------|
| **Prep** | Before a conversation | Generates 3 big questions + scary question + target commitment |
| **Review** | After a conversation | Classifies signals (fact/compliment/fluff/idea), checks commitment, binary verdict |
| **Question** | Designing questions | Filters through 3 Mom Test rules, rewrites failing questions |
| **Signal** | Interpreting a response | Classifies bad data type, provides recovery script (deflect/anchor/dig) |
| **Segment** | Finding who to talk to | Customer Slicing algorithm → who-where pairs |
| **Meeting** | Arranging conversations | VFWPA framing formula, Advisory Flip, casual vs formal |
| **Commitment** | Evaluating a lead | Commitment currencies, zombie/earlyvangelist classification |

## Installation

```bash
claude plugin install jadlis-advisor-momtest@jadlis-advisors
```

Or local:

```bash
claude --plugin-dir /path/to/Jadlis-Advisor-MomTest
```

## Usage

```
/jadlis-advisor-momtest:advisor
```

Then describe your situation — the advisor detects the appropriate mode automatically.

## The Mom Test — 3 Rules

1. Talk about their life instead of your idea
2. Ask about specifics in the past instead of generics or opinions about the future
3. Talk less and listen more

## Source

Rob Fitzpatrick. *The Mom Test: How to talk to customers and learn if your business is a good idea when everybody is lying to you.* 2013.

## License

Content derived from The Mom Test by Rob Fitzpatrick. Plugin structure and advisor logic by beCyborg.
