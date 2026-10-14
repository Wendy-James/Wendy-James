# Public portfolio evidence & safety policy

The public profile is a **selective evidence index**, not a mirror of private work.

## Before publishing or synchronizing any material

1. **Ownership:** confirm the source is individually owned and permitted for redistribution. Employer-owned code, SQL, internal business schemas and data, metrics, identifiers, screenshots, model weights and credentials are not public portfolio material.
2. **Identity/privacy:** only use the display name **Wendy / Wendy-James**. Do not introduce legal names or identifying personal details into profile, site titles or public project showcases.
3. **Reproducibility:** link to actual source, tests, commands, pinned revisions and measurements. State data type, hardware and evaluation split. Separate pilot/toy tests from real training and production outcomes.
4. **Claim status:** use **complete** only for tested deliverables; use **ongoing** or **planned** otherwise. Keep negative results, failure analysis and limitations visible.
5. **Research release:** unpublished manuscripts, private human evaluations, intermediate generations, unpublished datasets, checkpoints and embargoed results stay private until an explicit release review.
6. **License/provenance:** check and credit open-source dependencies, model licenses and dataset use terms.
7. **Publication audit:** scan new files/patches for secrets, internal identifiers and personally identifying information; inspect Git history and public mirrors when a potential disclosure is discovered.

## Escalation for potential leaks

- Stop any automated publication job that may continue to copy the material.
- Ask for a review of disclosure permissions and follow relevant employer/security processes.
- Removing an item from the repository's current branch **does not erase previous commits, forks, caches or archives**. Do not force-rewrite public history without owner approval and a remediation plan.
- Do not paste suspected sensitive excerpts into public issues, pull requests, or analysis documents.

## Evidence standards used on this profile

- **Foundation model engineering:** config, correct implementation, shape/numerical tests, fixed seeds, loss curves, benchmark protocol and hardware.
- **Post-training research:** hypotheses, fixed budget, independent verifier agreement, train/eval splits, uncertainty, null results and dataset/model revisions.
- **Open source contributions:** reproducible upstream issue, maintainer review and honest merged/not-merged status.
- **Hugging Face:** only approved model/dataset/Space artifacts with model/data cards, license and evaluation link, never automatically upload private weights.

This policy describes intended publishing rules; it does not certify that historical content was always compliant.
