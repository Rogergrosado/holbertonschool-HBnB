# Simple Web Client

In this phase, you will develop the front-end of your application using HTML5, CSS3, and JavaScript ES6. Your task is to create an interactive user interface that connects with the back-end services developed in previous phases.

## Objectives

- Develop a user-friendly interface following provided design specifications.
- Implement client-side functionality to interact with the back-end API.
- Ensure secure and efficient data handling using JavaScript.
- Apply modern web development practices to create a dynamic web application.

## Learning Goals

- Apply HTML5, CSS3, and JavaScript ES6 in a real-world project.
- Interact with back-end services using AJAX/Fetch API.
- Implement authentication mechanisms and manage user sessions.
- Use client-side scripting to enhance the user experience without page reloads.

---

## Tasks Breakdown

### 1. Design
#### Objectives
- Complete the provided HTML and CSS files to match the design specifications.
- Create the following pages:
  - Login Form
  - List of Places
  - Place Details
  - Add Review Form

#### Instructions
1. **Download Provided Files**: Use the base HTML and CSS files as a starting point.
2. **Complete HTML Structure**:
   - Use semantic HTML5 elements.
   - Ensure it matches the design specifications.
3. **Apply CSS Styles**:
   - Add necessary styles to achieve the desired design.
   - Follow the required structure (header, footer, navigation bar).
4. **Create Pages**:
   - Login Form
   - List of Places
   - Place Details
   - Add Review Form

#### Required Structure
- **Header**:
  - Include the application logo (`logo.png`) with the class `logo`.
  - Include the login button/link with the class `login-button`.
- **Footer**:
  - Indicate all rights reserved.
- **Navigation Bar**:
  - Include relevant navigation links (e.g., `index.html`, `login.html`).

#### Data Display Examples
- **Index**: Display a list of places as “cards” using the class `place-card`.
- **Place Details**: Include extended information using the class `place-details`.
- **Reviews**: Display each review as a card with the class `review-card`.

#### Styling Parameters
- **Fixed**: Use a 20px margin, 10px padding, 1px solid border, and 10px border-radius for cards.
- **Flexible**: Customize the color palette, font, and images.

---

### 2. Login
#### Objectives
- Implement login functionality using the back-end API.
- Store the JWT token in a cookie for session management.

#### Instructions
1. **Setup Event Listener**:
   - Use `preventDefault()` to handle form submission.
2. **Make API Request**:
   - Send a POST request to the login endpoint with the email and password.
3. **Handle Response**:
   - On success: Store the JWT token in a cookie and redirect to `index.html`.
   - On failure: Display an error message.

#### Example Code
```javascript
async function loginUser(email, password) {
    const response = await fetch('https://your-api-url/login', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ email, password })
    });
    if (response.ok) {
        const data = await response.json();
        document.cookie = `token=${data.access_token}; path=/`;
        window.location.href = 'index.html';
    } else {
        alert('Login failed: ' + response.statusText);
    }
}
```

---

### 3. Index
#### Objectives
- Display a list of all places.
- Fetch places data from the API and implement client-side filtering based on price.
- Show the login link only if the user is not authenticated.

#### Instructions
1. **Check Authentication**:
   - Verify the JWT token in cookies.
   - Fetch places if authenticated.
2. **Fetch Data**:
   - Send a GET request to fetch places.
   - Include the token in the `Authorization` header.
3. **Populate List**:
   - Dynamically create HTML elements to display places.
4. **Client-Side Filtering**:
   - Add event listener to the price filter dropdown.
   - Filter displayed places based on the selected price.

---

### 4. Place Details
#### Objectives
- Display detailed information about a place, including name, description, price, amenities, and reviews.
- Provide access to the add review form for authenticated users.

#### Instructions
1. **Get Place ID**:
   - Extract the place ID from the URL query parameters.
2. **Check Authentication**:
   - Display the review form if authenticated.
3. **Fetch Details**:
   - Send a GET request to fetch place details.
4. **Populate Details**:
   - Dynamically create elements to display the place’s details.

---

### 5. Add Review Form
#### Objectives
- Implement the form to add a review for a place.
- Ensure only authenticated users can submit reviews.

#### Instructions
1. **Check Authentication**:
   - Redirect unauthenticated users to the index page.
2. **Get Place ID**:
   - Extract the place ID from the URL query parameters.
3. **Setup Form Listener**:
   - Handle form submission with `preventDefault()`.
4. **Submit Review**:
   - Send a POST request to submit the review data.
   - Display a success message on success or an error message on failure.

---

## Resources
- [HTML5 Documentation](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)
- [CSS3 Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [JavaScript ES6 Features](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
- [Handling Cookies in JavaScript](https://developer.mozilla.org/en-US/docs/Web/API/Document/cookie)
- [Responsive Web Design Basics](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design)
- [FormData API](https://developer.mozilla.org/en-US/docs/Web/API/FormData)

---

## Authors

- **Roger G. Rosado** - [GitHub](https://github.com/Rogergrosado)

