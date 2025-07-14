# Diagnostic App - Complete User Flow Chart

## Mobile App User Flow

### 1. Initial Flow
```
┌─────────────────┐
│   Splash Screen │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│  Login/Signup   │
├─────────────────┤
│ • Login         │
│ • Signup        │
│ • Forgot Pass   │
│ • Reset Email   │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│   Home Screen   │
└─────────────────┘
```

### 2. Home Screen - Main Navigation
```
                    ┌─────────────────┐
                    │   Home Screen   │
                    └─────────┬───────┘
                              │
              ┌───────────────┼───────────────┐
              │               │               │
              ▼               ▼               ▼
    ┌─────────────────┐ ┌─────────────┐ ┌─────────────────┐
    │ Start Diagnosis │ │ Past Reports│ │ Recommendations │
    └─────────────────┘ └─────────────┘ └─────────────────┘
```

### 3. Start Diagnosis Flow
```
┌─────────────────┐
│ Start Diagnosis │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ Symptom Selection│
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ Step 1: Enter   │
│ Symptoms &      │
│ Details         │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ Step 2:         │
│ Additional      │
│ Questions       │
│ (if needed)     │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ Step 3:         │
│ Attachments/    │
│ Reports         │
│ (Optional)      │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ Review & Submit │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ View Diagnosis  │
│ Result          │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ • View/Edit     │
│   Profile       │
│ • Block User/   │
│   Report Issue  │
│   (optional)    │
└─────────────────┘
```

### 4. Past Reports Flow
```
┌─────────────────┐
│   Past Reports  │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ List of Previous│
│ Diagnoses       │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ View Full Report│
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ • Edit/Update   │
│   Report        │
│ • Export PDF/CSV│
│ • Delete Report │
└─────────────────┘
```

### 5. Recommendations/Guidance Flow
```
┌─────────────────┐
│ Recommendations │
│ & Guidance      │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ • View          │
│   Recommended   │
│   Actions       │
│ • Medication    │
│   Guidance      │
│ • Dosage &      │
│   Duration      │
│ • Disease &     │
│   Symptom       │
│   Education     │
└─────────────────┘
```

### 6. Profile & Settings Flow
```
┌─────────────────┐
│ Profile &       │
│ Settings        │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ • Edit Profile  │
│   Information   │
│ • Change        │
│   Password      │
│ • Notification  │
│   Preferences   │
│ • Language      │
│   Selection     │
│ • Dark Mode     │
│ • Export Data   │
│   (CSV/PDF)     │
└─────────────────┘
```

---

## Admin Panel Flow

### 1. Admin Authentication Flow
```
┌─────────────────┐
│   Admin Login   │
├─────────────────┤
│ • Login         │
│ • Forgot Pass   │
│ • Two-Factor    │
│   Auth          │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│   Dashboard     │
├─────────────────┤
│ • High-Level    │
│   Stats         │
│ • Notifications │
│ • Alerts        │
└─────────────────┘
```

### 2. Admin Dashboard - Main Navigation
```
                        ┌─────────────────┐
                        │   Dashboard     │
                        └─────────┬───────┘
                                  │
        ┌─────────────────────────┼─────────────────────────┐
        │                         │                         │
        ▼                         ▼                         ▼
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│ User Management │     │ Content Mgmt    │     │ System Config   │
└─────────────────┘     └─────────────────┘     └─────────────────┘
```

### 3. User Management Flow
```
┌─────────────────┐
│ User Management │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ • View Users    │
│ • Edit/Delete/  │
│   Block User    │
│ • Assign Roles  │
│ • Reset User    │
│   Password      │
└─────────────────┘
```

### 4. Content Management Flows

#### 4.1 Symptom Management
```
┌─────────────────┐
│ Symptom         │
│ Management      │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ • Add/Edit/     │
│   Delete        │
│   Symptoms      │
│ • Set Severity  │
│ • Mark Required/│
│   Optional      │
│ • Bulk Import/  │
│   Export        │
└─────────────────┘
```

#### 4.2 Disease Management
```
┌─────────────────┐
│ Disease         │
│ Management      │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ • Add/Edit/     │
│   Delete        │
│   Diseases      │
│ • Map Symptoms  │
│   to Diseases   │
│ • Attach Notes/ │
│   References    │
│ • Link          │
│   Diagnostic    │
│   Logic         │
└─────────────────┘
```

#### 4.3 Test Management
```
┌─────────────────┐
│ Test Management │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ • Add/Edit/     │
│   Delete Tests  │
│ • Set Test      │
│   Units &       │
│   Reference     │
│   Ranges        │
│ • Map Tests to  │
│   Diseases/     │
│   Symptoms      │
│ • Test Result   │
│   Management    │
└─────────────────┘
```

### 5. Diagnostic Logic Engine Flow
```
┌─────────────────┐
│ Diagnostic Logic│
│ Engine          │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ • Create/Edit   │
│   Rule-based    │
│   Logic         │
│ • AI/ML         │
│   Integration   │
│ • Test          │
│   Diagnostic    │
│   Paths         │
└─────────────────┘
```

### 6. Treatment Management Flow
```
┌─────────────────┐
│ Empiric         │
│ Treatment       │
│ Management      │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ • Add/Edit      │
│   Treatment     │
│   Protocols     │
│ • Map           │
│   Treatments    │
│   to Diseases   │
│ • Dosage &      │
│   Duration      │
│   Guidelines    │
│ • Link to       │
│   Education     │
│   Content       │
└─────────────────┘
```

### 7. Education Content Management Flow
```
┌─────────────────┐
│ Disease         │
│ Education       │
│ Content         │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ • Add/Edit      │
│   Informational │
│   Articles      │
│ • Upload        │
│   Multimedia    │
│ • Link Content  │
│   to Diseases/  │
│   Symptoms/     │
│   Treatments    │
└─────────────────┘
```

### 8. Reports & Analytics Flow
```
┌─────────────────┐
│ Reports &       │
│ Analytics       │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ • User Analytics│
│ • Disease Trends│
│ • System        │
│   Activity Logs │
│ • Data Export   │
│   (CSV/PDF/     │
│   Excel)        │
└─────────────────┘
```

### 9. App Configuration Flow
```
┌─────────────────┐
│ App             │
│ Configuration   │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐
│ • Manage Roles  │
│   & Permissions │
│ • Language/     │
│   Localization  │
│ • Theming       │
│   (Dark/Light)  │
│ • System        │
│   Maintenance   │
│   Tools         │
└─────────────────┘
```

## Complete System Architecture Flow

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                              DIAGNOSTIC APP SYSTEM                          │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌─────────────────────┐                    ┌─────────────────────┐        │
│  │   MOBILE APP        │                    │   ADMIN PANEL       │        │
│  │   (User Interface)  │                    │   (Management)      │        │
│  └─────────┬───────────┘                    └─────────┬───────────┘        │
│            │                                          │                    │
│            ▼                                          ▼                    │
│  ┌─────────────────────┐                    ┌─────────────────────┐        │
│  │ • Splash Screen     │                    │ • User Management   │        │
│  │ • Login/Signup      │                    │ • Content Mgmt      │        │
│  │ • Home Screen       │                    │ • Logic Engine      │        │
│  │ • Start Diagnosis   │                    │ • Reports           │        │
│  │ • Past Reports      │                    │ • Configuration     │        │
│  │ • Recommendations   │                    │ • Analytics         │        │
│  │ • Profile/Settings  │                    │ • System Maintenance│        │
│  └─────────┬───────────┘                    └─────────┬───────────┘        │
│            │                                          │                    │
│            └─────────────────┬──────────────────────────┘                    │
│                              │                                               │
│                              ▼                                               │
│                   ┌─────────────────────┐                                   │
│                   │   CORE SYSTEM       │                                   │
│                   │   DATABASE          │                                   │
│                   │                     │                                   │
│                   │ • User Data         │                                   │
│                   │ • Symptoms          │                                   │
│                   │ • Diseases          │                                   │
│                   │ • Tests             │                                   │
│                   │ • Diagnostic Logic  │                                   │
│                   │ • Treatment Data    │                                   │
│                   │ • Education Content │                                   │
│                   │ • Reports & Logs    │                                   │
│                   └─────────────────────┘                                   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

## Key Features Summary

### Mobile App Key Features:
- **User Authentication**: Login, signup, password reset
- **Diagnosis Process**: Multi-step symptom entry with optional attachments
- **History Management**: View, edit, export, and delete past reports
- **Guidance System**: Treatment recommendations and educational content
- **Profile Management**: User settings and data export

### Admin Panel Key Features:
- **User Management**: Control user access and roles
- **Content Management**: Manage symptoms, diseases, tests, and treatments
- **Logic Engine**: Configure diagnostic algorithms and rules
- **Analytics**: Track usage patterns and system performance
- **System Configuration**: Manage app settings and maintenance

This flowchart provides a comprehensive overview of both user-facing and administrative functionality for the diagnostic app system.