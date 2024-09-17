# Project Scope for Netflix Clone

## Included Features:

### 1. User Registration and Authentication:
- **User Sign-Up:**
  - Users can register using email, phone number, or social media accounts (Google, Facebook, etc.).
  - New users must provide verification via OTP (One-Time Password) or email link.
  - Password encryption using industry-standard hashing algorithms (e.g., bcrypt or Argon2).

- **Login:**
  - Users can log in using credentials (email/phone number + password) or single sign-on (SSO) via social media.
  - Support for two-factor authentication (2FA) to enhance account security.

- **Password Recovery:**
  - Users can reset forgotten passwords via email or SMS.
  - Security questions and captcha to prevent brute-force attacks.

- **Profile Management:**
  - Users can manage profile information such as name, avatar, contact info, and preferred payment method.
  - Profiles can be personalized for adults or children, with parental controls restricting specific content.

### 2. User Profiles and Roles:
- **Multiple User Profiles:**
  - A single account supports up to 5 user profiles with distinct watch histories, preferences, and recommendations.

- **Parental Control:**
  - Parents can set age restrictions on specific profiles to control what content children can access.
  - Ability to monitor and block content flagged as inappropriate for specific age groups.

- **Profile Switching:**
  - Easy switching between profiles within the same account for family members.

### 3. Content Streaming and Playback:
- **High-Quality Streaming:**
  - Adaptive bitrate streaming that adjusts video quality based on the user’s internet speed (from 480p to 4K UHD).

- **Playback Control:**
  - Standard playback controls: play, pause, forward, rewind, and skip intro.
  - Resume watching from where the user last left off across multiple devices (smartphones, smart TVs, laptops).

- **Subtitle and Language Options:**
  - Multi-language subtitle and audio track support.
  - Users can choose different subtitle fonts, colors, and sizes.
  - Automatic language detection based on user preferences or location.

- **Offline Downloads:**
  - Users can download select content for offline viewing.
  - Download quality can be adjusted to save device storage space (e.g., 720p, 1080p).

- **Device Support:**
  - Streaming on multiple devices including mobile apps, web browsers, smart TVs, Chromecast, Apple TV, and gaming consoles.

### 4. Content Discovery and Search:
- **Search Bar:**
  - Allows users to search for content by title, actors, genres, directors, or keywords.
  - Predictive search suggestions and recent searches shown in the search bar.

- **Recommendations:**
  - Personalized recommendations based on user’s watch history, genre preferences, and viewing habits.
  - "Because You Watched" section that suggests similar content.
  - Genre-based categorization: Action, Drama, Comedy, Documentaries, Kids, etc.

- **Trending and Recently Added Sections:**
  - Separate sections for "Trending Now," "Top 10 in Your Country," and "New Releases."
  - User can filter content by year, rating, or popularity.

- **User Preferences:**
  - Users can set content preferences such as genres, languages, and age ratings, which influence recommendations.

### 5. Watchlist and Favorites:
- **Watch Later:**
  - Users can add titles to their "Watch Later" list for easy access to content they intend to view.

- **Favorites:**
  - A separate section where users can mark content as their favorites and access them quickly.

- **Personalized Notifications:**
  - Users can receive notifications when new episodes or movies are added to their watchlist or favorite genres.
    
### 6. Subscription Management:
- **Subscription Plans:**
  - Three-tier subscription model: Basic (1 screen, 480p), Standard (2 screens, 1080p), and Premium (4 screens, 4K HDR).
  - Each tier has different pricing based on the number of screens and video quality.

- **Payment Methods:**
  - Multiple payment options, including credit/debit cards, PayPal, Apple Pay, and Google Wallet.
  -	Payment gateway integration for secure recurring payments.
  - Ability to pause or cancel subscriptions.

- **Subscription Upgrade/Downgrade:**
  - Users can upgrade or downgrade their subscription plan anytime.
  - Prorated billing adjustment when changing plans mid-cycle.

### 7. Content Rating and Reviews:
- **Rating:**
  - Users can rate shows and movies on a 1-5 star scale.

- **Reviews:**
  - Users can leave text reviews for content, with an option to make reviews public or private.

- **Aggregated Ratings:**
  - Display overall ratings based on user reviews.
  - Show critic ratings and reviews for specific content.

 ### 8. Download for Offline Viewing:
- **Offline Downloads:**
  - Users can download select titles for offline viewing, with file size options to suit device storage constraints.
  - Automatic download expiration after a set period (e.g., 30 days) to encourage fresh content consumption.

### 9. Push Notifications:
- **New Releases:**
  -  Notifications for new shows or movies released in a user’s favorite genres or watchlist.
-  **Reminders**:
  -  Notifications for upcoming movie/show release dates, promotional offers, and subscription renewals.
- **Customizable Preferences:**
  -  Users can control the type and frequency of notifications they receive (e.g., trailers, new releases, promotions).

### 10. Multi-Language and Localization:
  - **Localization:**
    -  The app will support multiple languages, including English, Spanish, French, German, and others.
  - **Content Based on Region:**
    -  Region-based content availability due to licensing agreements.

### Excluded Features:
 -  **Advanced AI-based Content Recommendation:**
  - No use of complex machine learning algorithms for personalized recommendations beyond basic user preferences and viewing history.
 -  **Live TV Streaming:**
  -  Excludes live broadcasting or pay-per-view events.
 - **Third-Party Streaming Integrations:**
  -  No integration with external streaming services like Hulu, Disney+, or Amazon Prime Video.
