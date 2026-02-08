# ZENTRA — Product Requirements Document
**Version:** 1.0  
**Status:** Seed Stage / MVP Development  

---

## 1. Executive Summary

Zentra is a safety-first tourism technology platform connecting lost or vulnerable tourists with verified, local guides in under 5 minutes. The platform combines human assistance, real-time translation, emergency safety features, and fair economics to solve daily tourist crises in India and emerging markets.

**Core Value Proposition:** *"Your Local Friend in Your Pocket"*

---

## 2. Problem Statement

### 2.1 Market Pain Points
- **2.5 million tourists get lost daily in India**
- Language barriers at critical transit points (airports, stations, hotels)
- Overcharging by vendors (up to 300% markup)
- Missed connections due to miscommunication
- Food safety/allergen risks
- Navigation of unsafe areas unknowingly
- **$10B annual economic loss** from poor tourist experiences

### 2.2 Affected Segments
| Segment | Annual Volume | Key Pain Point |
|---------|--------------|----------------|
| International Tourists (Japan, China, Korea) | 1.8M | Zero Hindi/English knowledge |
| Solo Female Travelers | 3.2M | Safety as #1 concern |
| Families & Senior Citizens | 2.1M | Need fast, accurate assistance |

### 2.3 Guide Side Problems
- Underpaid by existing platforms (40-50% commission)
- Lack digital tools and verification
- Unstable income, loss of trust

---

## 3. Product Vision & Goals

### 3.1 Vision
"No tourist feels helpless. Every guide earns with dignity. Technology strengthens human connection."

### 3.2 Mission
Provide instant, trusted, language-friendly local help — anywhere, anytime.

### 3.3 Success Metrics (Year 1)
- **Revenue:** ₹51 Crore
- **Gross Margin:** 70%
- **Guide Earnings:** ₹88 Crore
- **Cash Positive:** Month 3
- **Booking Commission:** 12% (₹1,000 avg booking → ₹880 guide earnings)

---

## 4. Functional Requirements

### 4.1 Core User Flows

#### Flow 1: Tourist Booking (Target: &lt;5 min to connection)
1. **Onboarding** — Multilingual registration (Hindi, English, Japanese, Mandarin, Korean)
2. **Search & Match** — Select location, need type, language
   - AI-assisted matching within 2 minutes
   - Guide profiles with ratings, verification badges, languages
3. **Secure Booking** — Escrow payment system
   - Funds held until service completion
   - Transparent pricing (no hidden fees)
4. **Connection** — In-app chat + voice calling
   - Live GPS sharing
   - Real-time voice translation
5. **Service Completion** — Release payment, rating, receipt generation

#### Flow 2: Emergency Support (Critical Safety Feature)
- **One-tap Panic Button** — Immediate alert
- **Auto-GPS Sharing** — Location sent to:
  - Local police/emergency services
  - Pre-configured family contacts
  - Zentra support team
- **Live Translation** — Emergency phrase assistance

#### Flow 3: Guide Onboarding & Management
- **Verification Process:** ID check, background verification, language testing
- **Profile Management:** Availability, service areas, specialties
- **Earnings Dashboard:** Real-time earnings, withdrawal, transaction history
- **Subscription Tier:** Premium guides (₹2,400/month) for priority listing

### 4.2 Feature Specifications

| Feature | Priority | Description | Acceptance Criteria |
|---------|----------|-------------|---------------------|
| Multilingual Onboarding | P0 | Support 5+ languages | RTL support, voice-guided setup |
| AI Matching Engine | P0 | Match tourist to guide | &lt;2 min match time, 90% satisfaction |
| Escrow Payments | P0 | Secure transaction holding | Funds released only on completion |
| Real-time Translation | P0 | Voice-to-voice translation | Support JA/ZH/KO ↔ HI/EN |
| SOS Emergency Button | P0 | One-tap safety alert | &lt;3 sec activation, GPS accuracy &lt;10m |
| In-app Communication | P1 | Chat + voice calls | End-to-end encryption |
| Trip History | P1 | Past bookings & receipts | 2-year retention, PDF export |
| Guide Verification | P1 | KYC + background checks | 48-hour verification SLA |
| Premium Subscriptions | P2 | Priority listing for guides | Stripe/Razorpay integration |
| Analytics Dashboard | P2 | Admin insights | Real-time booking metrics |

### 4.3 Translation Requirements
- **Supported Pairs:**
  - Japanese ↔ Hindi/English
  - Mandarin ↔ Hindi/English
  - Korean ↔ Hindi/English
- **Modes:** Text chat translation, Voice-to-voice real-time
- **Context Awareness:** Tourism-specific vocabulary (locations, food, transport)

---

## 5. Non-Functional Requirements

### 5.1 Performance
- **App Launch:** &lt;3 seconds
- **Match Time:** &lt;2 minutes (AI-assisted)
- **Translation Latency:** &lt;500ms for voice
- **Uptime:** 99.9% SLA

### 5.2 Security & Safety
- **Data Encryption:** AES-256 at rest, TLS 1.3 in transit
- **KYC Compliance:** Government ID verification for guides
- **GDPR/CCPA Ready:** Data portability, right to deletion
- **Emergency Response:** 24/7 human monitoring for SOS alerts

### 5.3 Scalability
- Support 10,000 concurrent users (Year 1 target)
- Horizontal scaling architecture
- CDN for static assets (images, audio)

### 5.4 Accessibility
- Voice-guided navigation for visually impaired
- High contrast mode
- Screen reader compatibility

---

## 6. Platform Requirements

### 6.1 Mobile Apps (Primary)
- **iOS:** iOS 14+, Swift/SwiftUI
- **Android:** Android 8+, Kotlin/Jetpack Compose
- **Offline Mode:** Cached maps, emergency phrases

### 6.2 Web Platform
- **Responsive Web App:** For guide management, admin
- **Browser Support:** Chrome, Safari, Firefox (last 2 versions)

### 6.3 Backend Infrastructure
- **Cloud:** AWS Mumbai / Google Cloud Mumbai (data sovereignty)
- **Database:** PostgreSQL (relational), Redis (caching/sessions)
- **Real-time:** WebSockets for chat/calls, Firebase for push notifications
- **AI/ML:** 
  - Matching algorithm (Python/TensorFlow)
  - Translation API (Google Cloud Translation / DeepL + custom models)
  - Speech-to-text (Whisper API)

---

## 7. Integration Requirements

### 7.1 Payment Gateway
- **India:** Razorpay (UPI, Cards, Wallets)
- **International:** Stripe (Cards, Apple Pay, Google Pay)
- **Escrow Logic:** Custom implementation with payment hold/release

### 7.2 Maps & Location
- **Primary:** Google Maps Platform (Places, Directions, Geocoding)
- **Fallback:** MapMyIndia (India-specific accuracy)
- **GPS Tracking:** Real-time location streaming (30s intervals during active service)

### 7.3 Communication
- **Video/Voice:** Twilio or Agora.io SDK
- **SMS:** Twilio (OTP, emergency alerts)
- **Push Notifications:** Firebase Cloud Messaging

### 7.4 Verification Services
- **KYC:** HyperVerge or IDfy (Indian market)
- **Background Checks:** Manual + API verification

---

## 8. Business Rules

### 8.1 Pricing Model
1. **Booking Commission:** 12% per transaction (Zentra keeps ₹120 on ₹1,000 booking)
2. **Live Translation:** ₹80/minute (premium add-on)
3. **Guide Subscription:** ₹2,400/month (priority placement, verified badge)

### 8.2 Cancellation Policy
- **Tourist cancel &lt;1 hour:** 50% refund
- **Tourist cancel &gt;1 hour:** Full refund minus processing fee
- **Guide no-show:** Account suspension, automatic refund

### 8.3 Dispute Resolution
- 48-hour mediation window
- Evidence collection (chat logs, GPS data)
- Arbitration team for unresolved cases

---

## 9. Regulatory & Compliance

### 9.1 India-Specific
- **PDPB Compliance:** Personal Data Protection Bill
- **GST Registration:** 18% on commission fees
- **Tourism Board Registration:** Ministry of Tourism approval
- **Police Verification:** Mandatory for all guides

### 9.2 International Expansion (2027+)
- **GDPR:** EU data residency
- **Local Tourism Laws:** Per-country guide licensing

---

## 10. Roadmap

### Phase 1: MVP (Months 1-4) — ₹20-25L Budget
- Delhi launch only
- iOS + Android apps
- Basic matching + chat
- Escrow payments
- SOS button

### Phase 2: Scale (Months 5-8)
- Golden Triangle expansion (Agra, Jaipur)
- Real-time voice translation
- Premium subscriptions
- Analytics dashboard

### Phase 3: Expansion (Months 9-12)
- Mumbai & Goa
- AI matching optimization
- Enterprise partnerships (hotels, airports)

### Phase 4: International (2027)
- Southeast Asia (Thailand, Vietnam, Indonesia)
- Multi-country guide network

---

## 11. Risks & Mitigation

| Risk | Impact | Mitigation |
|------|--------|------------|
| Guide supply shortage | High | Aggressive onboarding incentives, referral bonuses |
| Safety incidents | Critical | 24/7 monitoring, insurance partnership, strict vetting |
| Payment fraud | Medium | Escrow system, transaction limits, KYC |
| Translation accuracy | Medium | Human-in-the-loop for complex phrases, feedback loops |
| Regulatory changes | Medium | Legal advisory retainer, flexible architecture |

---

## 12. Open Questions

1. Insurance partnership for guide liability coverage?
2. Integration with Indian railway/airport authority systems?
3. Offline translation model for low-connectivity areas?
4. Accessibility partnerships (disabled traveler support)?

---

**Document Owner:** Product Team  
**Review Cycle:** Bi-weekly during MVP phase  
