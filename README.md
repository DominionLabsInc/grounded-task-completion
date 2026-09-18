# Task Completion as an Internal, Grounded Judgment

**An agent is done when it believes, past its own calibrated doubt, that the goal now holds in the world,
not when a procedure returns success.**

Stefan Ragland, Dominion Labs Research & Development. Published 14 October 2025.

- Paper (PDF): [`paper/grounded-task-completion.pdf`](paper/grounded-task-completion.pdf)
- Paper (web): <https://dmnlabs.org/research/grounded-task-completion/>
- Contact: research@dmnlabs.org

## The argument

"The agent said it succeeded" and "the world is now in the intended state" are different claims, and any
completion signal derived from a code path finishing measures the first while reporting the second. The
paper makes completion a per-task belief that must survive the agent's own doubt, formed from two
epistemically distinct kinds of evidence: what the action runtime reported it did, and what an
independent re-measurement of the world now shows. Correlated confirmations of a single observation
cannot masquerade as independent proof.

A single confirmation is insufficient (posterior about 0.72); action plus an independent observation is
accepted (about 0.975); a fabricated success collapses (about 0.30). On a nine-task suite including three
tools that report success while changing nothing, the mechanism recorded zero false completions and zero
false incompletions.

## Who closes the pursuit

Deciding whether a goal holds is one half; recording that judgment against the task's intent is the
other. The rule is that the execution path which owns a pursuit closes its intent exactly once, from the
re-observed world.

| What was tested | Result | Data |
|---|---|---|
| Seven ownership cases, each dispatched the way production dispatches it | 27 of 27 checks passed, 18 September 2026 | [`data/reconcile-01.json`](data/reconcile-01.json) |

Two cases carry the argument. An operation that acted on the wrong destination has its rule confirmed and
its pursuit closed as **missed**, because the re-observed world decides rather than the step's own account
of itself. An operation that was refused before it ran still closes its pursuit, as missed, with the
refusal as the reason: an intention dropped silently is indistinguishable later from one never formed.

## Citation

```bibtex
@techreport{ragland2025completion,
  title       = {Task Completion as an Internal, Grounded Judgment},
  author      = {Ragland, Stefan},
  institution = {Dominion Labs},
  year        = {2025},
  month       = {10},
  url         = {https://dmnlabs.org/research/grounded-task-completion/}
}
```

## License

The paper and the data are released under [Creative Commons Attribution 4.0](LICENSE). Please cite the
paper if you use them.
