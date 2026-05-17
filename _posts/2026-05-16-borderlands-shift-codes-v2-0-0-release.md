---
tags: ["2026", "Releases"]
---

## Borderlands SHiFT Codes v2.0.0

![Borderlands SHiFT Codes Banner](/images/BorderlandsSHiFTCodes/Banner.png)

I'm excited to announce the release of **Borderlands SHiFT Codes v2.0.0**. This is a major update that moves both the Android app and the web dashboard to a shared Supabase (PostgreSQL) data source, with automated loading and publishing through GitHub Actions.

### About the Application

Borderlands SHiFT Codes is an unofficial fan project designed to provide easy access to SHiFT codes for the Borderlands and Wonderlands gaming universe. This Android application serves as a convenient way to view and manage codes that can be redeemed on the official Gearbox SHiFT website or directly in-game.

### What's New in v2.0.0

**Android app.** The remote SHiFT source for the app now reads from Supabase Postgres instead of a published Google Sheets CSV.

**Data pipeline.** Remote SHiFT data is loaded into the database automatically from the repository-maintained file at `/appdata/BL_SHIFT_CODES.csv`. When changes to that file are pushed, a GitHub Actions workflow loads the updated data into Supabase.

**Dashboard.** The dashboard has moved from self-hosted hosting into this project and is published via GitHub Pages. It now uses the same Supabase-backed remote source instead of CSV. A GitHub Actions workflow republishes the dashboard when dashboard code changes are pushed. The dashboard is available at [Borderlands SHiFT Codes Dashboard](https://bmoler68.github.io/BorderlandsSHiFTCodes/).

This release also includes a few other miscellaneous cleanup and optimization changes.

### Download and Resources

- **📥 Download APK**: [Application Releases](https://www.brianmoler.com/releases/releases.html)
- **🔗 GitHub Repository**: [BorderlandsSHiFTCodes on GitHub](https://github.com/bmoler68/BorderlandsSHiFTCodes)
- **📊 Dashboard**: [Borderlands SHiFT Codes Dashboard](https://bmoler68.github.io/BorderlandsSHiFTCodes/)

For questions, support, or feedback, please contact me at bmoler@brianmoler.com.
