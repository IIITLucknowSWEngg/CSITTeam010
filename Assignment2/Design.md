# Software Design Description (SDD)

## 1. Introduction

### 1.1 Purpose
The purpose of this Software Design Description (SDD) is to provide a detailed design for the Netflix clone application. This document describes the software's architecture, components, interfaces, and their interactions to ensure that the implementation meets the system's functional and non-functional requirements.

### 1.2 Scope
The Netflix clone system enables users to stream video content via a web or mobile application. The system includes user management, video playback, content browsing, subscription handling, and external integrations with payment gateways and content delivery networks (CDNs).

## 4. Module Design

### 4.1 Web/Mobile Application (Frontend)

#### 4.1.1 User Interface (UI)
The UI is designed to be intuitive, responsive, and visually appealing. The UI components include:
- Home Screen
- Content Browsing and Search
- Video Playback
- User Profile Management
- Subscription Management

#### 4.1.2 Controller Layer
Manages user requests and communicates with the service layer for processing. This includes:
- Authentication Controller
- Video Playback Controller
- Subscription Controller
- Watchlist Controller

#### 4.1.3 Service Layer
Handles business logic such as content recommendations, subscription validation, and video progress tracking.

### 4.2 Backend System (Server-side)

#### 4.2.1 API Gateway
The API Gateway serves as the entry point for all application requests. It routes requests to appropriate backend services.

#### 4.2.2 Authentication Service
Handles:
- User registration
- User login
- Password recovery and reset
- Profile management

#### 4.2.3 Content Management Service
Handles:
- Content Upload: Admin uploads videos with metadata.
- Content Categorization: Categorizes content by genre, popularity, etc.
- Content Delivery: Facilitates streaming through CDN integration.

#### 4.2.4 Recommendation Service
Uses algorithms to suggest personalized content based on user preferences and viewing history.

#### 4.2.5 Subscription Management Service
Manages:
- Subscription plans
- Billing and payment processing
- Subscription status updates

  # Netflix Clone Database Schema

## Users
| Field               | Type                     | Description                       |
|---------------------|--------------------------|-----------------------------------|
| _id               | ObjectId                | Unique identifier for the user   |
| name              | string                  | Name of the user                 |
| email             | string                  | Email address of the user        |
| phone             | string                  | Phone number of the user         |
| password          | hashed_password         | Encrypted password               |
| preferences       | { language: string, genre: [string], playback_quality: string } | User preferences for content |
| subscription_status | { type: string, expiry_date: timestamp } | Subscription plan and expiry |

---

## Profiles
| Field          | Type        | Description                          |
|----------------|-------------|--------------------------------------|
| _id          | ObjectId    | Unique identifier for the profile   |
| user_id      | ObjectId    | Relation to the Users table         |
| profile_name | string      | Name of the profile                 |
| viewing_history | [ObjectId] | List of watched content (relation with Content) |

---

## Content
| Field         | Type           | Description                           |
|---------------|----------------|---------------------------------------|
| _id         | ObjectId       | Unique identifier for the content     |
| title       | string         | Title of the movie or TV show         |
| type        | string         | Type of content (movie or TV show)    |
| genre       | [string]     | Genres of the content                 |
| release_date| timestamp      | Release date of the content           |
| rating      | float          | Rating of the content                 |
| duration    | string         | Duration (e.g., "2h 10m")             |
| cast        | [string]     | Cast members                          |
| description | string         | Description of the content            |
| language    | string         | Language of the content               |

---

## Episodes
| Field           | Type           | Description                               |
|-----------------|----------------|-------------------------------------------|
| _id           | ObjectId       | Unique identifier for the episode         |
| content_id    | ObjectId       | Relation to the Content table             |
| season        | number         | Season number                             |
| episode_number| number         | Episode number                            |
| title         | string         | Title of the episode                      |
| duration      | string         | Duration of the episode (e.g., "40m")     |
| description   | string         | Description of the episode                |

---

## Watchlist
| Field         | Type           | Description                          |
|---------------|----------------|--------------------------------------|
| _id         | ObjectId       | Unique identifier for the watchlist |
| user_id     | ObjectId       | Relation to the Users table         |
| content_ids | [ObjectId]   | List of content in the watchlist    |

---

## Payments
| Field           | Type           | Description                            |
|-----------------|----------------|----------------------------------------|
| _id           | ObjectId       | Unique identifier for the payment      |
| user_id       | ObjectId       | Relation to the Users table            |
| amount        | float          | Payment amount                         |
| payment_method| string         | Payment method (e.g., card, UPI)       |
| status        | string         | Payment status (success/failed)        |
| timestamp     | timestamp      | Payment timestamp                      |

---


## Streaming Data
| Field            | Type           | Description                             |
|------------------|----------------|-----------------------------------------|
| _id            | ObjectId       | Unique identifier for the streaming log|
| user_id        | ObjectId       | Relation to the Users table            |
| content_id     | ObjectId       | Relation to the Content table          |
| watch_timestamp| timestamp      | Timestamp of when the content was watched |
| duration_watched | string       | Duration of content watched            |
...
