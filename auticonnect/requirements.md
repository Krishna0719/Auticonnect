# AutiConnect – Requirements Specification

## 1. Project Overview
AutiConnect is a mobile assistive communication system designed for individuals with mild Autism Spectrum Disorder (ASD), especially non-verbal and semi-verbal users. The application provides visual icon-based communication, adaptive recommendations, and context-aware room detection using Wi-Fi fingerprinting. The system enhances independence, communication, and caregiver monitoring.

## 2. Stakeholders
- Autistic individuals (Child users)
- Caretakers (Parents, Teachers, Therapists)
- Developers
- Healthcare and educational institutions

## 3. User Roles
### Child
- Uses visual icons to communicate
- Sends messages
- Receives personalized recommendations

### Caretaker
- Customizes rooms and icons
- Monitors communication
- Records Wi-Fi signals
- Reviews analytics

## 4. Functional Requirements

### 4.1 Authentication and Family Linking
- Register and login
- Role selection (Child or Caretaker)
- Caretaker generates unique family code
- Child joins using family code

### 4.2 Dynamic Room Management
- Create, update, delete rooms
- Custom room names
- Assign icons to rooms

### 4.3 Wi-Fi Fingerprinting
- Record multiple Wi-Fi signal strengths per room
- Store SSID, RSSI, and timestamp
- Allow unlimited samples

### 4.4 Automatic Room Detection
- Detect current room using nearest signal matching
- Manual override option

### 4.5 Icon-Based Communication
- Large grid icons
- Text labels
- Text-to-Speech
- Message sending

### 4.6 Icon Customization
- Add, edit, delete icons
- Upload custom images

### 4.7 Real-Time Messaging
- Child sends messages
- Caretaker receives and replies

### 4.8 Recommendation System
- Hybrid scoring
- Dynamic prioritization
- Quick access icons

### 4.9 Analytics
- Usage frequency
- Room behavior
- Time-based trends

## 5. Non-Functional Requirements
- High performance
- Accessibility-friendly UI
- Security and privacy
- Reliability
- Scalability

## 6. Constraints
- Flutter mobile platform
- Firebase backend
- Limited development time

## 7. Assumptions
- Stable Wi-Fi environment
- Users can interact with touch UI
- Mobile device availability

## 8. Success Criteria
- Improved communication efficiency
- High user satisfaction
- Accurate room detection