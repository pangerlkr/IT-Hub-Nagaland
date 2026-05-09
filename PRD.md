# 📋 Product Requirements Document (PRD)
## IT Hub Nagaland — Open Directory

**Version:** 1.0.0  
**Date:** May 2026  
**Author:** Pangerkumzuk Longkumer  
**Status:** Active Development  

---

## 1. Overview

### 1.1 Product Vision

IT Hub Nagaland is an open-source, community-maintained directory and knowledge base that maps the entire IT ecosystem of Nagaland and North East India. The project aims to be the most comprehensive and up-to-date reference for IT institutions, government digital initiatives, private tech companies, academic programs, and digital infrastructure in the region.

### 1.2 Problem Statement

Despite growing IT investment and digital transformation efforts, there is **no single, unified, publicly accessible directory** of IT institutions and infrastructure in Nagaland and the North East. This creates:

- Fragmented access to information for students, entrepreneurs, and policymakers
- Difficulty in networking within the regional tech ecosystem
- Limited visibility for local IT companies and startups
- Barriers for investors and researchers studying the regional tech landscape
- Missed opportunities for collaboration between institutions

### 1.3 Mission

> To democratize access to information about the IT ecosystem of Nagaland and North East India through an open, collaborative, and community-driven platform.

---

## 2. Goals & Objectives

### 2.1 Primary Goals

| Goal | Description | Success Metric |
|------|-------------|----------------|
| Comprehensive Directory | List all IT institutions, companies, and infra in NE India | 100+ entries across all 8 NE states |
| Community Driven | Enable open contributions via GitHub PRs | 20+ contributors in Year 1 |
| Accuracy | Maintain verified, up-to-date entries | < 5% outdated entries |
| Accessibility | Free, open-access data for everyone | 0 paywalls |

### 2.2 Secondary Goals

- Build a structured dataset (JSON/CSV) for developers and researchers
- Enable integration with web frontends, APIs, and mapping tools
- Establish a trusted reference cited by government reports and academic papers
- Foster local tech community identity and pride

---

## 3. Target Users

### 3.1 User Personas

**🎓 Student / Job Seeker**  
- Wants to find IT companies, training centers, or internship opportunities in the region  
- Needs clear contact info, location, and type of services offered

**🚀 Entrepreneur / Startup Founder**  
- Looking for co-working spaces, innovation hubs, government IT programs, and incubators  
- Wants to identify potential partners and investors in the region

**🏛️ Policymaker / Researcher**  
- Needs a macro-level view of the IT ecosystem for planning and policy writing  
- Requires structured, verifiable data with source citations

**💻 Developer / Open Source Contributor**  
- Wants to contribute data, improve structure, or build on top of the dataset  
- Needs clean, well-structured markdown and JSON files

**📰 Journalist / Media**  
- Looking for factual, citable information about the tech landscape in NE India  
- Needs historical context and current state of IT infrastructure

---

## 4. Scope

### 4.1 In Scope (v1.0)

- [x] Government IT departments and agencies (Nagaland focus)
- [x] Academic and technical institutions (all 8 NE states)
- [x] IT companies and software firms (Kohima & Dimapur focus)
- [x] IT infrastructure: IT parks, data centers, BharatNet
- [x] Innovation hubs and startup incubators
- [x] Central government schemes active in NE India
- [x] README and PRD documentation

### 4.2 Planned Scope (v2.0)

- [ ] Interactive web frontend (Next.js / React)
- [ ] Searchable JSON/CSV dataset exports
- [ ] Geolocation mapping (Google Maps / Leaflet.js)
- [ ] API endpoint for querying institutions
- [ ] User submission form for new entries
- [ ] Verified badges for entries with official sources
- [ ] Integration with LinkedIn company pages
- [ ] Regular automated scraping for data freshness

### 4.3 Out of Scope

- Personal profiles or individual freelancer listings
- Non-IT businesses
- Political or government entities not directly related to IT

---

## 5. Data Structure

### 5.1 Institution Entry Fields

Each institution or company listed must include as many of the following as available:

```json
{
  "id": "unique-slug",
  "name": "Full Institution Name",
  "type": "Government | Academic | Private Company | Startup | NGO | Infrastructure",
  "category": "IT Department | Training Center | Software Firm | Data Center | IT Park | ISP",
  "state": "Nagaland | Assam | Manipur | Meghalaya | Tripura | Mizoram | Arunachal Pradesh | Sikkim",
  "city": "City Name",
  "address": "Full Address",
  "website": "https://example.com",
  "phone": "+91-XXXXXXXXXX",
  "email": "contact@example.com",
  "services": ["Web Development", "IT Training", "Cloud Services"],
  "established": "YYYY",
  "verified": true,
  "source": "URL or citation",
  "last_updated": "YYYY-MM-DD"
}
```

### 5.2 File Structure

```
IT-Hub-Nagaland/
├── README.md                  # Main directory (human-readable)
├── PRD.md                     # This document
├── CONTRIBUTING.md            # Contribution guidelines
├── LICENSE                    # MIT License
├── data/
│   ├── nagaland.json          # Nagaland-specific data
│   ├── assam.json             # Assam data
│   ├── manipur.json           # Manipur data
│   ├── meghalaya.json         # Meghalaya data
│   ├── tripura.json           # Tripura data
│   ├── mizoram.json           # Mizoram data
│   ├── arunachal.json         # Arunachal Pradesh data
│   ├── sikkim.json            # Sikkim data
│   └── all.json               # Combined dataset
├── docs/
│   ├── SOURCES.md             # Reference sources
│   └── CHANGELOG.md           # Version history
└── assets/
    └── map.png                # Visual map of NE India IT hubs
```

---

## 6. Contribution Guidelines

### 6.1 How to Contribute

1. Fork the repository
2. Create a new branch: `feature/add-[institution-name]`
3. Add/update the relevant entry in `README.md` and the corresponding JSON file in `/data/`
4. Ensure the entry has at least: name, type, location, and source
5. Open a Pull Request with the title: `Add: [Institution Name] — [State]`

### 6.2 Quality Standards

- All entries must be **verifiable** with at least one public source
- No promotional or advertising language
- Use consistent formatting as per existing tables
- Entries should be **neutral and factual**

### 6.3 Review Process

- PRs are reviewed within 7 days
- Maintainer may request additional sources or corrections
- Merged entries are marked as `verified: true` in JSON

---

## 7. Roadmap

### Phase 1 — Foundation (May 2026)
- [x] Repository setup
- [x] Initial README with Nagaland + NE India entries
- [x] PRD documentation
- [ ] CONTRIBUTING.md
- [ ] LICENSE file
- [ ] JSON data files

### Phase 2 — Community Growth (Q3 2026)
- [ ] Recruit 10+ contributors
- [ ] Expand to all 8 NE states with 20+ entries each
- [ ] Add structured JSON dataset exports
- [ ] Social media presence for the project

### Phase 3 — Web Platform (Q4 2026)
- [ ] Build searchable web frontend
- [ ] Deploy on Vercel/Netlify
- [ ] Add map visualization
- [ ] Public API for data access

### Phase 4 — Sustainability (2027)
- [ ] Partner with DITC Nagaland for official endorsement
- [ ] Academic citations and research integration
- [ ] Annual update cycles
- [ ] Regional tech community events

---

## 8. Success Metrics

| Metric | Target (Year 1) |
|--------|-----------------|
| Total entries | 150+ |
| GitHub Stars | 50+ |
| Contributors | 20+ |
| States covered | All 8 NE states |
| Pull Requests merged | 30+ |
| External citations | 5+ |

---

## 9. Risks & Mitigations

| Risk | Impact | Mitigation |
|------|--------|------------|
| Data becomes outdated | High | Quarterly review cycles + community reporting |
| Low contribution | Medium | Outreach to NE tech communities, Discord, Twitter |
| Inaccurate entries | High | Source verification requirement for all PRs |
| Scope creep | Medium | Strict In/Out of Scope boundaries per version |
| No official endorsement | Low | Build credibility through accuracy and citations |

---

## 10. References

- [Rising North East — IT Sector Profile](https://risingnortheast.in)
- [Advancing North East — Industry Infrastructure](https://www.advancingnortheast.in)
- [DITC Nagaland](https://nagaland.gov.in)
- [NIDC Nagaland](http://nagaind.com)
- [STPI Kohima](https://noida.stpi.in/about-guwahati-kohima)
- [NIT Nagaland](https://www.nitnagaland.ac.in)
- [NIELIT India](https://nielit.gov.in)
- [Morung Express — Nagaland IT News](https://morungexpress.com)
- [NTTC Industry 4.0 Hub](https://morungexpress.com/nagaland-bets-big-on-industry-40-hub-at-nttc-jakhalu-urges-youth-to-dream-big)

---

*This PRD is a living document and will be updated as the project evolves.*
