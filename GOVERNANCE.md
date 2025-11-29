🇬🇧 [en](GOVERNANCE.md)&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;🇭🇺 [hu](GOVERNANCE.hu.md)

# Project Governance Model

## Contents

- [Leadership Model: BDFL + Code Owners](#-leadership-model-bdfl-code-owners)
- [Maintainers and Contributors](#-maintainers-and-contributors)
- [Decision-Making Process](#-decision-making-process)
- [Project Lifecycle and State](#-project-lifecycle-and-state)
- [Modifying This Governance Document](#-modifying-this-governance-document)

> **This document defines the governance structure of the project and the process by 
which decisions are made. Its purpose is to clearly specify who is authorized to 
maintain, direct, and ultimately make decisions about this repository and the 
associated project.**

## 🎩 Leadership Model: BDFL + Code Owners

The project follows a **[BDFL (Benevolent Dictator For 
Life)](https://en.wikipedia.org/wiki/Benevolent_dictator_for_life)** governance 
model.  This means that final authority over the project is held by:

1. **The repository owner**, and
2. **The code owners listed in the CODEOWNERS file**

Together, these individuals or teams constitute the "BDFL" for the project.

BDFLs have the authority to:

- define the strategic direction of the project,
- approve or reject pull requests,
- schedule releases,
- determine the project state (experimental, active, maintained, archived),
- overrule or amend contribution and operational guidelines,
- resolve disputes with final authority.

If the CODEOWNERS file contains only the repository owner, then the owner is the 
sole BDFL.

## 👥 Maintainers and Contributors

Contribution to the project is open to everyone, under the rules described in 
**[Contributing Guidelines](CONTRIBUTING.md)**.

Maintainers are responsible for:

- reviewing and triaging issues,
- reviewing pull requests,
- proposing and discussing technical changes,
- ensuring code quality,
- following the **[Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md)**.

Their decisions operate under the supervision of the BDFLs. If disagreements 
arise, the BDFLs make the **final decision**.


## 🧭 Decision-Making Process

Decision-making in this project is based on **rough consensus** and 
**best-effort collaboration**.

1. **Open Discussion** – In issues, pull requests, or GitHub Discussions.

2. **Maintainer Recommendation** – Maintainers review the matter and suggest a 
path forward.

3. **Decision**
   – If consensus is reached, maintainers merge or close the item.
   – If not, the BDFLs decide.

4. **Respectful Communication** – Decisions are always communicated clearly and 
respectfully.

## 🗂 Project Lifecycle and State

The project lifecycle follows the states defined in **[Project Lifecycle and 
Practices](PRACTICES.md)** guidelines:

- Experimental
- Actively developed
- Maintained
- Archived

The current state is determined by the BDFLs.

## 🔄 Modifying This Governance Document

Changes to this document:

- must be proposed through a pull request,
- must be reviewed by the code owners listed in CODEOWNERS,
- become effective **only with BDFL approval**.
