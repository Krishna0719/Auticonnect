# AutiConnect – System Design

## 1. System Architecture
The system consists of a Flutter mobile frontend and Firebase cloud backend. It follows clean architecture with separation of UI, business logic, and services.

## 2. High-Level Design
Modules:
- Authentication
- Child module
- Caretaker module
- Dynamic room system
- Wi-Fi fingerprinting
- Recommendation engine
- Messaging
- Analytics

## 3. Database Design (Firestore)

### Users
- userId
- role
- familyCode

### Families
- familyCode
- caretakerId
- childId

### Rooms
- roomId
- roomName
- familyCode

### RoomSignals
- roomId
- ssid
- signalStrength
- timestamp

### Icons
- iconId
- label
- roomId
- imageUrl
- isActive

### UsageLogs
- childId
- iconId
- roomId
- timestamp

### Messages
- senderId
- receiverId
- iconId
- timestamp
- status

## 4. Wi-Fi Fingerprinting Design
The caretaker records multiple signal samples per room. The system compares real-time RSSI values using nearest neighbor matching and selects the closest match. Confidence thresholds ensure reliability, and manual override is available.

## 5. Recommendation Engine
Hybrid scoring:
Score =
(Room Frequency × 0.5) +
(Overall Frequency × 0.3) +
(Recent Usage × 0.2)

The system dynamically prioritizes icons and updates quick access recommendations.

## 6. UI/UX Design
- Large touch targets
- Child-friendly visuals
- Minimal distractions
- Accessibility-first approach

## 7. Security Design
- Firebase authentication
- Role-based access
- Family-level isolation
- Secure Firestore rules

## 8. Data Flow
Login → Role detection → Room detection → Icon usage → Logging → Recommendation update → Messaging → Analytics.

## 9. Technology Stack
- Flutter
- Firebase Auth
- Firestore
- Firebase Storage
- Provider
- Wi-Fi plugin
- Text-to-Speech

## 10. Future Enhancements
- Emotion detection
- Voice recognition
- Machine learning prediction
- Offline support