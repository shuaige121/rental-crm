# 🏠 Rental CRM System

A comprehensive property rental management system built with FlutterFlow and Firebase, designed for multi-tenant SaaS deployment.

## 📋 Features

### Core Functionality
- **🏢 Property Management** - Manage properties, rooms, amenities, and photos
- **👥 Tenant Management** - Tenant profiles, identity verification, employment records
- **📝 Lease Management** - Digital lease creation, e-signatures, automatic renewals
- **💰 Payment Processing** - Automated reminders, online payments, overdue management
- **📊 Analytics & Reporting** - Monthly reports, financial summaries, occupancy analysis
- **🔔 Automated Notifications** - Email, calendar reminders, push notifications
- **📁 Document Management** - Google Drive integration, PDF generation, document packages
- **🔐 Multi-tenant Architecture** - Company isolation, role-based access control

## 🛠 Tech Stack

- **Frontend**: FlutterFlow (Low-code Flutter development)
- **Backend**: Firebase (Firestore, Authentication, Cloud Functions, Storage)
- **Payments**: Stripe
- **Email**: SendGrid
- **Calendar**: Google Calendar API
- **Storage**: Google Drive API
- **Language**: TypeScript (Cloud Functions)

## 📦 Project Structure

```
rental-crm/
├── firebase/               # Firebase configuration
│   ├── firestore.rules    # Security rules
│   ├── firestore.indexes.json # Database indexes
│   └── storage.rules      # Storage security rules
├── functions/             # Cloud Functions
│   └── src/
│       ├── auth/         # Authentication & user management
│       ├── payments/     # Payment processing
│       ├── automation/   # Automated tasks
│       ├── analytics/    # Reports generation
│       └── utils/        # Utility functions
├── flutterflow-config.md # FlutterFlow setup guide
├── firebase.json         # Firebase project config
└── package.json          # Node.js dependencies
```

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- Firebase CLI
- FlutterFlow account
- Firebase project

### Installation

1. Clone the repository:
```bash
git clone https://github.com/shuaige121/rental-crm.git
cd rental-crm
```

2. Run the setup script:
```bash
./setup.sh
```

3. Configure environment variables:
```bash
cp .env.example functions/.env
# Edit functions/.env with your API keys
```

4. Start the development environment:
```bash
npm run dev
```

## ⚙️ Configuration

### Firebase Setup
1. Create a Firebase project: `leonard-rental-crm`
2. Enable services:
   - Authentication (Email/Password)
   - Cloud Firestore
   - Cloud Storage
   - Cloud Functions

### FlutterFlow Setup
1. Create a new FlutterFlow project
2. Connect to your Firebase project
3. Import the data structure from `flutterflow-config.md`
4. Configure authentication and roles

### Environment Variables
Required environment variables in `functions/.env`:
- `STRIPE_SECRET_KEY` - Stripe API key
- `SENDGRID_API_KEY` - SendGrid API key
- `GOOGLE_APPLICATION_CREDENTIALS` - Service account key path

## 📱 Features Detail

### User Roles
- **Super Admin** - System administration
- **Admin** - Company management, full access
- **Tenant** - View own lease, make payments

### Payment Integration
- Stripe for subscription billing
- PayNow (Singapore) for rent payments
- Automated payment reminders
- Late fee calculation

### Automation
- Daily payment reminder checks
- Automatic lease renewal notifications
- Document generation and packaging
- Calendar event creation
- Email notifications

## 🔒 Security

- Role-based access control (RBAC)
- Multi-tenant data isolation
- Firestore security rules
- Custom claims for user roles
- Encrypted sensitive data

## 📊 Analytics

The system provides comprehensive reporting:
- Monthly revenue reports
- Tenant payment history
- Property occupancy rates
- Financial summaries
- Custom date range reports

## 🌍 Localization

Supports multiple languages:
- English
- Simplified Chinese (简体中文)

## 📝 API Documentation

### Cloud Functions Endpoints

```typescript
POST /createUserWithRole     // Create user with specific role
POST /sendPaymentReminder    // Send payment reminder email
POST /generateMonthlyReport  // Generate monthly report
POST /validateTenantData    // Validate tenant information
POST /processSignedDocument  // Process signed documents
POST /createCheckoutSession  // Create Stripe checkout
POST /uploadToGoogleDrive   // Upload files to Drive
```

## 🧪 Testing

Run tests:
```bash
npm test
```

## 🚢 Deployment

Deploy to production:
```bash
./deploy.sh
```

## 📄 License

MIT License - see LICENSE file for details

## 👨‍💻 Author

**Leonard Chow Yi Ding**
- Email: dinggege125@gmail.com
- Company: LA PURE PTE. LTD.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📞 Support

For support, please create an issue in the GitHub repository.

---
Built with ❤️ in Singapore