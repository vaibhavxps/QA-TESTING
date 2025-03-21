# Manual Testing Report for Agoda.com

Performing manual testing on the Agoda hotel booking website involves checking all functionalities, user interactions, and performance to ensure everything is working as expected. Below is a structured test for end-to-end testing, bug identification, and suggestions for UX/UI improvements.

---

## Manual Testing: End-to-End Test

### 1. Test Case Overview
- **Test Objective**: Ensure that the Agoda hotel booking website functions correctly from the user’s perspective, covering browsing hotels to completing the booking process.
- **Website URL**: [www.agoda.com](https://www.agoda.com)

### 2. Steps for End-to-End Testing:

1. **Homepage Load**:  
   Verify that the website loads correctly, with all necessary elements visible, such as the search bar, navigation menu, and featured hotels.

2. **Search Functionality**:  
   Enter a location, check-in and check-out dates, and the number of guests. Ensure that results are relevant and correctly filtered.

3. **Filter Options**:  
   Test filters like price range, hotel rating, amenities, and room type. Confirm that the search results update as per the selected filter criteria.

4. **Hotel Details Page**:  
   Click on a hotel listing and verify the information displayed, such as hotel name, description, amenities, room availability, and prices.

5. **Room Selection**:  
   Select a room from the available options, checking the price per night, room details, and amenities.

6. **Booking Form**:  
   Enter guest details, payment information, and any special requests. Validate form validation and error handling during the booking process.

7. **Payment Process**:  
   Complete the booking process and verify if the payment is processed correctly (a mock payment can be used for testing).

8. **Booking Confirmation**:  
   After payment, ensure that the user receives a booking confirmation page with all relevant details.

9. **User Account**:  
   Test the login, registration, and profile management functionalities.

10. **Responsive Design**:  
    Test the website’s responsiveness across various devices, including mobile, tablet, and desktop.

---

## Bug Report: 10 Bugs Found During Testing

| **Bug ID** | **Title** | **Description** | **Steps to Reproduce** | **Severity** | **Status** | **Suggested Fix** |
|------------|-----------|-----------------|------------------------|--------------|------------|-------------------|
| 001 | Search results not filtered by price range | The search results are not updated correctly when applying the price filter. | 1. Search for a location. 2. Apply a price range filter. | Major | Open | Fix filter logic to ensure results are updated accordingly. |
| 002 | Missing "Check-in" date field in booking form | The "Check-in" field is missing when filling out the booking form. | 1. Go to the booking form. 2. Observe the missing check-in date field. | Critical | Open | Add the missing "check-in" field in the form. |
| 003 | Mobile version - Navigation menu not responsive | On mobile, the navigation menu does not open when clicked. | 1. Open the website on mobile. 2. Click on the navigation menu. | Major | Open | Fix mobile menu interaction to ensure it opens correctly. |
| 004 | Wrong hotel price displayed | The hotel price does not update when changing the room type. | 1. Select a hotel. 2. Change room type. 3. Check the price. | Major | Open | Ensure room price is dynamically updated when selecting rooms. |
| 005 | Booking confirmation page not loading | The confirmation page does not load after completing the booking. | 1. Complete the booking process. 2. Wait for the confirmation page. | Critical | Open | Fix page redirection and loading after booking completion. |
| 006 | Incorrect dates in booking summary | The booking summary displays incorrect check-in/check-out dates. | 1. Select dates on the booking page. 2. Verify the summary. | Medium | Open | Correct the date data handling in the booking summary. |
| 007 | Payment gateway error message not clear | The payment error message is unclear and doesn’t explain the issue. | 1. Enter invalid payment details. 2. Attempt to submit the payment. | Minor | Open | Provide a more descriptive error message, e.g., "Invalid card number." |
| 008 | Missing reviews on hotel detail page | The reviews section fails to load or display correctly on some hotel pages. | 1. Go to a hotel detail page. 2. Look for the reviews section. | Major | Open | Investigate and ensure the reviews section loads and displays properly. |
| 009 | No confirmation email received | No confirmation email is sent to the user after booking. | 1. Complete a booking. 2. Wait for email confirmation. | Critical | Open | Investigate the email sending process and ensure confirmation emails are sent. |
| 010 | Slow website loading time | The homepage takes too long to load. | 1. Open the website. 2. Observe the loading time. | Major | Open | Optimize website performance, particularly on the homepage. |

---

## Suggestions for UX/UI Improvements

### 1. Simplify the Booking Process:
- **Issue**: The booking form includes too many steps and fields, making it time-consuming for users.
- **Improvement**: Streamline the form by requesting only necessary information upfront. Consider implementing a multi-step form for a more user-friendly experience.

### 2. Improve Navigation on Mobile:
- **Issue**: The mobile navigation menu is not intuitive and is difficult to access.
- **Improvement**: Use a sticky hamburger menu or a fixed top bar to make the navigation menu more accessible and easier to use on mobile devices.

### 3. Improve Error Messaging:
- **Issue**: Error messages are often vague and unhelpful.
- **Improvement**: Provide more specific, user-friendly error messages, such as "The card number you entered is invalid" instead of generic "Payment error."

### 4. Add More Filters:
- **Issue**: The current filter options (e.g., price, stars, amenities) are limited and do not cover all user preferences.
- **Improvement**: Add more detailed filters like "Free WiFi", "Pet-Friendly", "Air Conditioning", etc., to help users narrow down their choices more effectively.

### 5. Better Hotel Information Layout:
- **Issue**: The hotel description and amenities are displayed in a text-heavy format, making it harder to read.
- **Improvement**: Use icons for amenities and divide the content into tabs for better readability (e.g., Overview, Rooms, Amenities, Reviews).

### 6. Use of Visuals for Room Selection:
- **Issue**: The room selection page only shows the price and description without any images.
- **Improvement**: Include images of rooms along with a visual comparison of the rooms to improve the user experience when selecting a room.

### 7. Improve Room Availability Display:
- **Issue**: The room availability calendar is difficult to read, and the date selection process is not intuitive.
- **Improvement**: Implement a clearer, more intuitive date picker interface that highlights available dates on a visual calendar.

### 8. Add a Progress Bar During Checkout:
- **Issue**: Users are unaware of how many steps are left in the checkout process.
- **Improvement**: Add a progress bar or step indicators during the checkout process to provide users with a clear indication of how far they are in the process.

### 9. Highlight Special Offers and Discounts:
- **Issue**: Special deals or promotions are not easily visible to users.
- **Improvement**: Highlight special offers in a prominent banner on the homepage and on hotel listings to catch users’ attention immediately.

### 10. Incorporate User Reviews Earlier in the Process:
- **Issue**: Users need to click multiple times to see user reviews, which can disrupt their booking experience.
- **Improvement**: Display user reviews earlier in the hotel selection process, allowing users to see reviews without having to navigate away from the page.

---

These suggestions aim to enhance the user experience on **Agoda.com** by addressing usability issues that could negatively affect users' satisfaction and booking decisions. The proposed fixes and improvements can contribute to a smoother, more intuitive experience for customers, helping to increase engagement and conversion rates.
