## Mark Gingrass — Solutions Architect & Product Leader

*Air Force enlisted → GS-14 federal program leader. 20+ years building and shipping things that matter.*

GS-14 Program Manager at the FDA, running enterprise systems for 400+ regulatory scientists. CS + MBA. Staying technical enough to be useful at the whiteboard, not just present in the room. Currently pursuing AWS Solutions Architect – Associate while running production AWS infrastructure.

---

### Featured: [PetShots.app](https://petshots.app) — Live serverless SaaS on AWS

Built and deployed end-to-end with AWS CDK (TypeScript). Production, not a sandbox.

| Layer | Service | Decision |
|---|---|---|
| Frontend | React/TS on S3 + CloudFront (OAC) | Private bucket, ACM certs, IPv4/IPv6 |
| Auth | Cognito + PreSignUp Lambda | Bot-blocking via Turnstile; secrets in Secrets Manager |
| API | API Gateway HTTP API + Lambda router | JWT at the gateway — unauthenticated never hits Lambda |
| Storage | S3 per-user prefixes, presigned POST/GET | File bytes never pass through the API |
| Automation | EventBridge cron → Lambda → SES | Daily vaccination-expiry reminders |
| IaC | AWS CDK (TypeScript) | `RemovalPolicy.RETAIN` on all user data |

I first built the VPC + EC2 + ALB + Auto Scaling + Aurora architecture as SAA-C03 prep — then made the production call to go serverless. Near-zero idle cost. No servers to patch.

---

### Also shipped
- **GreenvilleRunClubs** — iOS app, live on the App Store
- **IWNDWYToday** — iOS habit tracker, live on the App Store
- **LaneDetectionProject1** — Computer vision / ML pipeline (Jupyter + Python)
- **Tweet2WordPress** — NLP pipeline: scrape → analyze → auto-publish

---

### Background
- U.S. Air Force veteran (avionics, mission-critical systems)
- GS-14 Program Manager & COR III, FDA Center for Tobacco Products
- CS degree + MBA · Certified Scrum Product Owner (scrum.org)
- [markgingrass.com](https://markgingrass.com) · [newsletter.markgingrass.com](https://newsletter.markgingrass.com)
