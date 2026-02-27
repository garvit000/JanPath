# JanPath

**JanPath** is a Civic Grievance Intelligence Platform that connects citizens, municipal workers, and administrators to streamline the reporting and resolution of public grievances. The platform enables citizens to raise issues, workers to respond and resolve them, and admins to oversee operations across multiple districts.

---

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Backend Setup](#backend-setup)
  - [Web Admin Setup](#web-admin-setup)
  - [Mobile App Setup](#mobile-app-setup)
- [Roles & Access](#roles--access)
- [Contributing](#contributing)
- [License](#license)

---

## Features

- 📋 **Grievance Submission** – Citizens can submit, track, and view the status of civic complaints.
- 👷 **Worker Assignment** – Admins assign grievances to qualified workers based on skills and availability.
- 📊 **Real-time Dashboard** – Live operational overview of grievance flows and resolution progress.
- 🔐 **Role-based Access Control** – Separate interfaces and permissions for Citizens, Workers, and Admins.
- 🌍 **Multi-district Support** – Manage grievances across 150+ districts from a single platform.
- 🤖 **Neural Insights** – Surface escalation patterns and resolution bottlenecks.
- 🛡️ **Trust Layer** – Granular permissions and immutable audit trails.
- 📱 **Mobile App** – Cross-platform mobile application (Android & iOS) for on-the-go access.
- 🌐 **Multilingual Support** – i18n support in the mobile app.
- ☁️ **Firebase Integration** – Authentication and Firestore database for real-time data sync.

---

## Tech Stack

| Component   | Technology                                      |
|-------------|------------------------------------------------|
| Web Admin   | Next.js 14, React, TypeScript, Tailwind CSS, Three.js, Framer Motion |
| Mobile App  | React Native, Expo, React Navigation           |
| Backend     | Node.js (see `/backend`)                       |
| Database    | Firebase Firestore                             |
| Auth        | Firebase Authentication                        |

---

## Project Structure

```
JanPath/
├── backend/          # Backend server
├── mobile-app/       # React Native / Expo mobile application
│   ├── src/
│   │   ├── screens/  # App screens (User, Worker, Admin)
│   │   ├── i18n/     # Internationalization / translations
│   │   └── firebase.js
│   └── App.js
└── web-admin/        # Next.js web dashboard
    └── src/
        ├── app/      # Next.js App Router pages & layouts
        │   ├── auth/       # Login pages (citizen / worker / admin)
        │   └── dashboard/  # Role-specific dashboards
        ├── components/
        ├── context/
        └── lib/
```

---

## Getting Started

### Prerequisites

- **Node.js** v18 or later
- **npm** or **yarn**
- **Expo CLI** (`npm install -g expo-cli`) for the mobile app
- A **Firebase** project with Firestore and Authentication enabled

### Backend Setup

```bash
cd backend
npm install
npm start
```

### Web Admin Setup

```bash
cd web-admin
npm install
npm run dev
```

The web admin panel will be available at `http://localhost:3000`.

> **Note:** Create a `.env.local` file in the `web-admin/` directory with your Firebase configuration. Use `.env.local.bak` as a reference.

### Mobile App Setup

```bash
cd mobile-app
npm install
npx expo start
```

Scan the QR code with the **Expo Go** app on your device, or press `a` / `i` to open on an Android emulator or iOS simulator.

---

## Roles & Access

| Role    | Capabilities                                                                 |
|---------|------------------------------------------------------------------------------|
| **Citizen** | Register, submit grievances, upload photos, track status, view history   |
| **Worker**  | View assigned grievances, update status, mark issues as resolved         |
| **Admin**   | Manage all grievances, assign workers, approve worker sign-ups, view analytics |

New worker accounts require admin approval before they can access the platform.

---

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add your feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

## License

This project is open source. See the [LICENSE](LICENSE) file for details.

