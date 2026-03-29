# PPWL8 Fullstack Monorepo

## Deskripsi
Proyek ini adalah monorepo modern yang dikelola menggunakan **Bun**. Proyek ini mengintegrasikan Backend (Node.js/Prisma), Frontend (React/Vite), dan Shared Packages untuk membangun aplikasi manajemen kelas (Classroom) dengan sistem autentikasi.

## Materi & Fitur
- **Monorepo Architecture:** Pengelolaan aplikasi backend, frontend, dan shared logic dalam satu repositori menggunakan Bun Workspaces.
- **Backend (API):** Dibangun dengan Node.js, menggunakan **Prisma ORM** untuk manajemen database (SQLite), serta fitur **Autentikasi** dan manajemen data **Classroom**.
- **Frontend (UI):** Aplikasi web berbasis **React + TypeScript + Vite** dengan integrasi **Tailwind CSS** dan **Shadcn UI** untuk antarmuka yang modern dan responsif.
- **Shared Package:** Berisi logic atau tipe data yang digunakan bersama oleh backend dan frontend untuk memastikan konsistensi kode.

## Struktur Folder
```
root/
├── apps/
│   ├── backend/       # API Server (Node.js, Prisma, Auth)
│   └── frontend/      # Web Dashboard (React, Vite, Tailwind)
├── packages/
│   └── shared/        # Shared types & utilities
├── bun.lock           # Bun lockfile
├── package.json       # Workspace configuration
└── README.md          # Dokumentasi proyek
```

## Cara Menjalankan
Pastikan Anda sudah menginstal [Bun](https://bun.sh/).

1. **Install Dependensi:**
   ```bash
   bun install
   ```

2. **Setup Database (Backend):**
   ```bash
   cd apps/backend
   bun x prisma migrate dev
   bun run prisma/seed.ts
   ```

3. **Jalankan Proyek (Development):**
   Dari root direktori, Anda bisa menjalankan semua aplikasi sekaligus:
   ```bash
   bun dev
   ```
   Atau jalankan secara spesifik:
   - Backend: `bun dev:backend`
   - Frontend: `bun dev:frontend`

---
Dikembangkan oleh: @franzxml
