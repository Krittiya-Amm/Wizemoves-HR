# Project Card

> Output ของ Stage 0 — structured version ของ raw PM brief
> Jira: [WMMT-1498](https://sellsuki.atlassian.net/browse/WMMT-1498) — Critical / TO DO

---

## Section 1 — Project Identity

**Project name:** `Wizemoves HR — Sales Page (HR Digital Product / Document Templates)`
**Client:** `Wizemoves HR team (internal stakeholder — P'Yok HR)`
**PM:** `Amonpan (Suru) Lertbanapan` (reporter)
**Designer (lead):** `krittiya.won` (assignee)
**Date received:** `2026-06-24`
**Brief source:** `Jira card WMMT-1498 + Google Doc brief (P'Yok HR) + โครง Web Sales Page .md`

---

## Section 2 — Tier & Classification

**Project tier:**
- [x] S — landing page / single screen / < 1 week
- [ ] M — multi-screen / 1-3 weeks
- [ ] L — multi-module / 1-3 months
- [ ] Enterprise — large scope / 3+ months / multiple teams

**Tier rationale:**
`หน้าขายเดียว (single sales page) สำหรับขาย template เอกสาร HR — scope คือ 1 long-scroll page (Hook → Agitation → Solution → Value Stack → Social Proof → Risk Reversal → CTA). PM ระบุชัดว่าอยากได้ "เร็วๆ" เพราะ Suki Space รอนานเกิน`

**Client relationship:**
- [x] Returning client (internal — Wizemoves Martech project)
- [ ] First-time client
- [ ] Long-term retainer

**Urgency:**
- [x] Hard deadline signal: priority = **Critical**, PM ต้องการเร็ว (reason: HR มี template พร้อมขายแล้วแต่ยังไม่มีหน้าเว็บ — รอ Suki Space ไม่ไหว)
- [ ] Soft deadline / flexible
- [ ] No deadline (timeline TBD)

---

## Section 3 — Objective & Deliverable

**Client's objective (in their words):**
> "ทำหน้าขายสินค้าแบบหน้าเดียวสำหรับขาย template เอกสารบริษัท จากทีม HR เพื่อให้ลูกค้าจะสามารถดูแม่แบบและซื้อได้ตรงจากเว็บไซต์เลย ... อยากได้เว็บหน้าเดียวแบบเร็วๆเพื่อใช้ในการขายก่อน"

**Translated objective (1 line):**
`Long-scroll sales page หน้าเดียว ขาย 3 bundle เอกสาร HR ที่ออกแบบให้ปิดการขาย (conversion-first) พร้อม CTA ซื้อ/ลงทะเบียน`

**End users:**
`SME owners + HR managers ที่กลัวข้อพิพาทแรงงาน / อยากได้เอกสาร HR มาตรฐาน — entry จาก Facebook/LinkedIn ads + SEO`

**Deliverable list (in scope):**
- [x] Sales page (single long-scroll) ตามโครง 7 sections: Hook → Agitation → Solution + Mockups → Value Stack → Social Proof → Risk Reversal → CTA
- [x] 3 Bundle blocks: Legal Shield (4,990), Perfect Onboarding (2,990), Performance & Data Mastery (4,990)
- [x] Value Stack comparison tables (ราคาเต็ม vs offer price)
- [x] Urgency/Scarcity element (countdown timer, limited bonus)
- [x] CTA buttons → ซื้อ / ลงทะเบียนรับโค้ด (link target TBD — ดู open questions)
- [x] Responsive (mobile-first — ads traffic ส่วนใหญ่มาจากมือถือ)
- [x] Code repo + README
- [x] Staging deploy (shareable URL)
- [x] Handoff doc

**Out of scope (explicit):**
- `ระบบ payment / checkout จริง (Order Bump, One-Click Upsell เป็น future — ดู brief แต่ไม่อยู่ใน v1 ถ้าไม่มี backend)`
- `Membership area / file delivery system`
- `Email automation sequence`
- `Suki Space integration (PM บอกชัดว่าข้ามไปก่อนเพราะรอนาน)`
- `HR Consulting booking flow (CTA upsell เป็นแค่ link/anchor ใน v1)`

---

## Section 4 — Tech Stack (locked at Stage 1)

**Stack choice:**
- [x] **Modern default** (greenfield, client neutral): Next.js + TypeScript + Tailwind CSS + shadcn/ui
- [ ] Client's existing stack
- [ ] Custom modern stack

> ⚠ ห้ามใช้ Sellsuki DS 1.0 / DS 2.0 ใน project track

**Rationale:**
`Greenfield, ไม่มี existing codebase. Sales page เน้น speed + clean aesthetic (ref: paypers.ai) → Next.js static export + Tailwind + shadcn เหมาะกับ landing ที่ deploy เร็วบน Vercel. พิจารณา Framer ได้ถ้าต้องการ no-code (ref site เป็น Framer) — แต่ default = Next.js เพื่อ control + handoff repo ได้`

**Deploy target:**
- [x] Vercel (default — staging URL เร็ว)
- [ ] Other

---

## Section 5 — Milestone (S-size compressed)

**Total estimated timeline:** `~3-4 วันทำงาน (S-size, single page)`

| Stage | Day(s) | Deliverable | Client checkpoint? |
|---|---|---|---|
| 0 Brief Intake | Day 1 | PM Card | — |
| 1 Research & Plan | Day 1 | light desk research + section plan | — |
| 2 Vibe Design | Day 1-2 | 1-2 hi-fi variants (ui-ux-pro-max) | ✓ variant pick |
| 3 Vibe Code | Day 2-3 | working sales page | — |
| 4 Deploy | Day 3 | staging URL | — |
| 5 Test & Improve | Day 3-4 | iterated build | ✓ UAT (1 round) |
| 6 Handoff | Day 4 | handoff package | ✓ sign-off |

**Buffer:** `1 วัน สำหรับ copy/asset จาก HR`

---

## Section 6 — UAT Round Budget

**Budgeted rounds:** `1 (S-size)`

| Round | Status | Date | Findings (B/I/CR/OOS) |
|---|---|---|---|
| 1 | not started | | |

**Overage policy:** Round 2 triggers scope conversation with PM

---

## Section 7 — Open Questions

| # | Question | Owner | Asked by | Status |
|---|---|---|---|---|
| 1 | ปุ่ม CTA "ซื้อ" ลิงก์ไปไหน? (payment gateway / LINE / form ลงทะเบียน / external store) | PM/HR | 2026-06-25 | open |
| 2 | มี brand asset ไหม (logo Wizemoves, สี, font)? หรือให้ design ใหม่ตาม ref paypers.ai | PM/HR | 2026-06-25 | open |
| 3 | Mockup ภาพสินค้า (Excel screenshot, E-book cover, เอกสาร) มีให้ไหม หรือต้องสร้าง 3D mockup เอง | HR | 2026-06-25 | open |
| 4 | Testimonials / social proof มีของจริงไหม หรือใช้ placeholder ก่อน | HR | 2026-06-25 | open |
| 5 | ราคาขายสุดท้าย lock ที่เท่าไหร่ (brief มีทั้ง 4,990 / 2,990 / 1,999 — ขัดกัน) | HR | 2026-06-25 | open |
| 6 | Domain / hosting ปลายทาง (deploy บน Vercel ชั่วคราว หรือมี domain Wizemoves) | PM | 2026-06-25 | open |

---

## Section 8 — Risks

| # | Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|---|
| 1 | ราคาในbrief ไม่ตรงกัน (1,999 vs 2,990 vs 4,990) | high | med | lock ราคากับ HR ก่อน Stage 3 |
| 2 | ไม่มี payment system → CTA ขายไม่จบ | high | high | v1 ใช้ form/LINE ก่อน, payment เป็น future scope |
| 3 | ไม่มี asset จริง (mockup, testimonial) | med | med | ใช้ placeholder + 3D mockup generator, มาร์คชัดว่าเป็น placeholder |

---

## Section 9 — Links

- Brief source (Jira): https://sellsuki.atlassian.net/browse/WMMT-1498
- Brief (P'Yok HR Google Doc): https://docs.google.com/document/d/1U3P2vTxnKsSkh7gBnB1AT_SO0AM9m4GTjP9ly-UGGxs/edit
- Brief (local .md): `/Users/krittiyawongwattanachai/Downloads/โครง Web Sales Page HR Digital Product.md`
- Web mockup ref: https://ai.studio/apps/9492a7e4-3549-4da1-bb9d-afff86550205
- Style refs: https://paypers.ai/ , https://dsignmestudio.framer.website/ขาย-2 , https://doitfitth.com/cookbook
- Research plan: `[TBD Stage 1]`
- Design spec: `[TBD Stage 2]`
- Code repo: `[TBD]`
- Staging URL: `[TBD Stage 4]`
- Handoff doc: `[TBD Stage 6]`

---

## Status

- [x] Stage 0 — Brief Intake
- [ ] Stage 1 — Research & Plan
- [ ] Stage 2 — Vibe Design
- [ ] Stage 3 — Vibe Code
- [ ] Stage 4 — Deploy
- [ ] Stage 5 — Test & Improve
- [ ] Stage 6 — Handoff
- [ ] Closed

**Last updated:** `2026-06-25 12:54`
