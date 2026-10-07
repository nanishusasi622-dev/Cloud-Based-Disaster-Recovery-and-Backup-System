# Cloud-Based Disaster Recovery and Backup System

**Project Type:** Cloud Computing Mini Project  
**Technology:** HTML, CSS, JavaScript  
**Author:** S. Nanisha

## 1. Project Overview

CloudGuard DR is a browser-based academic project that demonstrates the basic workflow of a **Cloud-Based Disaster Recovery and Backup System**.

The system provides:
- Backup creation and recovery-point management
- Simulated cloud storage usage
- Recovery point restoration
- Disaster simulation
- Recovery workflow: Detect → Select Backup → Restore → Verify
- RPO and RTO display
- Activity/audit logs
- Responsive dashboard

> Note: This version is a safe **cloud workflow simulation**. It does not upload real files to a cloud provider. Browser `localStorage` is used to demonstrate the backup and recovery logic without requiring cloud credentials.

## 2. Problem Statement

Organizations depend on digital data. Hardware failures, database corruption, ransomware, power outages, and data-center failures can make important information unavailable.

A disaster recovery and backup system should protect data regularly and provide a reliable way to restore a previous recovery point.

## 3. Objectives

1. Demonstrate regular backup creation.
2. Maintain recovery points.
3. Show cloud storage usage.
4. Simulate disaster scenarios.
5. Restore the latest recovery point.
6. Display RPO and RTO objectives.
7. Maintain an activity log for backup/recovery operations.

## 4. System Architecture

```text
             +----------------------+
             |   Primary System     |
             | Application + Data   |
             +----------+-----------+
                        |
                        | Scheduled Backup
                        v
             +----------------------+
             |   Cloud Backup      |
             | Recovery Points     |
             +----------+-----------+
                        |
                        | Disaster occurs
                        v
             +----------------------+
             | Recovery Process    |
             | Detect -> Restore   |
             | -> Verify -> Resume |
             +----------------------+
```

## 5. Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Web page structure |
| CSS3 | Dashboard design and responsive layout |
| JavaScript | Backup, restore, simulation and logs |
| Browser LocalStorage | Simulated cloud persistence |
| VS Code | Development environment |
| Git/GitHub | Version control and project hosting |

## 6. Project Structure

```text
Cloud-Based-Disaster-Recovery-and-Backup-System/
│
├── index.html
├── README.md
└── assets/
    ├── style.css
    └── app.js
```

## 7. How to Run in VS Code

### Step 1
Extract the ZIP file.

### Step 2
Open VS Code.

### Step 3
Select:

`File → Open Folder`

Choose:

`Cloud-Based-Disaster-Recovery-and-Backup-System`

### Step 4
Open `index.html`.

### Step 5
Run the project using either:
- Double-click `index.html`, or
- Install the **Live Server** extension in VS Code and click **Go Live**.

## 8. How to Test

### Backup
1. Open Dashboard.
2. Click **Create Backup**.
3. Open **Backups**.
4. Confirm the recovery point appears.

### Restore
1. Open **Backups**.
2. Click **Restore**.
3. The system displays a successful restore message.

### Disaster Recovery
1. Open **Disaster Recovery**.
2. Select a disaster scenario.
3. Click **Simulate Disaster**.
4. Watch the four recovery steps.
5. The system uses the latest backup if one exists.

### Logs
Open **Activity Logs** to view backup and recovery operations.

## 9. RPO and RTO

**RPO – Recovery Point Objective:**  
The maximum amount of data that can be lost after a disaster. This demo uses 24 hours.

**RTO – Recovery Time Objective:**  
The target time required to restore service after a disaster. This demo uses 1 hour.

## 10. Disaster Recovery Workflow

```text
Disaster Detected
       ↓
Incident Identified
       ↓
Select Recovery Point
       ↓
Restore Protected Data
       ↓
Verify System
       ↓
Resume Service
```

## 11. Advantages

- Simple and user-friendly dashboard
- Demonstrates core cloud backup concepts
- Recovery points can be created quickly
- Disaster scenarios can be tested safely
- Activity logs improve visibility
- Responsive interface
- Easy to extend with a real cloud backend

## 12. Limitations

This academic version uses browser LocalStorage, so it is a simulation rather than a production cloud backup platform. It does not provide real multi-user authentication, encryption, object storage, automated server scheduling, or cross-region replication.

## 13. Future Enhancements

A production version can add:
- Firebase Authentication
- Firebase Storage / AWS S3 / Azure Blob Storage
- Real file upload and download
- Automated scheduled backups
- Database backup
- Encryption
- Multi-user access control
- Email/SMS alerts
- Cross-region disaster recovery
- Cloud monitoring and analytics

## 14. GitHub Upload

From the project folder in a terminal:

```bash
git init
git add .
git commit -m "Cloud disaster recovery and backup system"
git branch -M main
git remote add origin YOUR_GITHUB_REPOSITORY_URL
git push -u origin main
```

## 15. Deploy with GitHub Pages

1. Push the project to GitHub.
2. Open the repository.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select `main` and `/root`.
6. Click **Save**.
7. GitHub will generate a public website URL.

## 16. Conclusion

CloudGuard DR demonstrates how cloud backup and disaster recovery concepts can be represented in a simple web application. The project provides backup management, recovery-point restoration, disaster simulation, recovery objectives, and activity monitoring. It can later be connected to a real cloud storage provider for production-level functionality.
