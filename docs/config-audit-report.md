# Configuration Audit Report

> **Date:** 2026-03-03
> **Scope:** Merged host configuration files from hostconfig repository
> **Auditor:** Automated review during repo merge
> **Status:** 30 improvements identified, applied, and verified

---

## Summary

During the integration of the hostconfig repository into the master Syn_OS repo, a full audit was performed. Duplicate entries were removed, outdated configurations were updated, and 30 potential improvements were identified and applied.

---

## Improvements Applied

### SSH Configuration (ssh_config & sshd_config)

| # | File | Improvement | Priority |
|---|---|---|---|
| 1 | `ssh_config` | Removed deprecated `Protocol 1` references — enforced Protocol 2 only | 🔴 High |
| 2 | `ssh_config` | Added `KexAlgorithms` with modern key exchange (curve25519-sha256) — removed legacy diffie-hellman-group1 | 🔴 High |
| 3 | `ssh_config` | Added `HostKeyAlgorithms` restricting to ed25519 and rsa-sha2 — removed ssh-dss | 🔴 High |
| 4 | `ssh_config` | Added `Ciphers` whitelist (chacha20-poly1305, aes256-gcm) — removed arcfour, blowfish | 🔴 High |
| 5 | `ssh_config` | Added `MACs` restriction to etm variants — removed hmac-md5, hmac-sha1 | 🔴 High |
| 6 | `ssh_config` | Set `ForwardAgent no` as default — prevents agent hijacking | 🟡 Medium |
| 7 | `ssh_config` | Added `HashKnownHosts yes` — protects host list privacy | 🟡 Medium |
| 8 | `sshd_config` | Set `MaxAuthTries 3` (was 6) — reduces brute-force window | 🔴 High |
| 9 | `sshd_config` | Set `LoginGraceTime 30` (was 120) — reduces connection holding attacks | 🟡 Medium |
| 10 | `sshd_config` | Added `AllowAgentForwarding no` and `AllowTcpForwarding no` — reduces lateral movement risk | 🟡 Medium |

### Kernel Parameters (sysctl.conf)

| # | File | Improvement | Priority |
|---|---|---|---|
| 11 | `sysctl.conf` | Added `kernel.dmesg_restrict = 1` — restricts dmesg to root | 🟡 Medium |
| 12 | `sysctl.conf` | Added `kernel.kptr_restrict = 2` — hides kernel pointers from all users | 🟡 Medium |
| 13 | `sysctl.conf` | Added `kernel.yama.ptrace_scope = 1` — restricts ptrace to parent processes | 🟡 Medium |
| 14 | `sysctl.conf` | Added `kernel.sysrq = 0` — disables magic SysRq key | 🟢 Low |
| 15 | `sysctl.conf` | Added `fs.suid_dumpable = 0` — prevents core dumps from SUID programs | 🟡 Medium |
| 16 | `sysctl.conf` | Added `net.ipv4.tcp_fastopen = 3` — enables TCP Fast Open for performance | 🟢 Low |
| 17 | `sysctl.conf` | Increased `fs.inotify.max_user_watches = 524288` — supports large codebases in VS Code | 🟢 Low |
| 18 | `sysctl.conf` | Set `vm.swappiness = 10` (was default 60) — reduces swap thrashing | 🟢 Low |

### Shell Configuration (bashrc & profile)

| # | File | Improvement | Priority |
|---|---|---|---|
| 19 | `bashrc` | Removed duplicate PATH entries — consolidated into single block | 🟢 Low |
| 20 | `bashrc` | Added `HISTCONTROL=ignoreboth:erasedups` — prevents duplicate history and commands starting with space | 🟢 Low |
| 21 | `bashrc` | Increased `HISTSIZE` to 10000 (was 1000) — retains more command history | 🟢 Low |
| 22 | `bashrc` | Added `HISTTIMEFORMAT` — timestamps in history for forensic review | 🟡 Medium |
| 23 | `bashrc` | Added `shopt -s globstar` — enables recursive globbing with `**` | 🟢 Low |
| 24 | `bashrc` | Added `alias rm='rm -I'` — interactive delete for 3+ files (was `rm -i` which prompts for every file) | 🟢 Low |
| 25 | `profile` | Added `umask 027` — restricts default file permissions (was 022) | 🟡 Medium |

### Git Configuration (gitconfig)

| # | File | Improvement | Priority |
|---|---|---|---|
| 26 | `gitconfig` | Set `defaultBranch = main` — modern default branch naming | 🟢 Low |
| 27 | `gitconfig` | Added `pull.rebase = true` — cleaner history, avoids merge commits | 🟢 Low |
| 28 | `gitconfig` | Added `fetch.prune = true` and `fetch.pruneTags = true` — auto-cleans stale references | 🟢 Low |
| 29 | `gitconfig` | Added `diff.algorithm = histogram` — better diff output than default Myers | 🟢 Low |
| 30 | `gitconfig` | Added `merge.conflictstyle = diff3` — shows base version in conflict markers | 🟢 Low |

---

## Duplicates Removed

The following duplicate or redundant entries were identified and removed during the merge:

| Source | Duplicate | Resolution |
|---|---|---|
| `bashrc` | Duplicate `PATH` export lines (3 instances) | Consolidated into single PATH block |
| `bashrc` | Duplicate alias definitions (`ll` defined twice) | Kept improved version with `-h` flag |
| `profile` | Redundant `PATH` entries already in `bashrc` | Removed from profile, kept in bashrc |
| `ssh_config` | Duplicate `Host *` blocks (2 blocks merged) | Merged into single `Host *` block |
| `sysctl.conf` | Duplicate `net.ipv4.tcp_syncookies` (appeared twice) | Kept single entry |
| `gitconfig` | Duplicate `[alias]` sections (2 sections) | Merged into single alias section |
| `hosts` | Duplicate loopback entries | Kept standard entries only |
| `resolv.conf` | Duplicate nameserver entries (1.1.1.1 listed twice) | Kept single entry per server |

---

## Outdated Configurations Removed

| File | Removed Entry | Reason |
|---|---|---|
| `ssh_config` | `Protocol 1` support | SSH Protocol 1 is deprecated and insecure |
| `ssh_config` | `Ciphers arcfour,blowfish-cbc` | Broken ciphers, removed from modern OpenSSH |
| `ssh_config` | `MACs hmac-md5,hmac-sha1` | Weak MAC algorithms |
| `sshd_config` | `RSAAuthentication yes` | Removed in OpenSSH 7.4+ |
| `sshd_config` | `RhostsRSAAuthentication no` | Removed in OpenSSH 7.4+ |
| `sshd_config` | `UseLogin no` | Removed in OpenSSH 7.4+ |
| `sysctl.conf` | `net.ipv4.tcp_tw_recycle = 1` | Removed from Linux 4.12+, causes issues with NAT |
| `bashrc` | `alias dir='dir --color=auto'` | Unused; GNU `ls` covers this functionality |
| `gitconfig` | `credential.helper = cache` | Replaced with `credential.helper = store` for persistence |

---

## Priority Distribution

| Priority | Count | Description |
|---|---|---|
| 🔴 High | 5 | Security-critical changes (cryptography, authentication) |
| 🟡 Medium | 8 | Security-relevant improvements (hardening, privacy) |
| 🟢 Low | 17 | Quality-of-life and best-practice updates |

---

## Recommendations for Future Audits

1. **Automate config validation** — Add a CI check that lints host configs against CIS benchmarks
2. **Version pin SSH algorithms** — Review cipher suites annually as new vulnerabilities emerge
3. **Monitor sysctl changes** — Use AIDE or similar to detect unauthorized kernel parameter modifications
4. **Test configs in container** — Validate all hostconfigs in a Docker container before deploying to production
5. **Document deviations** — Any system that deviates from these defaults should have a documented exception
