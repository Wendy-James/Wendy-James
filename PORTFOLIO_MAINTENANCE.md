# Portfolio maintenance standards

This repository is a **selective evidence index**, not a mirror of all work. Keep the English profile, Chinese profile, and linked public research site consistent.

## Weekly review

1. **Evidence freshness:** inspect the publicly visible branches, milestone reports, linked CSVs, reproducible commands, tests and open PR status. Update a completion claim only after public evidence is inspectable and actually supports it.
2. **Research narrative:** prioritize LLM Post-training × Agentic RL. Preserve the boundary between ongoing private work, verified public engineering results, and planned tool-use/RL experiments. Do not claim a submission, acceptance, or experimental gain without evidence and permission to publish.
3. **Privacy:** scan edited files, linked project READMEs, commit metadata and public site content for legal name, university identity, education dates, personal emails, locations and identifying images. Avoid putting sensitive strings into public automated workflows or commit messages.
4. **Ownership and licensing:** review the source and license of forks, upstream copies, datasets, evaluation harnesses and dependent models before featuring them as original work.
5. **Quality and navigation:** test links, broken anchors, mobile layout, status summaries, bilingual consistency and usefulness to research/ML hiring readers.
6. **Security:** never sync employer-owned source, schemas, data, keys, internal metrics, unreleased research or private experiment artifacts.
7. **Restraint:** do not make cosmetic commits to manufacture activity. If nothing has changed, record the audit privately and make no public commit.

## Status vocabulary

- **Completed:** implemented, tested, documented and supported by public inspectable evidence.
- **Draft / in progress:** under development; may include partial smoke tests but lacks full validation.
- **Private research:** work exists but is not publicly auditable; share no unapproved results or details.
- **Planned:** a research goal, not a shipping or performance claim.

## Release checklist

- [ ] New claim verified against its linked artifact and original source
- [ ] Metrics state dataset, split, baselines, hardware, limitations and negative results
- [ ] Upstream licenses and authors are credited
- [ ] Personal details and non-public resources excluded
- [ ] English/Chinese README and portfolio page tell the same story
- [ ] Links resolve and screenshots/metadata do not reveal identity
- [ ] No changes made solely for contribution-count optics

Never assume removing a current-branch reference erases prior public Git history, cached pages or forks. Escalate any suspected disclosure instead of rewriting history impulsively.
