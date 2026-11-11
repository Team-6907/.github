# Security Policy 安全策略

This policy covers every repository in the Team-6907 organization.

## Reporting a vulnerability 报告漏洞

Email [contact@team6907.org](mailto:contact@team6907.org). Please do not open a
public issue or pull request for a security problem.

Include, as far as you can:

- the repository and the file, URL or commit involved;
- what an attacker could do, and the steps to reproduce it;
- how we can reach you for follow-up questions.

We are a student team, so a reply can take a few days, longer during
competition weeks.

## Accidentally committed secret 误提交了密钥

If a password, API key, token or other credential ends up in a commit, in any
branch, even for a minute:

1. **Rotate first.** Revoke or regenerate the credential at its provider right
   away. Treat it as compromised from the moment it was pushed; deleting the
   commit does not undo the exposure.
2. **Report it.** Tell a software lead, or email
   [contact@team6907.org](mailto:contact@team6907.org), with the repository and
   the commit. Do not paste the secret itself into the message.
3. **Then remove it.** Take it out of the code and, together with a software
   lead, decide whether the history needs to be rewritten.
4. **Prevent a repeat.** Read the value from an environment variable and commit
   only a placeholder file such as `.dev.vars.example`.

先作废并更换密钥，再清理代码和历史记录；只删除提交并不能消除泄露。

## Scope 范围

Robot code from past seasons is archived and kept for reference only; it does
not receive fixes. Reports about our website and other live services are
especially welcome.
