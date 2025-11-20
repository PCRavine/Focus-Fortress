# Privacy Policy for Focus Fortress

**Last Updated: November 20, 2024**

## Introduction

Focus Fortress ("we", "our", or "us") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, and safeguard your information when you use our mobile application.

## Information We Collect

### Account Information
- **Anonymous User ID**: We use Supabase authentication to create an anonymous user ID for each user. This ID is used solely to identify your session and does not contain any personally identifiable information.
- **Player Name**: You provide a display name when creating or joining a room. This name is visible to other players in your squad.

### Usage Data
- **Room Codes**: Temporary 4-character codes generated for each focus session
- **Session Data**: Timer duration, lives remaining, and session completion status
- **Fortress Progress**: Your squad's collective statistics (level, bricks collected, win streak)
- **Activity Logs**: Timestamps of when lives are lost during sessions
- **Session Participation**: We track each session you participate in, including:
  - Number of sessions per week, month, and lifetime
  - When you last participated in a session
  - Whether sessions were completed successfully or breached
  - Duration of each session
  - Which squad/room you participated with

### Device Information
- **App State**: We monitor whether the app is in the foreground or background to implement the grace period feature
- **Device Permissions**:
  - Vibration (for grace period haptic feedback)
  - Audio (for grace period warning sounds)
  - Wakelock (to keep screen awake during sessions)

## How We Use Your Information

We use the collected information to:
- Facilitate multiplayer focus sessions between squad members
- Synchronize timer and lives data across all participants in real-time
- Track fortress progress and maintain win streaks
- Implement the grace period feature when the app is backgrounded
- Provide session completion and breach notifications
- **Monitor app usage** to understand how users engage with the app
- **Improve the app** based on usage patterns and popular features
- **Support future premium features** by tracking session participation
- Analyze which features are most valuable to users

## Data Storage and Security

- All data is stored securely using Supabase (PostgreSQL database)
- Real-time synchronization uses encrypted WebSocket connections
- Session data is temporary and associated with room codes
- We implement Row Level Security (RLS) policies to protect user data
- No personally identifiable information is collected beyond your chosen display name

## Data Sharing

We do not:
- Sell your data to third parties
- Share your information with advertisers
- Use your data for marketing purposes
- Track you across other apps or websites

Your data is only shared with:
- Other members of your squad (room code, player name, session activity)
- Supabase infrastructure for data storage and real-time synchronization

## Data Retention

- **Active Sessions**: Data is retained while a room is active
- **Inactive Rooms**: Room data may be automatically deleted after extended periods of inactivity (typically 24 hours)
- **Session History**: We retain records of your session participation for analytics and to support potential premium features
- **User Profiles**: Session counters and usage statistics are retained while you use the app
- **Account Deletion**: As we use anonymous authentication, simply uninstalling the app removes your local data. Server-side data associated with your anonymous ID (including session history and usage statistics) will be retained for operational purposes but cannot be linked back to you personally.

## Children's Privacy

Focus Fortress is suitable for users of all ages. We do not knowingly collect personal information from children under 13. If you believe we have inadvertently collected such information, please contact us.

## Third-Party Services

Focus Fortress uses the following third-party services:
- **Supabase**: Backend infrastructure for authentication, database, and real-time synchronization
  - Privacy Policy: https://supabase.com/privacy

## Your Rights

You have the right to:
- Know what data we collect about you
- Request deletion of your data (contact us)
- Opt out of using the app at any time by uninstalling it

## Changes to This Privacy Policy

We may update this Privacy Policy from time to time. We will notify users of any material changes by updating the "Last Updated" date at the top of this policy.

## Contact Us

If you have questions or concerns about this Privacy Policy, please contact us at:

**Email**: [Your Email Address]
**GitHub**: https://github.com/[your-username]/focus-fortress

## Consent

By using Focus Fortress, you consent to this Privacy Policy and agree to its terms.

---

## Technical Details

### Permissions Used
- **Internet Access**: Required for real-time synchronization with other squad members
- **Vibration**: Used for haptic feedback during the grace period countdown
- **Wakelock**: Keeps the screen awake during active focus sessions to prevent accidental app backgrounding
- **Foreground Service**: Monitors app lifecycle state to detect backgrounding

### Data Processing
- All data processing occurs on secure Supabase servers
- Real-time updates use WebSocket connections with TLS encryption
- No data is processed or stored on third-party analytics platforms

### Security Measures
- Row Level Security (RLS) policies prevent unauthorized data access
- PostgreSQL database with regular automated backups
- Secure authentication tokens with automatic expiration
- No plain-text password storage (anonymous authentication only)
