# Exploratory Data Attack Session — June 19, 2026
**Charter:** Explore all input fields with unusual, long, or unexpected data

**Tester:** Elyor Xujam

**Duration:** 10:30 PM - 11:30 PM

**Environment:** Chrome v125.0, Windows 11

### What I Explored
- Targeted all text inputs across the platform, including the global search bar, custom roadmap title fields, and account profile description boxes. Tested input limits, code injection attempts, special characters, and non-Latin scripts.

### Observations & Anomalies
- Pasting a 1000-character string into the Community Roadmap Search field fail with 403 error quaitly without any user-friendly — severity: low
- Inputting Arabic text into the search bar works perfectly, but using `<script>alert(1)</script>` renders literally failed with 403 error again — severity: low
- Ever node in Custom roadmap can't automaticly size up, so i put large text in node text lacking out of box - severity: low
- Inputting emojes into the search bar returning all roadmap instead of "Not found" — severity: low
- In AI-tutor input field there is not character size limit. — severity: low
- In Profile page "Headline" input has not size limit it — severity: low

### Coverage: Areas Touched
- Global Search Component
- AI-tutorr input field
- Custom Roadmap Creation Input Forms
- User Profile Editing Fields

### Coverage: Areas NOT Touched (and why)
- Email input fields during signup (Skipped to avoid creating dozens of dummy test accounts on live auth).

### Session Quality Rating
- Bugs found that scripted testing would have missed: 4