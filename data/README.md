# Data

`reconcile-01.json` is the run record written by the ownership study: seven cases, each dispatched the
way production dispatches it, with every check and its evidence.

| Field | What it carries |
|---|---|
| `summary` | checks run, passed, failed, and the outcome |
| `cases` | per case: what ran, how many times the intent was closed, and the status it closed with |
| `metrics` | the counts the claim rests on |
| `environment` | Python version and platform only |

One redaction, stated because a data file should say what was done to it: the environment block of the
original record also holds local filesystem paths, the database name, the operating-system user and a git
commit. Those are removed from this published copy. Nothing that carries a result was changed; the
checks, their evidence and the summary are exactly as the run wrote them.
