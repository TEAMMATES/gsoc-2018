# Sample Student

**Project: Java 8 and Google Cloud SDK Migration**

Overall Direction:
- Migrate to Java 8 runtime
- Update libraries to latest, particularly those blocked by Java 8
- Adopt Java 8 best practices and syntaxes (lambda, functional interface, etc.)
- Migrate development tools to Google Cloud SDK in CLI, Eclipse, IntelliJ
- Establish TEAMMATES as a Java 8 project

---

Week 1 Plan:
- [x] Change build/test environments to Java 8, remove/update incompatible libraries
- [x] Update all tests to pass under Java 8 environment

Week 1 Works:
- [x] Merged: [Upgrade to Java 8](https://github.com/TEAMMATES/teammates/pull/7637)

Week 1 Retrospect:

No major setback; managed to achieve the goal of allowing the whole system to run under Java 8 runtime.

Week 2 Plan:
- [x] Update CheckStyle to 8.0
- [ ] Update Selenium to 3.x

Week 2 Works:
- [x] Merged: [Update CheckStyle to 8.0](https://github.com/TEAMMATES/teammates/pull/7874)

Week 2 Retrospect:

Selenium update is delayed because there are too many failing tests.

Week 3:
- [ ] Update Selenium to 3.x
- [ ] Migrate development tools from Google Plugin to Google Cloud SDK
- [ ] Temporarily disable support for all IDEs

Week 3 Works:
- [ ] Ongoing: [Migrate development tools to Google Cloud SDK - CLI/Gradle](https://github.com/TEAMMATES/teammates/pull/8045)

Week 3 Retrospect:
- Selenium update is taken out of the action plan as it is not critical for the project's goal of supporting Java 8 runtime.
- Met some difficulties and disagreement on how to handle local datastore getting wiped out across different builds; will resolve and finish the ongoing PR by next week.

---
Week 4 (current):
- [ ] Migrate development tools from Google Plugin to Google Cloud SDK
- [ ] Temporarily disable support for all IDEs
---

Week 5:
- [ ] Migrate Eclipse development tools to Cloud Tools for Eclipse

Week 6:
- [ ] Migrate IntelliJ development tools to Cloud Tools for IntelliJ

Week 7:
- [ ] Cooling-off period for core team members to try the new routine
- [ ] Merge back to `master` branch and release as V6.0.0
