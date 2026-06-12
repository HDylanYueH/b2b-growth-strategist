# B2B Growth Strategist (Claude Skill)

一个通用的 B2B 商业分析与增长策略 Claude Skill。将增长目标转化为可执行的商业策略与
BD打法 —— 市场/行业分析、目标公司研究、BD策略制定、销售工具生成（邮件/会议议程/POC方案）、
以及结构化商业文档输出（Word/PPT/Excel）。

A general-purpose B2B business analysis and growth-strategy skill for Claude. Turns
growth goals into executable commercial strategy — market/industry analysis, target
company research, BD strategy & entry plans, sales tool generation (cold emails,
meeting agendas, POC plans, pricing frameworks), and structured business document
output (Word/PPT/Excel).

This project is a generalized, open-source version of a skill originally built for a
specific company's BD workflow. **All company-specific information has been replaced
with a configuration file that you fill in with your own company's details.**

---

## 快速开始 / Quick Start

1. **Fork / clone this repo**, or copy the `b2b-growth-strategist/` folder into your
   Claude skills directory (e.g. `/mnt/skills/user/` for claude.ai, or your Claude
   Code / Claude Desktop skills folder).

2. **Fill in your company profile.**

   Copy `config/company-profile.md` (it's a blank template) and fill in your company's
   information: name, products/services, target customers, competitive advantages,
   value propositions, target markets, and language preferences.

   See `config/company-profile.example.md` for a fully filled-out example
   (a fictional clean-energy components company) showing the expected level of detail.

3. **Start using it.** Trigger phrases include:
   - "帮我分析这家公司 [Company Name]" / "Analyze [Company Name] for us"
   - "帮我制定进入 [市场/国家] 的策略" / "Help me build an entry strategy for [market]"
   - "写一封开发客户的邮件" / "Write a cold outreach email to [prospect]"
   - "90天增长计划" / "Build a 90-day growth plan"
   - "生成商业一页纸" / "Generate a business one-pager"

   If `config/company-profile.md` is still blank when the skill is triggered, Claude
   will ask you to fill it in (or describe your company conversationally, and Claude
   will write the config file for you).

---

## 项目结构 / Project Structure

```
b2b-growth-strategist/
├── SKILL.md                              # Main skill definition & workflow
├── config/
│   ├── company-profile.md                # ← YOU FILL THIS IN (your company info)
│   └── company-profile.example.md        # Worked example (do not use directly)
└── references/
    ├── company-analysis-framework.md     # Target company analysis framework
    ├── bd-toolkit.md                     # BANT/MEDDICC, email templates, agendas, POC, pricing
    └── market-frameworks.md              # TAM/SAM/SOM, competitive analysis, GTM strategy
```

---

## 核心工作流 / Core Workflow

The skill follows a structured B2B growth workflow:

1. **Understand the request** — clarify goal, product, market, constraints, success criteria
2. **Target company analysis** — product/tech alignment, strategic signals, competitive vs.
   partnership classification, market entry points
3. **Business one-pager** — value proposition, ICP, ROI logic, differentiation, pricing,
   sales funnel, risks, next steps
4. **Multiple strategy paths** — fast-close / ecosystem partnership / lighthouse pilot
5. **BD toolkit** — lead qualification (BANT/MEDDICC), outreach templates, meeting agendas,
   POC proposals, pricing frameworks, objection handling
6. **Quantitative models** — TAM/SAM/SOM, unit economics, sensitivity analysis
7. **Deep-dive deliverables** — account plans, sales playbooks, 90-day growth plans

All steps reference `config/company-profile.md` as the "our company" perspective — no
company-specific information is hardcoded in the skill logic.

---

## 配置文件说明 / Config File Sections

`config/company-profile.md` covers:

| Section | Content |
|---|---|
| 1. Company Overview | Name, location, website, stage |
| 2. Core Positioning | One-paragraph "who we are" statement |
| 3. Product & Service Portfolio | List of offerings with specs and target applications |
| 4. Target Customer Segments | Who buys, what they need, buyer roles |
| 5. Competitive Advantages | Differentiation by dimension |
| 6. Value Propositions by Segment | Quantified pitch per customer type |
| 7. Potential Partnership Models | Supply, licensing, JV, channel, etc. |
| 8. Target Markets & Geography | Priority regions and verticals |
| 9. Language & Output Preferences | Conversation vs. formal output language |
| 10. Additional Context | Regulations, key accounts, known competitors, etc. |

---

## 文档输出 / Document Generation

The skill can generate formal deliverables as Word, PowerPoint, or Excel files
(business one-pagers, account plans, sales playbooks, market analysis reports,
competitive analyses) using Claude's document-generation capabilities.

---

## 贡献 / Contributing

Issues and PRs welcome — especially additional reference frameworks (e.g. industry-
specific GTM playbooks) or improvements to the company-profile schema.

## License

MIT
