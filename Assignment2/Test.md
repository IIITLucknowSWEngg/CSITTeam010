# Feature: User Registration

## Scenario: User registers successfully

### Given:
The user is on the registration page.

### When:
The user enters valid information (name, email, password).

### Then:
The user should be successfully registered.  
The user should be redirected to the login page.

## Chai.js Code:

```javascript
const chai = require('chai');
const expect = chai.expect;
const registrationPage = require('../pages/registrationPage');

describe('User Registration', function() {
  it('should register user successfully', function() {
    registrationPage.open();
    registrationPage.fillRegistrationForm('Jane Doe', 'jane@example.com', 'securePass123');
    registrationPage.submitForm();
    expect(registrationPage.getSuccessMessage()).to.equal('Registration successful');
    expect(browser.getUrl()).to.include('/login');
  });
});
```


# *Feature: Ride Booking*  
## Scenario: User books a ride successfully  

*Given:*  
- The user is logged in.  
- The user is on the ride booking page.  

*When:*  
- The user enters valid pickup and drop-off locations.  
- The user selects a payment method.  

*Then:*  
- The ride should be successfully booked.  
- The user should receive a confirmation message.  

### *Chai.js Code:*
```
const chai = require('chai');
const expect = chai.expect;
const ridePage = require('../pages/ridePage');

describe('Ride Booking', function() {
  it('should book a ride successfully', function() {
    ridePage.open();
    ridePage.enterLocations('123 Main St', '456 Elm St');
    ridePage.selectPaymentMethod('Credit Card');
    ridePage.submitBooking();
    expect(ridePage.getConfirmationMessage()).to.equal('Ride booked successfully');
    expect(browser.getUrl()).to.include('/ride-details');
  });
});
```
# **Feature: Netflix Account Subscription**

## Scenario: User subscribes to a plan

**Given:**  
- The user is logged in.

**When:**  
- The user selects a subscription plan (e.g., Basic, Standard, Premium).

**Then:**  
- The subscription plan should be successfully applied to the user account.  
- The user should receive a confirmation message.

### **Chai.js Code:**

```javascript
const chai = require('chai');
const expect = chai.expect;
const subscriptionPage = require('../pages/subscriptionPage');

describe('Netflix Account Subscription', function() {
  it('should subscribe to a plan successfully', function() {
    subscriptionPage.open();
    subscriptionPage.selectSubscriptionPlan('Premium');
    subscriptionPage.submitSubscription();
    expect(subscriptionPage.getConfirmationMessage()).to.equal('Subscription successful');
    expect(browser.getUrl()).to.include('/account');
  });
});
```
# **Feature: Content Search**

## Scenario: User searches for a movie/show

**Given:**  
- The user is logged in.

**When:**  
- The user enters a valid movie/show title in the search bar.

**Then:**  
- The search results should display the relevant content.

### **Chai.js Code:**

```javascript
const chai = require('chai');
const expect = chai.expect;
const searchPage = require('../pages/searchPage');

describe('Content Search', function() {
  it('should return relevant search results', function() {
    searchPage.open();
    searchPage.searchContent('Stranger Things');
    expect(searchPage.getSearchResults()).to.include('Stranger Things');
  });
});
```
# **Feature: Watch Content**

## Scenario: User watches a movie/show

**Given:**  
- The user is logged in.  
- The user has an active subscription.

**When:**  
- The user selects a movie/show to watch.

**Then:**  
- The movie/show should begin playing.

### **Chai.js Code:**

```javascript
const chai = require('chai');
const expect = chai.expect;
const contentPage = require('../pages/contentPage');

describe('Watch Content', function() {
  it('should start playing the movie/show', function() {
    contentPage.open();
    contentPage.selectContent('Stranger Things');
    contentPage.play();
    expect(contentPage.isPlaying()).to.equal(true);
  });
});
```
# **Feature: User Profile Management**

## Scenario: User updates their profile information

**Given:**  
- The user is logged in.

**When:**  
- The user navigates to the profile page and updates their profile information.

**Then:**  
- The profile should be updated successfully.

### **Chai.js Code:**

```javascript
const chai = require('chai');
const expect = chai.expect;
const profilePage = require('../pages/profilePage');

describe('User Profile Management', function() {
  it('should update user profile successfully', function() {
    profilePage.open();
    profilePage.updateProfile('John Updated', 'johnupdated@example.com');
    expect(profilePage.getSuccessMessage()).to.equal('Profile updated successfully');
  });
});

