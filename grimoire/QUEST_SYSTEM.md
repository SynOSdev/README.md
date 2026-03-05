# 🗺️ GRIMOIRE Quest System

The quest system tracks your progression through GRIMOIRE and determines your unlocks, rewards, and synOS build.

---

## Progression Mechanics

### XP and Levels

| Level | Title | XP Required | Unlock |
|-------|-------|-------------|--------|
| 1 | Initiate | 0 | Core Foundation labs |
| 5 | Apprentice | 500 | Faction-specific labs |
| 10 | Operative | 1500 | Advanced faction labs |
| 15 | Specialist | 3000 | Cross-faction labs |
| 20 | Expert | 5000 | Build Your Own labs |
| 25 | Master | 8000 | All side quests |
| 30 | GRIMOIRE Elite | 12000 | Full synOS build + post-game report |

### XP Sources

| Activity | XP |
|----------|-----|
| Lab completion | 100–300 XP |
| Side quest completion | 50–150 XP |
| Build Your Own component | 200–500 XP |
| Perfect lab score (no hints) | +50 XP bonus |
| Speed run bonus | +25 XP |
| Cross-faction lab | +75 XP bonus |

---

## Quest Types

### 🔬 Main Quests (Labs)
Primary progression through the 42 labs. Each lab is a self-contained quest with:
- **Objectives** — What you must accomplish
- **Deliverables** — What you produce/build
- **Skill checks** —验证 verification of learned skills
- **Build component** — Tool or config you create

### ⚡ Side Quests
Optional challenges that deepen specific skills. See [SIDE_QUESTS.md](SIDE_QUESTS.md).

### 🏆 Faction Quests
Special multi-lab challenges unique to each faction:
- **Crimson Circuit:** Full penetration test simulation
- **Azure Shield:** Live incident response scenario
- **Violet Nexus:** End-to-end attack-defense exercise
- **Shadow Protocol:** Complete OSINT investigation

---

## Unlock System

### How Unlocks Work
1. Complete a lab → Earn XP + unlock associated tool/config
2. Tool is auto-installed into your synOS environment
3. Personal guide is generated explaining the tool and your custom build
4. Post-game report updates with new skills and capabilities

### Unlock Categories

| Category | Examples |
|----------|---------|
| **Tools** | Network scanners, log analyzers, custom scripts |
| **Configurations** | Firewall rules, SIEM configs, detection rules |
| **Guides** | Personal how-to docs tailored to your build |
| **Dashboards** | Monitoring views, analysis workbenches |
| **Automations** | Scheduled tasks, response playbooks, pipelines |

---

## Post-Game Report

Upon completing your faction track + capstone labs, GRIMOIRE generates a comprehensive report:

1. **Skills Inventory** — Every skill learned, rated by proficiency
2. **Tools Manifest** — Every tool unlocked with usage guides
3. **Build Summary** — Your complete synOS configuration
4. **Personal Guides** — Customized documentation for YOUR system
5. **Recommended Next Steps** — Areas for continued growth
6. **Achievement Log** — Quests completed, side quests, speed runs

---

## Skill Trees

Each faction/role combination has a unique skill tree. Completing labs fills in nodes:

```
[Core Foundation] → [Faction Track] → [Advanced Ops] → [Build Your Own] → [Capstone]
         ↓                  ↓                ↓                 ↓
    [Side Quests]     [Side Quests]    [Side Quests]     [Post-Game Report]
```

Cross-faction labs become available at Level 15, allowing you to fill in skill nodes from other factions.
