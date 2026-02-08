
## Creating comprehensive requirements.md for Zentra platform

## Document Information
- **Version**: 1.0
- **Date**: February 2026
- **Status**: Seed Stage MVP
- **Target Launch**: Delhi, August 2026

---

## 1. Executive Summary

Zentra is a safety-first tourism technology platform connecting lost/confused tourists with verified, trusted local guides in India and emerging global markets. The platform bridges the gap between human assistance and technology through real-time translation, safety features, and fair economic models.

**Core Value Proposition**: "Your Local Friend in Your Pocket" - Instant, trusted, language-friendly local help anywhere, anytime.

---

## 2. Problem Statement

### 2.1 Market Pain Points
- **2.5 million tourists get lost daily in India**
- Language barriers at airports, stations, and hotels
- Overcharging by transport and local vendors (up to 300% markup)
- Missing trains, buses, and flights due to miscommunication
- Food safety concerns and allergen communication issues
- Navigation of unsafe areas unknowingly

### 2.2 Economic Impact
- **$10 billion lost annually** due to poor tourist experiences
- Lost repeat visits and negative global perception
- Panic, fear, and helplessness especially among women and elderly travelers

### 2.3 Stakeholder Suffering

#### International Tourists (1.8M annually from Japan, China, Korea)
- Zero knowledge of Hindi or English
- High dependency on strangers
- Cultural navigation challenges

#### Solo Female Travelers (3.2M annually)
- Safety is #1 concern
- Lack of verified help increases vulnerability
- Need for trusted companionship

#### Families & Senior Citizens (2.1M annually)
- Children and elderly require fast, accurate assistance
- Medical emergency concerns
- Accessibility needs

#### Local Guides (Overlooked Stakeholders)
- Underpaid by existing platforms (40-50% commission)
- Lack digital tools and verification support
- Unstable income and lack of trust on both sides

---

## 3. Solution Overview

### 3.1 Platform Definition
Zentra is a mobile + web platform that connects tourists to verified local guides within **5 minutes**, combining human assistance, real-time translation, safety technology, and fair economics.

### 3.2 Key Differentiators
- **Verified humans**, not strangers
- **Built-in safety systems** (SOS, GPS tracking)
- **80% cheaper** than hotel concierges
- **100% safer** than informal guides
- Fair guide earnings (only 12% commission vs 40-50% industry standard)

---

## 4. Functional Requirements

### 4.1 User Flow - Tourist Journey

#### Step 1: Search & Match (Target: <2 minutes)
**FR-1.1**: Tourist shall select preferred language from supported languages
**FR-1.2**: Tourist shall specify need type (navigation, translation, emergency, general guidance, food assistance, transport)
**FR-1.3**: System shall perform AI-assisted matching based on:
- Language compatibility
- Proximity (GPS-based)
- Guide availability status
- Tourist need category
- Guide specialization tags

**FR-1.4**: System shall display matched guide profiles with:
- Verification badge status
- Rating and review count
- Languages spoken
- Specializations
- Response time
- Photo and brief bio

#### Step 2: Secure Booking
**FR-2.1**: System shall support escrow payment system
**FR-2.2**: Tourist shall view transparent pricing before confirmation
**FR-2.3**: Payment shall be held in escrow until service completion
**FR-2.4**: Auto-release mechanism after service confirmation or 24-hour dispute window
**FR-2.5**: Support for multiple payment methods (UPI, cards, international wallets)

#### Step 3: Connect & Explore
**FR-3.1**: In-app chat system with message persistence
**FR-3.2**: Voice calling capability within app
**FR-3.3**: Real-time voice translation feature
**FR-3.4**: Photo and location sharing
**FR-3.5**: Session timer and cost tracker

#### Step 4: Emergency Support
**FR-4.1**: One-tap panic button accessible from all screens
**FR-4.2**: Automatic GPS location sharing with:
- Local police/emergency services
- Pre-configured emergency contacts
- Zentra support team

**FR-4.3**: Emergency escalation protocols
**FR-4.4**: Offline emergency mode (SMS-based location sharing)

### 4.2 User Flow - Guide Journey

**FR-G1**: Guide onboarding with document verification
**FR-G2**: Background check integration
**FR-G3**: Language proficiency testing
**FR-G4**: Training module completion
**FR-G5**: Availability toggle and schedule management
**FR-G6**: Earnings dashboard with transaction history
**FR-G7**: Rating and review management
**FR-G8**: Dispute resolution center

### 4.3 Core Features

#### 4.3.1 Multilingual Support
**FR-M1**: Support for minimum languages:
- Tourist: English, Japanese, Mandarin, Korean, French, German, Spanish, Arabic
- Local: Hindi, Tamil, Telugu, Bengali, Marathi, Gujarati, Punjabi, Kannada, Malayalam

**FR-M2**: AI-powered real-time voice translation
**FR-M3**: Text translation in chat
**FR-M4**: Cultural context tips for guides

#### 4.3.2 Safety & Trust
**FR-S1**: Government ID verification for all guides
**FR-S2**: Criminal background checks
**FR-S3**: Real-time GPS tracking during active sessions
**FR-S4**: Session recording (with consent) for dispute resolution
**FR-S5**: 24/7 support hotline
**FR-S6**: Safety check-ins every 30 minutes during sessions
**FR-S7**: Safe zone mapping (areas to avoid)

#### 4.3.3 Financial Systems
**FR-F1**: Transparent pricing calculator
**FR-F2**: Commission split (12% platform, 88% guide)
**FR-F3**: Instant payout option for guides (minus fee)
**FR-F4**: Weekly settlement option
**FR-F5**: Tax documentation generation
**FR-F6**: Refund processing within 48 hours

#### 4.3.4 Admin & Operations
**FR-A1**: Super admin dashboard
**FR-A2**: Guide verification workflow
**FR-A3**: Dispute management system
**FR-A4**: Analytics and reporting
**FR-A5**: Content management system
**FR-A6**: Marketing campaign management

---

## 5. Non-Functional Requirements

### 5.1 Performance
**NFR-1**: Matchmaking response time < 2 minutes (95th percentile)
**NFR-2**: App launch time < 3 seconds
**NFR-3**: Translation latency < 2 seconds
**NFR-4**: Support 10,000 concurrent users at launch
**NFR-5**: 99.9% uptime SLA

### 5.2 Security
**NFR-6**: End-to-end encryption for all communications
**NFR-7**: PCI DSS compliance for payments
**NFR-8**: GDPR compliance for international users
**NFR-9**: Data localization for Indian users
**NFR-10**: Regular security audits (quarterly)

### 5.3 Scalability
**NFR-11**: Horizontal scaling architecture
**NFR-12**: CDN for static assets
**NFR-13**: Database sharding strategy for multi-city expansion

### 5.4 Usability
**NFR-14**: WCAG 2.1 AA accessibility compliance
**NFR-15**: Support for low-bandwidth mode
**NFR-16**: Offline mode for critical features
**NFR-17**: Maximum 3 taps to reach emergency button

---

## 6. Revenue Model Requirements

### 6.1 Revenue Streams

**REV-1: Booking Commission (Primary)**
- 12% per transaction
- Average booking value: ₹1,000
- Guide earns: ₹880 per transaction

**REV-2: Live Voice Translation (Premium)**
- ₹80 per minute
- Usage: Emergencies and complex tasks
- Auto-triggered when language mismatch detected

**REV-3: Premium Guide Subscription**
- ₹2,400/month
- Benefits: Priority listing, verification badge, analytics dashboard

**REV-4: Future Streams (Phase 2)**
- Tourist insurance partnerships
- Hotel/airport commission referrals
- Branded safety devices rental

### 6.2 Financial Projections (Year 1)
- **Total Revenue Target**: ₹51 Crore
- **Gross Margin**: 70%
- **Guide Earnings**: ₹88 Crore
- **Cash-positive**: Month 3

---

## 7. Technical Architecture Requirements

### 7.1 Platform
- Mobile Apps: iOS (Swift) and Android (Kotlin)
- Web App: React/Next.js for guides and admin
- Backend: Node.js/Python microservices
- Database: PostgreSQL + Redis for caching
- Real-time: WebSockets for chat/calls
- Translation: Integration with Google Translate API + custom models
- Payments: Razorpay/Stripe
- Maps: Google Maps API / MapMyIndia

### 7.2 Infrastructure
- Cloud: AWS Mumbai region (primary)
- CDN: CloudFront
- Monitoring: DataDog/New Relic
- Error Tracking: Sentry
- Communication: Twilio (SMS/Voice), SendGrid (Email)

---

## 8. Go-to-Market Requirements

### 8.1 Launch Strategy
**Phase 1: Delhi (April 2026)**
- Minimum 500 verified guides
- Partnerships with 50 hotels
- Airport counter presence
- Tourism board collaboration

**Phase 2: Golden Triangle (Sept 2026)**
- Delhi, Agra, Jaipur corridor
- 2,000 guides
- Transport operator partnerships

**Phase 3: Mumbai & Goa (Dec 2026)**
- International airport focus
- Beach safety programs
- 5,000 guides

**Phase 4: Southeast Asia (2027)**
- Thailand, Vietnam, Indonesia
- Localization requirements

**Phase 5: Global (2028)**
- Europe, Americas expansion

### 8.2 Marketing Requirements
- Digital marketing budget allocation
- Guide referral incentive program
- Tourist waitlist management
- Influencer partnerships (travel bloggers)
- PR campaign for safety features

---

## 9. Compliance & Legal Requirements

**COMP-1**: GST registration and compliance
**COMP-2**: Tourism operator licenses (state-wise)
**COMP-3**: Data protection compliance (DPDP Act 2023)
**COMP-4**: Labour law compliance for guides
**COMP-5**: Insurance coverage (liability, cyber)
**COMP-6**: Foreign exchange regulations for international payments

---

## 10. Success Metrics (KPIs)

### 10.1 Business Metrics
- **Monthly Active Tourists**: 10,000 (Year 1 target)
- **Guide Activation Rate**: >70%
- **Average Session Rating**: >4.5/5
- **Customer Acquisition Cost**: <₹500
- **Lifetime Value**: >₹5,000
- **Repeat Usage Rate**: >40%

### 10.2 Safety Metrics
- **Emergency Response Time**: <5 minutes
- **Safety Incident Rate**: <0.1%
- **Dispute Resolution Time**: <48 hours

### 10.3 Financial Metrics
- **Monthly Burn Rate**: <₹8L (pre-revenue)
- **Runway**: 18 months with seed funding
- **Unit Economics**: Positive by Month 3

---

## 11. Risk Mitigation

| Risk | Impact | Mitigation |
|------|--------|------------|
| Guide supply shortage | High | Referral bonuses, training programs |
| Safety incidents | Critical | Insurance, verification, real-time monitoring |
| Payment fraud | Medium | Escrow, KYC, transaction limits |
| Regulatory changes | Medium | Legal counsel, government relations |
| Competition | Low | First-mover advantage, safety focus |

---

## 12. Future Roadmap (Post-MVP)

### Phase 2 Features
- AI travel companion (chatbot)
- Group tour management
- Itinerary planning
- Integration with booking.com, MakeMyTrip
- Wearable device integration

### Phase 3 Features
- Blockchain-based identity verification
- DAO for guide governance
- Predictive safety analytics
- Virtual reality previews

---

## 13. Investment Requirements

**Seed Funding Ask**: ₹30 Lakh

**Use of Funds**:
- Product Development: ₹18L (60%)
- Marketing & Operations: ₹7L (23%)
- Compliance & Legal: ₹3L (10%)
- Contingency: ₹2L (7%)

**Timeline**: 4-6 months to MVP with efficient outsourcing

---

## 14. Appendix

### A. Supported Languages (Phase 1)
Tourist: EN, JA, ZH, KO, FR, DE, ES, AR
Local: HI, TA, TE, BN, MR, GU, PA, KN, ML

### B. Verification Documents (Guides)
- Aadhaar Card
- Police Verification Certificate
- Bank Account Details
- Language Proficiency Certificate (if claiming)

### C. Emergency Contacts Integration
- Police: 100
- Tourist Helpline: 1363
- Women Helpline: 181
- Ambulance: 108

---

**Document Owner**: Product Team  
**Review Cycle**: Monthly during MVP phase  
**Next Review**: March 2026
