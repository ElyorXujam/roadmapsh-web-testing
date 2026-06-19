# Exploratory Order Attack Session — June 18, 2026

**Charter:** Explore core features by performing actions in unexpected or reverse order

**Tester:** Elyor Xujam

**Duration:** 10:00 AM - 11:30 AM

**Environment:** Chrome v125.0, Windows 11

### What I Explored
- I focused heavily on the roadmap progression tracker and user authentication flow. I opened the "Frontend Developer" roadmap in multiple browser tabs simultaneously to see how data synchronizes. I also initiated custom roadmap creation and purposely interrupted the flow by navigating away or using browser controls mid-action.
- In the "Projects" section of the roadmap, if a user submits a project, deletes the repository on GitHub, and then tries to share the link again, the system does not check if the project actually exists. Additionally, there is currently no option to restart or redo a submitted project. 

### Observations & Anomalies
- Marking a node as "Done" in Tab 1 did not instantly update Tab 2. I had to manually refresh Tab 2 to see the progress. — severity: low

### Questions Raised
- Is the lack of real-time multi-tab synchronization an intentional choice to save server resources, or should we implement WebSockets/local storage listeners?

### Coverage: Areas Touched
- Interactive Roadmap Viewer (Frontend/Backend tracks)
- Progress Tracking System
- Custom Roadmap Editor Draft Mode
- Account Settings and Profile management

### Coverage: Areas NOT Touched (and why)
- AI-tutor (i don't have pro)

### Session Quality Rating
- Bugs found that scripted testing would have missed: 2