# Armada Volleyball Club — Android APK project

This project turns `TALLY SHEET.xlsx` into a phone-friendly scorekeeping app using the original 12-match order and the spreadsheet's scoring/standings rules.

## Features
- Armada Volleyball Club header and supplied logo; navy/blue/teal/sand/rust palette inspired by the logo image.
- 12 matches in the same order as the workbook.
- Winner rule: at least 25 points and at least a 2-point lead.
- Automatic wins, losses, points for/against, point differential, matches played and rank.
- Ranking: wins first, then points scored; tied teams can share a rank.
- Saves scores locally on the device and exports CSV.
- No server/database required.

## Build an APK from an iPad using GitHub
1. Create a new **public or private repository** on GitHub named `armada-volleyball-club-app`.
2. Download/unzip this project. Upload the **contents** of the folder (including `.github`, `www`, `package.json`, and `capacitor.config.json`) to the repository root. On iPad, use GitHub in Safari and choose **Add file → Upload files**. If `.github` is hidden, create the workflow file via GitHub's web editor at `.github/workflows/build-apk.yml`.
3. Commit the files to the `main` branch.
4. Open the repository's **Actions** tab. Select **Build Android APK**, then **Run workflow** if it has not run automatically.
5. Wait for the workflow to finish successfully. Open the completed run and download the **Armada-Volleyball-Club-APK** artifact. GitHub downloads it as a ZIP; open the ZIP in Files to extract `app-debug.apk`.
6. Transfer the APK to an Android device and install it. Android may ask you to allow installation from that source.

## Important
- The APK produced by this workflow is a **debug APK**, suitable for direct testing/installation, not a Play Store release.
- An APK cannot be compiled natively on iPadOS itself. GitHub Actions builds it in the cloud, so no Android Studio is needed on the iPad.
- This project recreates the spreadsheet's scoring logic in a mobile interface; it does not embed the Excel workbook or support arbitrary Excel formulas/macros. Check the app against a few sample match results before using it for an official tournament.
