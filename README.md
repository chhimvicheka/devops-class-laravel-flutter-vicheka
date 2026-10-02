# DevOps Conception Class
- Student: [Name]

## Lesson 2: My CI/CD pipeline
- Project: IT Support System
- Trigger: push to feature/register
- Target: Laravel staging server + Android testing device

### Pipeline design
Code -> Test -> Build -> Release -> Deploy

1. Code: Call API | Developers | Committed | Manual
2. Test: Check API | Developers | Test result | Auto
3. Build: Tag v1.4, SMTP & build APK | Developer | Artifact pass | Auto
4. Release: Approve v1.0.2 | Release manager | Approved version | Manual
5. Deploy: Stage API and install APK | APK tester | Running app | Manual

### Controls
On test/build failure: stop, fix, and retest | Release approval by: release manager
After deployment, check: app works on the test device | If it fails: rollback or fix and redeploy
Feedback for the next change: monitor app behavior and collect tester feedback

Optional drawing: ![My pipeline](image.png)
