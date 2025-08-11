# Creating an organisation

Create .github repo
Set rulessets  


Enforce branchings strategy  

| Strategy | Core Branches | Workflow (1-liner) | Pros | Cons | Best For | Complexity | Release Cadence | Parallel Maintenance |
|---|---|---|---|---|---|---|---|---|
| **Git Flow** | `main`, `develop`, `feature/*`, `release/*`, `hotfix/*` | Features → `develop`; cut `release/*`; merge to `main` + tag; hotfix from `main`. | Clear roles; supports multiple versions; structured. | Heavy; slower CI/CD; many merges. | Enterprises, planned releases, regulated teams. | High | Batch (scheduled releases) | Strong (multiple supported lines) |
| **GitHub Flow** | `main`, short-lived `feature/*` | Branch off `main`; PR; review/CI; merge & deploy. | Simple; fast; great for CD; easy onboarding. | `main` must always be releasable; needs solid tests. | Small/medium web services, startups. | Low | Continuous | Weak (usually single line) |
| **GitLab Flow** | `main` + (env branches like `staging`/`production`) or `release/*` | Merge via env or release branches; often issue-linked. | Flexible; maps to environments; less heavy than Git Flow. | Can drift without rules; merge discipline needed. | Teams with multi-env CI/CD pipelines. | Medium | Continuous or Batch | Medium (via release branches) |
| **Trunk-Based** | `main` (trunk) + very short feature branches | Tiny branches merged multiple times/day; use feature flags. | Minimal merge pain; fastest CI/CD; high throughput. | Requires strong tests, flags, and discipline. | High-velocity teams, product orgs. | Low–Medium | Continuous | Weak (prefer backports/flags) |
| **Release Branching** | `main`, `release/x.y`, `hotfix/*` | Cut `release/x.y`; stabilize there; maintain until EOL. | Clean isolation per release; easy patching. | Many long-lived branches; backports needed. | SDKs, libraries, long support windows. | Medium | Batch | Strong |
| **Feature Branching (standalone)** | `main` (or `develop`), `feature/*` | Work isolated per feature; merge when ready. | Isolation; review friendly. | Long-lived branches → big merges; slower integration. | Teams needing isolation without heavy process. | Medium | Continuous or Batch | Medium (depends on policy) |

Template repo  
Maybe Create needed branches according to branching strategy    
Use some tool for versioning  


